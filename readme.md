# fedora-desktop-ansible #

This is my provisioner for the Fedora 29 Gnome3 / Wayland
generic desktop. Feel free to use it, modify, contribute etc.
Always interested in your comments - write me!

### Usage: ###

1. Clone this repo
1. Edit **group_vars/all.yml**
1. Install prerequisites on destination box: `dnf -y install ansible sudo python-dnf libselinux-python`
1. Create entry for your user in **/etc/sudoers.d/user** so you don't need to provide password for sudo (optional)
1. Enter proper **ansible_ssh_host** and **ansible_ssh_user** in **hosts** file
1. Make sure it works: `ansible -m ping <your_host>`
1. Copy **master.yml** to **my-laptop.yml** and adjust it to your needs.
1. Rollout: `ansible-playbook my-laptop.yml`

If you want to only update packages (like `dnf update -y` simply run:

`$ ansible-playbook my-laptop.yml --tags pkgs,update --skip-tags install`

### Contributing / committing changes ###

1. In order to modify those roles a bit to match your needs simply fork and work on your forked repo
1. If you feel like your change should be added to this repo - create Pull Request (thanks btw!)

### Managing multiple workstations ###

I use this repository in order to manage couple of workstations. Basically create 
provisioner yaml for every workstation and that's it. Thanks to that you can also easily customize every
configuration. so no need to modify **hosts** file.

Maciej Lasyk
@docent-net
https://maciej.lasyk.info

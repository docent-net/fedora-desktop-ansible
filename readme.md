This is my official provisioner for the Fedora 23 XFCE/Gnome3
desktop. Feel free to use it, modify, contribute etc.
Always interested in your comments - write me!

As for now there are 2 branches here (master for XFCE and gnome3 for Gnome3).
This will be changed in the future.

Usage:

1. Edit **group_vars/all.yml**
1. `dnf -y install ansible sudo`
2. Create entry for your user in /etc/sudoers.d/user
3. Clone this repo
4. Make sure it works: `ansible -m ping fedex-c local`
5. Rollout: `ansible-playbook master.yml`

Of course you may install just a specified part of the
whole installation by using tags. List available tags
with:

`$ ansible-playbook master.yml --list-tags`

 And install specified part with:

`$ ansible-playbook master.yml --tags dropbox,virtualbox`

If you want to only update packages (like `dnf update -y` simply run:

`$ ansible-playbook master.yml --tags pkgs,update --skip-tags install`

Maciej Lasyk
@docent-net
http://maciej.lasyk.info

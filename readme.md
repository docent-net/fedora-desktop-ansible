This is my official provisioner for the Fedora 21 desktop
Feel free to use it, modify, contribute etc
Always interested in your comments - write me!

Usage:

1. `yum -y install ansible sudo`
2. Create entry for your user in /etc/sudoers.d/user
3. Clone this repo
4. Make sure it works: ansible -m ping fedex-c local
5. Rollout: `ansible-playbook master.yml`

Of course you may install just a specified part of the
whole installation by using tags. List available tags
with:

`$ ansible-playbook master.yml --list-tags`

 And install specified part with:

`$ ansible-playbook master.yml --tags dropbox`

Maciej Lasyk
@docent-net
http://maciej.lasyk.info


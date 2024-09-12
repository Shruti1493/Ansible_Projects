### Playboom for installing and starting nginx on ubuntu docker container

 turns out my system wasn't booted using systemd as init system. So I changed the Ansible module from ansible.builtin.systemd to ansible.builtin.sysvinit

# Without using systemctl
service nginx status  
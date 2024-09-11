```bash
ansible --version
```

```bash
ansible localhost -m ping
```

To begin using Ansible as a means of managing your server infrastructure, you need to install the Ansible software on the machine that will serve as the Ansible control node.

From your control node, run the following command to include the official project’s PPA (personal package archive) in your system’s list of sources:

```bash
apt install software-properties-common
```

```bash
apt-add-repository ppa:ansible/ansible

```

```bash
apt install ansible
```

```bash
ansible localhost -m ping
```

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

#### Setting Up the Inventory File
 Although Ansible typically creates a default inventory file at etc/ansible/hosts, you are free to create inventory files in any location that better suits your needs. In this case, you’ll need to provide the path to your custom inventory file with the -i parameter when running Ansible commands and playbooks


```bash
mkdir ansible
touch hosts
```

The default inventory file provided by the Ansible installation contains a number of examples that you can use as references for setting up your inventory. The following example defines a group named [servers] with three different servers in it, each identified by a custom alias: server1, server2, and server3. Be sure to replace the highlighted IPs with the IP addresses of your Ansible hosts.
```yaml
[servers]
server1 ansible_host=203.0.113.111
server2 ansible_host=203.0.113.112
server3 ansible_host=203.0.113.113

[all:vars]
ansible_python_interpreter=/usr/bin/python3
```
The all:vars subgroup sets the ansible_python_interpreter host parameter that will be valid for all hosts included in this inventory. This parameter makes sure the remote server uses the /usr/bin/python3 Python 3 executable instead of /usr/bin/python (Python 2.7), which is not present on recent Ubuntu versions.

When you’re finished, save and close the file by pressing CTRL+X then Y and ENTER to confirm your changes.

### Whenever you want to check your inventory, you can run:

```bash
ansible-inventory --list -y
```

```bash
 apt-get update
```

```bash
apt-get install net-tools
```

```bash
 apt-get install openssh-client
```

```bash
 apt-get install coreutils
```

## Install SSH server in the target container

###  Install openssh-server:

```bash
apt-get install openssh-server
```

```bash
service ssh start
```

-   Verify SSH configuration:
    Ensure that the SSH service is running properly inside the container, and port 22 is open. You can check with:

```bash
netstat -tuln | grep 22
```

### Ensure that the SSH server is configured to allow root login. Check the SSH configuration file (/etc/ssh/sshd_config) inside the target container:

```bash
apt-get install nano
```

```bash
nano /etc/ssh/sshd_config
```

**_ PermitRootLogin yes _**

service ssh restart

### In the container from which you want to connect, ensure that openssh-client is installed.

```bash
apt-get install openssh-client
```

## Check for Running apt-get Processes:

```bash
ps aux | grep apt
```

```bash
kill -9 <PID>
```

#### To avoid the password use  rsa key pair

1. Generate key on Ansible node
```bash
ssh-keygen
```

2. Copy the generated key to the remote server 1 from ansible node
```bash
ssh-copy-id (target machine ip)
```



Number of key(s) added: 1

Now try logging into the machine, with:   "ssh '172.17.0.3'"
and check to make sure that only the key(s) you wanted were added.


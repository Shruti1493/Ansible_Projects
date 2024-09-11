```bash
 apt-get update
 ```

 ```bash
 apt-get install net-tools
 ```


```bash
 apt-get install openssh-client
 ```


### Install SSH server in the target container

- Install openssh-server:

```bash
apt-get install openssh-server
```

```bash
service ssh start
 ```

#### Verify SSH configuration:
Ensure that the SSH service is running properly inside the container, and port 22 is open. You can check with:


```bash
netstat -tuln | grep 22
 ```


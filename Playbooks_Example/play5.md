## Run A script on Remote Server

# ON Remote server

create a dir /temp/script
create a file test.sh

paste the below code
```bash
#!/bin/bash

echo "HEY SHRUTI KE"
touch testscriptfile
```

run this command to provide executable permission to the file
```bash
chmod u+x test.sh
```

# ON Ansible Node

create a file play5.yml

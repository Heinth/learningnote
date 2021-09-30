# Execute command remotely server

ssh -t username@ip "command"

```text
ssh -t user1@192.168.10.1 "service apache2 restart"
```

Here is the script for this command easy to use

```text
#!/bin/bash
##Take input server ip##
read -p " Username: " un
read -p " Server IP: " svr
read -p " Directory Path: " pth
ssh -t $un@$svr "tail -f $pth"
```


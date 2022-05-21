# Execute command remotely server

ssh -t username@ip "command"

```
ssh -t user1@192.168.10.1 "service apache2 restart"
```

Here is the script for this command easy to use

```
#!/bin/bash
##Take input server ip##
read -p " Username: " un
read -p " Server IP: " svr
read -p " Directory Path: " pth
ssh -t $un@$svr "tail -f $pth"
```

If you want to execute more than one commands, you can put ; in command.

```
ssh user1@server1.example.com ls -l /; pwd; ip addr
```

When you want to execute root privileges command

```
ssh -t user1@server1.example.com sudo ls -l /root
```

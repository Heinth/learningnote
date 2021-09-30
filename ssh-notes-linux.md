---
description: to access shell and data transfer (scp)
---

# SSH notes \(Linux\)

Log in the system with other port

```text
ssh user@ip -p port:no
# for example 
ssh hta@192.168.99.1 -p 2200
```

Disable root login 

```text
#change vi /etc/ssh/sshd_config
#permit root login yes -- permit root login no
service sshd restart
```

To change ssh default port

```text
vi /etc/ssh/sshd_config
# change the port 22 to port no
 port 2200
:wq
service sshd restart
```

data transfer with scp \(secure copy\)

```text
#command syntax-- scp file_location user@ip:/localtion
# I will send data file 
scp /home/user/data hta@192.168.99.1:/home/hta
```

Get data with scp

```text
#command syntax-- scp user@ip:/file_location receive_location
# I will take data file
scp hta@192.168.99.1:/home/hta/data /home/user/
```

Close password Authentication ssh

```text
#Change the PasswordAuthentication Yes to "No"
vi /etc/ssh/sshd_config
PasswordAuthenication no
:wq
service sshd restart
```

Ssh config file for multiple host or server

```text
touch /root/.ssh/config
vi /root/.ssh/config
##write this text to config 
#Host centos     
#HostName ip     
#Port port no   
#user username
Host centos
Hostname 192.168.99.1
Port 2200
user hta  
:wq
ssh centos
```




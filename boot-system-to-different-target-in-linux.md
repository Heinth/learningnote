# Boot system to different target in Linux

First of all I will check the current default target

```text
systemctl get-default
```

Here is the different run level of linux system

```text
Runlevel     Target Units                              Description
0	      runlevel0.target,poweroff.target       Shutdown and poweroff the system
1       runlevel1.target,rescue.target         Set up a rescue shell 
2	      runlevel2.target,multi-user.target     Set up a non-graphical multi-user system
3	      runlevel3.target,multi-user.target     Set up a non-graphical multi-user system
4       runlevel4.target,multi-user.target     Set up a non-graphical multi-user system
5	      runlevel5.target,graphical.target      Sep up a graphical multi-user system
6	      runlevel6.target,reboot.target	       Shutdown and reboot system
```

Now I will change the default target to multiuser target

```text
systemctl set-default multi-user.target
reboot
```


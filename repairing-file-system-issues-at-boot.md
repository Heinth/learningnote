# Repairing File system Issues at Boot

Reboot the server.

When the boot-loader menu appears, press any key to interrupt the countdown, except Enter

Press e to edit the current entry.

Use the cursor keys to navigate to the line that starts with linux.

Press End to move the cursor to the end of the line

Append systemd.unit=emergency.target to the end of the line.

Press Ctrl+x to boot using the modified configuration.

Log in to emergency mode. The root password is redhat.

```
Give root password for maintenance
(or press Control-D to continue): redhat
[root@servera ~]#
```

Determine which file systems are currently mounted.

```
[root@servera ~]# mount
...output omitted...
/dev/vda1 on / type xfs (ro,relatime,seclabel,attr2,inode64,noquota)
...output omitted...
```

Remount the root file system read/write.

```
[root@servera ~]# mount -o remount,rw /
```

Use the mount -a command to attempt to mount all the other file systems. With the -- all (-a) option, the command mounts all the file systems listed in /etc/fstab that are not yet mounted.

```
[root@servera ~]# mount -a
mount: /RemoveMe: mount point does not exist.
```

Edit /etc/fstab to fix the issue.

```
[root@servera ~]# vim /etc/fstab
...output omitted...
# /dev/sdz1 /RemoveMe xfs defaults 0 0
```

Update systemd for the system to register the new /etc/fstab configuration

```
[root@servera ~]# mount -a
```

reboot the system

systemctl reboot


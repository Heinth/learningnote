# Linux Challenge Notes

## Sudo

Make sure all users under "admins" group can run all commands with "sudo" and without entering any password.

```
visudo
%admins ALL=(ALL) NOPASSWD:ALL
```

Make sure all users under "devs" group can only run the "dnf" command with "sudo" and without entering any password.

```
visudo
%devs ALL=(ALL) NOPASSWD:/usr/bin/dnf
```

## Limits

Configure a "resource limit" for the "devs" group so that this group (members of the group) can not run more than "30 processes" in their session. This should be both a "hard limit" and a "soft limit", written in a single line.

```
vi /etc/security/limits.conf
@devs            -       nproc           30
```

## Quota

Edit the disk quota for the group called "devs". Limit the amount of storage space it can use (not inodes). Set a "soft" limit of "100MB" and a "hard" limit of "500MB" on "/data" partition.

First, determine the device path for `/data`

```
mount | grep '/data'
setquota -g devs 100M 500M 0 0 /dev/vdb1
```

##

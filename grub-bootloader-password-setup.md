---
description: For Redhat 6, 7 and 8
---

# Grub Bootloader password setup

For rhel 6 server,

### Using SHA-265 or SHA-512 hashes

```
#grub-crypt
```

Copy the encrypted password returned in the last line of the output which would look like a long scrambled string. Paste it before the TITLE statement in the **/boot/grub/grub.conf** file, like this

```
# vi /boot/grub/grub.conf
....
default=0
timeout=5
splashimage=(hd0,0)/grub/splash.xpm.gz
hiddenmenu
password --encrypted $6$GXGrYVEnbKXAnQoT$p64OkyclNDt4qM2q47GMsgNxJxQaclNs79gvYYsl4h07ReDtJpt5P5kQn1KQ52u2eW8pKHTqcG50ffv0UlRcW0
title Red Hat Enterprise Linux (2.6.32-358.el6.x86_64)
```

For Rhel7 and 8

Create a password for **GRUB**, be a **root** user, and open the command prompt, type the below command\


```
# grub2-setpassword 
```

This will generate a hashed GRUB bootloader password in the file **/boot/grub2/user.cfg** file and can be viewed using the [cat command](https://www.tecmint.com/13-basic-cat-command-examples-in-linux/) as shown.

```
# cat /boot/grub2/user.cfg
```

After creating the GRUB password, you need to re-create the new **GRUB** configuration file by running the following command.

```
# grub2-mkconfig -o /boot/grub2/grub.cfg
# reboot
```

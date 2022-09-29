# Fstab notes



* **Device**: usually the given name or UUID of the mounted device (sda1/sda2/etc).
* **Mount Point**: designates the directory where the device is/will be mounted.&#x20;
* **File System Type**: nothing trick here, shows the type of filesystem in use.&#x20;
* **Options**: lists any active mount options. If using multiple options they must be separated by commas.&#x20;
* **Backup Operation**: (the first digit) this is a binary system where `1` = dump utility backup of a partition. `0` = no backup. This is an outdated backup method and should NOT be used.&#x20;
* **File System Check Order**: (second digit) Here we can see three possible outcomes.  `0` means that fsck will not check the filesystem. Numbers higher than this represent the check order. The root filesystem should be set to `1` and other partitions set to `2`.

**First field – The block device (UUID,/dev/sd\*)**

**Second field – The mount point**

**Third field – The filesystem type (swap,ext4,..)**

**Fourth field – Mount options**

* `rw` (read-write);
* `suid` (respect [setuid and setgid bits](https://linuxconfig.org/how-to-use-special-permissions-the-setuid-setgid-and-sticky-bits));
* `dev` (interpret characters and block devices on the filesystem);
* `exec` (allow executing binaries and scripts);
* `auto` (mount the filesystem when the -a option of the mount command is used);
* `nouser`(make the filesystem not mountable by a standard user);
* `async` (perform I/O operations on the filesystem asynchronously).

&#x20;

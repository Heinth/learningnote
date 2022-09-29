# Fstab notes



* **Device**: usually the given name or UUID of the mounted device (sda1/sda2/etc).
* **Mount Point**: designates the directory where the device is/will be mounted.&#x20;
* **File System Type**: nothing trick here, shows the type of filesystem in use.&#x20;
* **Options**: lists any active mount options. If using multiple options they must be separated by commas.&#x20;
* **Backup Operation**: (the first digit) this is a binary system where `1` = dump utility backup of a partition. `0` = no backup. This is an outdated backup method and should NOT be used.&#x20;
* **File System Check Order**: (second digit) Here we can see three possible outcomes.  `0` means that fsck will not check the filesystem. Numbers higher than this represent the check order. The root filesystem should be set to `1` and other partitions set to `2`.&#x20;

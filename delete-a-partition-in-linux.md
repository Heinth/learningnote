# Delete a Partition in Linux

To select a disk, run the following command:

```
fdisk /dev/sdb
```

#### Delete Partitions <a href="#ftoc-heading-4" id="ftoc-heading-4"></a>

**Before deleting a partition, back up your data. All data is automatically deleted when a partition is deleted.**

To delete partition, run the **`d`** command in the **`fdisk` ** command-line utility.

The partition is automatically selected if there are no other partitions on the disk. If the disk contains multiple partitions, select a partition by typing its number.

The terminal prints out a message confirming that the partition is deleted.


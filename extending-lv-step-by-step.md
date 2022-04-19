# Extending LV step by step

Create standard partition with linux lvm type

After that create the pv with previous partition.

```
pvcreate /dev/vdb3
```

First we need to extend the existing vg first

```
vgextend vg01 /dev/vdb3
```

After extending vg , we can extend the existing lv

```
lvextend -L +300M /dev/vg01/lv01
```

Final step is we have to extend the file system

```
xfs_growfs /mnt/data
```


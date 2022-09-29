# LVM notes

LVM Creation.

First we need to create pv, after vg and lv.

```
pvcreate /dev/sdb1
vgcreate test_vg /dev/sdb1
lvcreate -n test_lv -L 10G test_vg 
             (OR)
lvcreate -n test_lv -l 100%FREE test_vg
mkfs.ext4 /dev/test_vg/test_lv
```

Second lvm remove.

Delete /etc/fstab lvm line

umount the partition and disable lvm

```
lvchange -an /dev/CVOL/workspace
lvremove /dev/test_vg/test_lv
vgremove test_vg
pvremove /dev/sdb1
```

Extend LV in existing VG & LV.

```
pvcreate /dev/sdb1
vgextend test_vg /dev/sdb1
lvextend -r -L +10G /dev/test_vg/test_lv
```

Resizing LV

```
lvreduce -L -r -2G /dev/test_vg/test_lv
```

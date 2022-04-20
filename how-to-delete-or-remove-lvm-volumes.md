# How to Delete or Remove LVM volumes

## Delete entry from /etc/fstab <a href="#6c27" id="6c27"></a>

```
# cat /etc/fstab
...
/dev/CVOL/workspace            /data              ext4    defaults        0 0
```

## unmount the partition <a href="#dcea" id="dcea"></a>

## **Disable LVM** <a href="#e7fc" id="e7fc"></a>

```
# lvchange -an /dev/CVOL/workspace
```

## **Delete LVM volume** <a href="#d2d7" id="d2d7"></a>

```
lvremove /dev/CVOL/workspace
```

## **Disable volume group** <a href="#0974" id="0974"></a>

```
# vgremove CVOL
```

## **Delete physical volumes used for volume group “vg”** <a href="#a8e1" id="a8e1"></a>

```
# pvremove /dev/sda4
```


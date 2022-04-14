# Create File of a Given Size

```
dd if=/dev/zero of=output.dat  bs=1024  count=10240
```

The above dd command creates a zero-filled file named output.dat consisting of a count of 10240 blocks, each of block size 1024.


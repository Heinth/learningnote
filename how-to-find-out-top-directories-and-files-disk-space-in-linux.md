# How to Find Out Top Directories and Files (Disk Space) in Linux

#### How to Find Biggest Files and Directories in Linux

```
# du -a /home | sort -n -r | head -n 5
```

**Find Largest Directories in Linux**

```
#du -hs * | sort -rh | head -5
```


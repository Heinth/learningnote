# Find files or dir by owner and copy

```
find /home -user "student" -type df -exec cp -rv '{}' /Testing \;
```

copying file with original folder structure

```
find /home/usersdata/ -type f -user yousuf -exec cp --parents {} /blog \;
```

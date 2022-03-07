---
description: Checking installed packages in linux
---

# 2 Ways to check installed packages in linux

#### Using RPM Package Manager

```
# rpm -qa
```

#### Using YUM Package Manager

```
# yum list installed
```

Example check command

```
# yum list installed | grep httpd
# rpm -qa | grep nginx
```

---
description: How to configure time zone in centos 8
---

# Timedate configure in Centos 8 \(Linux\)

First we need to check time zone

```text
timedatectl
```

And then set the time zone with Yangon Myanmar

```text
timedatectl set-timezone Asia/Yangon
```

After set the time zone, we need to check the result

```text
timedatectl
```


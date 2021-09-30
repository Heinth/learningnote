---
description: One time Task Scheduling
---

# at \( Linux Scheduling\)

### at \(Linux scheduling\)

service name atd 

apt install atd

```text
at 1 am
at 1 am  july 15
at 1 am tomorrow
at 1 am next month
at 1 am next year
at now + 3 min
at now + 1 week
at now + 1 hour
at now + 2 day
at noob
at -f test.sh now + 1 hour
```

After putting jobs --&gt; Ctrl+d

Checking job

```text
atq
```

Checking job id and detail

```text
at -c job_id
ex: at -c 2
```

Removing job

```text
atrm job_id
atrm 3
```


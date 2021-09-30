---
description: Linux ufw useful command
---

# Ufw \(Linux\)

Activate the firewall and Deactivate the firewall

```text
ufw enable
ufw disable
```

Check the status of ufw

```text
ufw status
ufw status numbered
```

Allow or reject the services

```text
ufw allow ssh
ufw deny ssh
```

Allow or reject the port

```text
ufw allow 22
ufw deny 22
```

Block the ip address

```text
ufw insert 1 deny from 192.168.5.254
ufw insert 1 allow from 192.168.5.254
```

When the service is updated, we need to reload

```text
ufw reload
```


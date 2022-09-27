---
description: Linux firewalld useful commad
---

# Firewalld (Linux)

Show list the firewall zones

```
firewall-cmd --list-all-zones
```

Show list of public firewall zones

```
firewall-cmd --zone=public --list-all
```

Default and active zone

```
firewall-cmd --get-default-zone
firewall-cmd --get-active-zone
```

Change the default zone

```
firewall-cmd --set-default-zone=block
firewall-cmd --set-default-zone=public
```

Allow Ports

```
firewall-cmd --permanent --add-port=9100/tcp
```

Block ip address

```
firewall-cmd --add-rich-rule='rule family=ipv4 source address="8.8.8.8" reject’
firewall-cmd --remove-rich-rule='rule family=ipv4 source address="8.8.8.8" reject’
```

When the rules are updated we have to reload the firewall&#x20;

```
firewall-cmd --reload
```

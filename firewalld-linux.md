---
description: Linux firewalld useful commad
---

# Firewalld \(Linux\)

Show list the firewall zones

```text
firewall-cmd --list-all-zones
```

Show list of public firewall zones

```text
firewall-cmd --zone=public --list-all
```

Default and active zone

```text
firewall-cmd --get-default-zone
firewall-cmd --get-active-zone
```

Change the default zone

```text
firewall-cmd --set-default-zone=block
firewall-cmd --set-default-zone=public
```

Allow & reject the services

```text
firewall-cmd --add-rich-rule='rule family=ipv4 service name="ssh" reject'
firewall-cmd --remove-rich-rule='rule family=ipv4 service name="ssh" reject'
```

Allow & Reject the services

```text
firewall-cmd --add-rich-rule='rule family=ipv4 port port="443" protocol="tcp" reject'
firewall-cmd --remove-rich-rule='rule family=ipv4 port port="443" protocol="tcp" reject'
```

Block ip address

```text
firewall-cmd --add-rich-rule='rule family=ipv4 source address="8.8.8.8" reject’
firewall-cmd --remove-rich-rule='rule family=ipv4 source address="8.8.8.8" reject’
```

When the rules are updated we have to reload the firewall 

```text
firewall-cmd --reload
```


# Register redhat subscription

Register and automatically subscribe in one step

```text
# subscription-manager register --username <username> --password <password> --auto-attach
```

Register first, then attach a subscription in the Customer Portal

```text
# subscription-manager register

# subscription-manager refresh

# subscription-manager attach --auto
```

Registration via GUI

```text
# subscription-manager-gui
```

Unregistering a system

```text
# subscription-manager remove --all
# subscription-manager unregister
# subscription-manager clean
```


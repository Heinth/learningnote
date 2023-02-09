# How to log every shell command in Linux

```
# vi /etc/rsyslog.d/bash.conf
local6.* /var/log/commands.log

# vi ~/.bashrc
whoami="$(whoami)@$(echo $SSH_CONNECTION | awk '{print $1}')"
export PROMPT_COMMAND='RETRN_VAL=$?;logger -p local6.debug "$whoami [$$]: $(history 1 | sed "s/^[ ]*[0-9]\+[ ]*//" ) [$RETRN_VAL]"'

# systemctl restart rsyslog
```

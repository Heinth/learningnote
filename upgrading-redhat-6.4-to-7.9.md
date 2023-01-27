# Upgrading redhat 6.4 to 7.9

```
In 6.4
update the latest packages
#yum update
after upgarding the packages of rhel 6.4, mount rhel 6.9 iso in server
#mount /dev/sr0 /mnt
#vi /etc/yum.repos.d/dvd.repo
***baseurl to rhel 6.9 iso
#yum repolist
#yum upgrade
Attach the redhat subscription
#subscription-manager register
#subscription-manager list --available
#subscription-manager attach --pool=8a85f9a17d76f31b017e019a918148b5
#subscription-manager repos --enable rhel-6-server-extra-rpms --enable rhel-6-server-optional-rpms
#yum install preupgrade-assistant preupgrade-el6toel7 redhat-upgrade-tool preupgrade-assistant-contents
#preupg
Disable the all repos in server
#yum-config-manager --disable \*
After that put the rhel 7.9 iso to server 
#redhat-upgrade-tool --iso /tmp/rhel-server-7.9-x86_64-dvd\ \(1\).iso --cleanup-post
#init 6
```

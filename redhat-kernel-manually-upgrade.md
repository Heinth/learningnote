# Redhat kernel manually upgrade

Download the rpm package .you can use the [Red Hat package browser](https://access.redhat.com/downloads/content/package-browser) to find the kernel you want to install

Before we install, it is good to confirm the number of kernels installed on the system

```
rpm -qa kernel
```

Installing

```
rpm -ivh kernel-3.10.0-862.2.3.el7.x86_64.rpm
```

reboot the system to make it start with the new kernel

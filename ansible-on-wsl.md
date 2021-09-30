---
description: Installation ansible on ubuntu wsl
---

# Ansible on WSL

### Install WSL \(Windows Subsystem for Linux\)

copy and paste in powershell

```text
dism.exe /online /enable-feature /featurename:Microsoft-Windows-Subsystem-Linux /all /norestart
dism.exe /online /enable-feature /featurename:VirtualMachinePlatform /all /norestart
```

Create script file and copy this and paste.

```text
sudo apt-add-repository ppa:ansible/ansible
sudo apt-get update
#sudo apt-get install ansible
sudo apt install python3-pip
sudo pip3 install pywinrm
sudo pip3 install pyvmomi
sudo pip3 install ansible
sudo pip3 install ansible[azure]
```


# Installation of kubectl in ubuntu

create script file in your system

```text
vi kubectl.sh
```

And copy the all of these to kubectl.sh

```text
sudo apt-get update && sudo apt-get install -y apt-transport-https gnupg2 curl
curl -s https://packages.cloud.google.com/apt/doc/apt-key.gpg | sudo apt-key add -
echo "deb https://apt.kubernetes.io/ kubernetes-xenial main" | sudo tee -a /etc/apt/sources.list.d/kubernetes.list
sudo apt-get update
sudo apt-get install -y kubectl
:wq!
chmod +x kubectl.sh
./kubectl.sh
```


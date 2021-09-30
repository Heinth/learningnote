# Installation terraform in ubuntu

 _Terraform_ is a tool for building, changing, and versioning infrastructure safely and efficiently called Iac \( Infrastructure as a code\).

Here is the topic for installation of the terraform in ubuntu operating system.

First step, we need to download the terraform from hashicorp 

```text
sudo wget https://releases.hashicorp.com/terraform/0.12.18/terraform_0.12.18_linux_amd64.zip
```

After that we have to unzip the downloaded terraform file.

```text
sudo unzip terraform_0.12.18_linux_amd64.zip
```

And we will remove terraform file to bin directory for executable.

```text
sudo mv terraform /usr/local/bin/
```

The terraform cli is successfully installed in our system and check its version

```text
terraform -v 
(or)
terraform --version
```


# Awscli configure in ubuntu \(Linux\)

First of all, we need to create new user in AWS IAM and also give new user to Administrator permission. After that we need enter the Security Credentials and create new access key.

Then we have Access key ID and Password for new user

After that we need to install aws materials in ubuntu

```text
sudo apt-get install python2-pip
sudo apt-get install python3-pip
sudo pip install awscli
sudo pip3 install awscli
```

After installed the awscli in ubuntu, we need to configure the aws new user.

```text
aws configure
```

When we typed this command, it'll ask the Access Key ID, Secret Access key , Default Region and output format. you can fill the first 2 from creating new access key in IAM and can use default region to currently region that you are in.

```text
#After that we can test our user configuration.
aws ec2 describe-instances
```


---
description: How to make .tar to docker image
---

# Change docker image to .tar file and load image

### Firstly we need to pull the image in out system or machine

### And then we will type this command to change image to .tar file

```
docker save -o /tmp/test.tar test:latest
docker load -i /tmp/test.tar
```

---
description: >-
  These are the basic command to use docker. Hope will get something about
  docker.
---

# Container \( Docker basic command\)

This command is used to get the currently installed version of docker

```text
docker --version
```

Used to pull images from the docker repository\(hub.docker.com\)

```text
docker pull <image_name or id>
```

This command is used to create a container from an image

```text
docker run -it -d <image name or id>
```

Check the list of the container in system

```text
docker ps
```

Check the list of the container in system including stopped container

```text
docker ps -a
```

This command is used to access the running container

```text
docker exec -it /bin/bash <container_name or id>
```

To stop the docker container

```text
docker stop <container_name or id)
```

Check the list of the container images in system

```text
docker images
```

This command is to delete the container \(ps. the container must to stop\)

```text
docker rm <container_name or id>
```

This command is used to delete an image from local storage.

```text
docker rmi <image-name or id>
```

This command is used to build an image from a specified docker file

```text
docker build -t <path to docker file>
```


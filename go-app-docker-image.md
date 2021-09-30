# Go App docker image

Here is the very basically structure of docker image for Go app.

```text
FROM golang:alpine
WORKDIR /go/src/app
ADD . .
RUN go mod init
RUN go build -o helloworld
EXPOSE 6111
CMD ["./helloworld"]
```

FROM - set the base image

WORKDIR - working directory of this app

ADD - copy current data files to container

RUN - execute the command

EXPOSE  - set for container port

CMD - to set the default command execute when the container start


FROM golang:1.8.1-alpine

ENV SOURCES /go/src/github.com/Zhanat87/cloud-native/advanced/Discovery/Kubernetes/server/
COPY . ${SOURCES}

RUN cd ${SOURCES} && CGO_ENABLED=0 go build

WORKDIR ${SOURCES}
CMD ${SOURCES}server

FROM golang:1.8-alpine
MAINTAINER Iskakov Zhanat <iskakov_zhanat@mail.ru>

RUN apk update && apk upgrade && apk add --no-cache bash git
RUN go get github.com/gin-gonic/gin

ENV SOURCES /go/src/github.com/Zhanat87/cloud-native/advanced/
COPY . ${SOURCES}

RUN cd ${SOURCES} && CGO_ENABLED=0 go build

WORKDIR ${SOURCES}

CMD ${SOURCES}advanced

ENV PORT 8080
EXPOSE 8080
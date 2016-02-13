FROM alpine:latest

MAINTAINER Bruno Henrique - Garu <squall.bruno@gmail.com> (@garucosta)

RUN apk --update add go

ENV GOPATH /go
ENV PATH $GOPATH/bin:/usr/local/lib/go/bin:$PATH

RUN mkdir -p "$GOPATH/src" "$GOPATH/bin" && chmod -R 777 "$GOPATH"
WORKDIR $GOPATH

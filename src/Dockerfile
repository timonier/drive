FROM alpine:3.1
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV DRIVE_VERSION v0.3.3

RUN set -x \
    && BUILD_DEPS="git go" \
    && apk add -U $BUILD_DEPS \
    && mkdir -p /go/src/github.com/odeke-em/drive \
    && git clone https://github.com/odeke-em/drive.git /go/src/github.com/odeke-em/drive \
    && git -C /go/src/github.com/odeke-em/drive checkout $DRIVE_VERSION \
    && CGO_ENABLED=0 GOPATH=/go go get github.com/odeke-em/drive/cmd/drive \
    && mv /go/bin/drive /usr/bin/drive \
    && apk del $BUILD_DEPS \
    && rm -rf /go /var/cache/apk/*

ENTRYPOINT [ "/usr/bin/drive" ]

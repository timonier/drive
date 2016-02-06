FROM alpine:3.1
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV \
    DRIVE_VERSION=0.3.3

RUN set -x \

    # Prepare system

    && apk add -U \

    # Install packages

    && BUILD_DEPS="git go" \
    && apk add \
           $BUILD_DEPS \

    # Compile drive

    && mkdir -p /go/src/github.com/odeke-em/drive \
    && git clone https://github.com/odeke-em/drive.git /go/src/github.com/odeke-em/drive \
    && git -C /go/src/github.com/odeke-em/drive checkout v$DRIVE_VERSION \
    && CGO_ENABLED=0 GOPATH=/go go get github.com/odeke-em/drive/cmd/drive \
    && mv /go/bin/drive /usr/bin/drive \

    # Clean

    && apk del \
           $BUILD_DEPS \
    && rm -rf \
           /go \
           /var/cache/apk/*

ENTRYPOINT [ "/usr/bin/drive" ]

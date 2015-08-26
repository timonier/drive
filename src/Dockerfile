FROM golang:1.3
MAINTAINER Morgan Auchede <morgan.auchede@gmail.com>

ENV DRIVE_VERSION v0.2.8

RUN set -x \
    && mkdir -p $GOPATH/src/github.com/odeke-em/drive \
    && git clone https://github.com/odeke-em/drive.git $GOPATH/src/github.com/odeke-em/drive \
    && git -C "$GOPATH/src/github.com/odeke-em/drive" checkout $DRIVE_VERSION \
    && go get github.com/odeke-em/drive/cmd/drive \
    && rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*

ENTRYPOINT [ "/go/bin/drive" ]

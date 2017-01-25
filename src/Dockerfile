FROM alpine:3.4

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

ENV \
    DRIVE_VERSION=0.3.8

RUN set -x \

    # Install packages

    && apk add --no-cache --no-progress --virtual build_deps \
           build-base \
           curl \
           git \
           go \

    && apk add --no-cache --no-progress \
          ca-certificates \

    # Install drive

    && export GOPATH=/tmp \
    && mkdir -p ${GOPATH}/src/github.com/odeke-em/drive \
    && git clone https://github.com/odeke-em/drive.git ${GOPATH}/src/github.com/odeke-em/drive \
    && git -C ${GOPATH}/src/github.com/odeke-em/drive checkout v${DRIVE_VERSION} \
    && go get -v github.com/odeke-em/drive/cmd/drive \
    && mv ${GOPATH}/bin/drive /usr/bin/drive \

    # Install timonier/dumb-entrypoint

    && curl -sL "https://github.com/timonier/dumb-entrypoint/raw/master/bin/installer" | INSTALL_DIRECTORY="/usr/sbin" sh -s install \

    # Clean

    && apk del --no-progress \
           build_deps \

    && rm -rf \
           /tmp/*

ENTRYPOINT [ "dumb-init" , "--" , "dumb-entrypoint" ]

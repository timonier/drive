FROM golang:alpine as drive

RUN set -e -u -x \
\
    # Install packages
\
    && apk add --no-cache --no-progress build-base git \
\
    # Install drive
\
    && go get -u github.com/odeke-em/drive/drive-gen \
    && drive-gen

# ---

FROM alpine:latest

LABEL \
    maintainer="Morgan Auchede <morgan.auchede@gmail.com>"

RUN set -e -u -x \
\
    # Install packages
\
    && apk add --no-cache --no-progress --virtual BUILD_DEPS curl \
    && apk add --no-cache --no-progress bash ca-certificates \
\
    # Install dumb-entrypoint
\
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/dumb-entrypoint/installer" | sh -s -- install \
    && curl --location "https://github.com/timonier/dumb-entrypoint/raw/master/src/gosu/installer" | sh -s -- install \
\
    # Clean
\
    && apk del --no-progress BUILD_DEPS \
    && rm -f -r /tmp/*

COPY --from=drive /go/bin/drive /usr/local/bin/drive

ENTRYPOINT [ "dumb-entrypoint" ]

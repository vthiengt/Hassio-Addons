ARG BUILD_FROM
FROM $BUILD_FROM

RUN arch=$(uname -m); if [ "$arch" = "aarch64" ]; then export VERSION='1.5.0-r0'; else export VERSION='1.10.0-r1'; fi && \
	apk add --no-cache --repository=http://dl-cdn.alpinelinux.org/alpine/edge/community \
		"syncthing=$VERSION"

COPY root /

# Ver: 1.2 by Endial Fang (endial@126.com)
#

# 镜像生成 ========================================================================
FROM colovu/openjre:1.8-alpine
ARG apt_source=default
ARG local_url=""

ENV APP_NAME=ffmpeg \
	APP_VERSION=4.3.1

LABEL \
	"Version"="v${APP_VERSION}" \
	"Description"="Docker image for ${APP_NAME} v${APP_VERSION}." \
	"Dockerfile"="https://github.com/colovu/docker-${APP_NAME}-java" \
	"Vendor"="Endial Fang (endial@126.com)"

RUN select_source ${apt_source}
RUN install_pkg ffmpeg

RUN set -eux; \
	\
# 验证安装的软件是否可以正常运行，常规情况下放置在命令行的最后
	${APP_NAME} -version;

WORKDIR /

CMD []
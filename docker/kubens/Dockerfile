FROM alpine:3.19

RUN apk add --no-cache kubectl ncurses

ARG VERSION=v0.9.4
ARG PACK_NAME=kubens_${VERSION}_linux_x86_64.tar.gz

RUN wget https://github.com/ahmetb/kubectx/releases/download/${VERSION}/${PACK_NAME}
RUN tar -xvzf ${PACK_NAME} && rm ${PACK_NAME}
RUN mv kubens /usr/local/bin/

ENTRYPOINT ["/usr/local/bin/kubens"]

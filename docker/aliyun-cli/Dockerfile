FROM alpine:3.19

RUN apk add --no-cache jq nodejs npm

RUN wget https://aliyuncli.alicdn.com/aliyun-cli-linux-latest-amd64.tgz
RUN tar -xvzf aliyun-cli-linux-latest-amd64.tgz
RUN rm aliyun-cli-linux-latest-amd64.tgz
RUN mv aliyun /usr/local/bin/
RUN npm i @alicloud/sso-cli -g

RUN mkdir /lib64 && ln -s /lib/libc.musl-x86_64.so.1 /lib64/ld-linux-x86-64.so.2
RUN mkdir /root/.aliyun && \
    ln -s /root/.aliyun/alibabacloud_sso /root/.alibabacloud_sso && \
    ln -s /root/.aliyun/alibabacloud_sso_sts /root/.alibabacloud_sso_sts

ENTRYPOINT ["/usr/local/bin/aliyun"]
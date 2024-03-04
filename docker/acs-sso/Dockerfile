FROM alpine:3.19

RUN apk add --no-cache nodejs npm
RUN npm i @alicloud/sso-cli -g

RUN mkdir /root/.aliyun && \
    ln -s /root/.aliyun/alibabacloud_sso /root/.alibabacloud_sso && \
    ln -s /root/.aliyun/alibabacloud_sso_sts /root/.alibabacloud_sso_sts

ENTRYPOINT ["/usr/local/bin/acs-sso"]
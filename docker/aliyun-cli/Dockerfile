FROM alpine:3.19

# 添加 jq，以 JSON 的格式输出
RUN apk add --no-cache jq

# 获取并安装阿里云 CLI 工具
RUN wget https://aliyuncli.alicdn.com/aliyun-cli-linux-latest-amd64.tgz
RUN tar -xvzf aliyun-cli-linux-latest-amd64.tgz
RUN rm aliyun-cli-linux-latest-amd64.tgz
RUN mv aliyun /usr/local/bin/

# 注意：alpine需要额外创建 lib64 的动态链接库软连接
RUN mkdir /lib64 && ln -s /lib/libc.musl-x86_64.so.1 /lib64/ld-linux-x86-64.so.2

ENTRYPOINT ["/usr/local/bin/aliyun"]
FROM rabbitmq:3.8.10-management-alpine

RUN apk update && apk add ca-certificates && \
    apk add tzdata && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone && \
    cd /opt/rabbitmq/plugins/ && \
    wget https://github.com/rabbitmq/rabbitmq-autocluster/releases/download/0.10.0/autocluster-0.10.0.ez && \
    ls -al /opt/rabbitmq/plugins/ && \
    rabbitmq-plugins list && \
    rabbitmq-plugins enable autocluster --offline
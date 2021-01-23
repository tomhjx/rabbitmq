FROM rabbitmq:3.8.10-management-alpine

RUN apk update && apk add ca-certificates && \
    apk add tzdata && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone && \
    rabbitmq-plugins list && \
    cd /opt/rabbitmq/plugins/ && \
    ls -al /opt/rabbitmq/plugins/ && \
    wget https://github.com/rabbitmq/rabbitmq-autocluster/releases/download/0.10.0/autocluster-0.10.0.ez && \
    wget https://github.com/rabbitmq/rabbitmq-autocluster/releases/download/0.10.0/rabbitmq_aws-0.10.0.ez && \
    rabbitmq-plugins list && \
    ls -al /opt/rabbitmq/plugins/ && \
    rabbitmq-plugins enable autocluster --offline
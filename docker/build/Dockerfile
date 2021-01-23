FROM rabbitmq:3.8.10-management-alpine

RUN apk update && apk add ca-certificates && \
    apk add tzdata && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone && \
    mkdir -p /tmp/plugins && \
    cd /tmp/plugins && \
    wget https://github.com/rabbitmq/rabbitmq-autocluster/releases/download/0.10.0/autocluster-0.10.0.ez && \
    wget https://github.com/rabbitmq/rabbitmq-autocluster/releases/download/0.10.0/rabbitmq_aws-0.10.0.ez && \
    chmod 777 ./*.ez && \
    cp -rf ./*.ez /opt/rabbitmq/plugins/ && \ 
    ls -al /opt/rabbitmq/plugins/ && \
    rabbitmq-plugins list && \
    rabbitmq-plugins enable autocluster --offline
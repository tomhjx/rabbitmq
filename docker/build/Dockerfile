FROM rabbitmq:3.8.14-management-alpine

RUN apk update && apk add ca-certificates && \
    apk add tzdata && \
    ln -sf /usr/share/zoneinfo/Asia/Shanghai /etc/localtime && \
    echo "Asia/Shanghai" > /etc/timezone && \
    rabbitmq-plugins list && \
    cd /opt/rabbitmq/plugins/ && \
    ls -al /opt/rabbitmq/plugins/ && \
    wget https://github.com/rabbitmq/rabbitmq-delayed-message-exchange/releases/download/3.8.9/rabbitmq_delayed_message_exchange-3.8.9-0199d11c.ez && \
    rabbitmq-plugins enable rabbitmq_delayed_message_exchange
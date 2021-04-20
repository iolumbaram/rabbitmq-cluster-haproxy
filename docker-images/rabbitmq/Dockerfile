FROM rabbitmq:3.8-management
RUN rabbitmq-plugins enable --offline rabbitmq_mqtt rabbitmq_federation_management rabbitmq_stomp rabbitmq_management

COPY ./rabbitmq.conf /etc/rabbitmq/rabbitmq.conf

EXPOSE 5671 5672 15671 15672 25672 4369 9100 9101 9102 9103 9104 9105
CMD ["rabbitmq-server"]
FROM rabbitmq:3.5.3-management

COPY rabbitmq-cluster /usr/local/bin/
COPY pre-entrypoint.sh /

EXPOSE 5672 15672 25672 4369 9100 9101 9102 9103 9104 9105
RUN ["chmod", "+x", "/pre-entrypoint.sh"]
RUN ["chmod", "+x", "/usr/local/bin/rabbitmq-cluster"]
ENTRYPOINT ["/pre-entrypoint.sh"]
CMD ["rabbitmq-cluster"]

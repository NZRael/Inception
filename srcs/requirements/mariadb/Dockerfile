FROM debian:bullseye
RUN apt-get update -y && apt-get install -y
RUN apt-get install -y mariadb-server mariadb-client
COPY ./conf/my.cnf /etc/mysql/my.cnf
COPY ./tools/script.sh /tmp/script.sh
RUN chmod +x /tmp/script.sh
EXPOSE 3306
CMD ["/tmp/script.sh"]
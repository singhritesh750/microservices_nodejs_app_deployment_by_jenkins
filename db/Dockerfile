FROM mysql
ENV MYSQL_DATABASE employees_db
ENV MYSQL_ALLOW_EMPTY_PASSWORD=1
COPY ./testdump.sql /docker-entrypoint-initdb.d/
EXPOSE 3306


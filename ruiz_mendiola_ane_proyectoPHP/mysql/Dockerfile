FROM mysql:5.7

# Copiamos los scripts .sql al directorio /docker-entrypoint-initdb.d
# Se ejecutan al arrancar el contenedor en orden alfabético en la BBDD indicada en MYSQL_DATABASE
# Cuidado con las mayúsculas y las minúsculas
COPY crearBBDD.sql insertarDatos.sql /docker-entrypoint-initdb.d/

RUN echo [mysqld] >> /etc/mysql/my.cnf
RUN echo "innodb_use_native_aio=0" >> /etc/mysql/my.cnf

EXPOSE 3306
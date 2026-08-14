# go-mysql

Para poder usar Mysql con go para fines practicos y con el fin de poder entender como funciona las consultas sql dentro de go usaremos Go-MySQL-Driver, por motivos de seguridad y de simplesa a la hora de escribir codigo
se recomienda usar algun tipo de orm que nos permita escribir consultas en lenguaje nativo 

[Go-MySQL-Driver](https://github.com/go-sql-driver/MYSQL)

**por motivos de seguridad es obligatorio el uso de varibles de entorno independientemente del lenguaje**, se usa para guardad las claves a bases de datos, apy-key y todo lo que sea una llave de acceso o parecido

para correr la base de datos use Xamp dentro de un contenedor de docker **No se recomienda usar xamp en un contenedor de docker en produccion, por que puede llegar a generar problemas de escalavilidad y de actulizacion**
en este caso se usa con fines practicos 


##docker compose

```docker 
services:
  # Servidor Web Apache + PHP
  web:
    image: php:8.3-apache
    container_name: entorno_web
    ports:
      - "8080:80"
    volumes:
      - ./src:/var/www/html

  # Base de Datos MariaDB
  db:
    image: mariadb:latest
    container_name: entorno_db
    environment:
      MYSQL_ROOT_PASSWORD: root
      MYSQL_DATABASE: prueba_db
    volumes:
      - datos_db:/var/lib/mysql

  # Interfaz gráfica phpMyAdmin
  phpmyadmin:
    image: phpmyadmin:latest
    container_name: entorno_pma
    ports:
      - "8081:80"
    environment:
      PMA_HOST: db

volumes:
  datos_db:
```



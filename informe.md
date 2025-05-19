# Informe YML

## 2. Tiempo de duración
**Tiempo estimado: 90 minutos**

## 3. Fundamentos

### ¿Qué es WordPress?
WordPress es un sistema de gestión de contenidos (CMS) de código abierto que permite crear y administrar sitios web fácilmente. Se integra con bases de datos para guardar contenido, usuarios, configuraciones y más.

### ¿Qué es PostgreSQL?
PostgreSQL es un sistema de gestión de bases de datos relacional, robusto y de código abierto. Es muy usado por su estabilidad y capacidad para manejar grandes volúmenes de datos.

### ¿Qué es pgAdmin?
pgAdmin es una herramienta visual para administrar bases de datos PostgreSQL desde el navegador, permitiendo crear, editar y consultar estructuras y datos sin necesidad de usar comandos.

### ¿Qué es una red personalizada en Docker?
Permite que varios contenedores se comuniquen entre sí utilizando nombres amigables, mejorando la seguridad y organización del entorno.

### ¿Qué es un volumen en Docker?
Un volumen es una carpeta que guarda datos de manera persistente, incluso si el contenedor es borrado o reiniciado.

## 4. Conocimientos previos
- Comandos básicos de Docker: `docker run`, `docker volume`, `docker network`.
- Conceptos básicos de base de datos.
- Acceso a navegador y terminal.
- Manejo de estructura YML en Docker Compose.

## 5. Objetivos a alcanzar
- Crear una red personalizada para interconectar los contenedores.
- Crear volúmenes persistentes para PostgreSQL y WordPress.
- Levantar los contenedores necesarios mediante Docker Compose.
- Conectarse a pgAdmin y registrar el servidor PostgreSQL.
- Acceder a WordPress desde el navegador.

## 6. Equipo necesario
- PC con Docker instalado.
- Conexión a internet.
- Navegador actualizado.
- Editor de texto (como VS Code o Nano).

## 7. Material de apoyo
- [Docker Documentation](https://docs.docker.com)
- [Bitnami WordPress](https://hub.docker.com/r/bitnami/wordpress)
- [pgAdmin Docs](https://www.pgadmin.org/docs/)
- [PostgreSQL Manual](https://www.postgresql.org/docs/)

## 8. Procedimiento

### 1. Crear archivo docker-compose.yml

Se estructuraron 3 servicios: `wordpress_wp`, `postgres_wp`, `pgadmin_wp`. 
Se definieron variables de entorno, puertos, red personalizada y volúmenes persistentes.

### 2. Crear red y volúmenes

Docker Compose crea automáticamente la red `red_wp` y los volúmenes definidos al ejecutar el comando:

docker-compose up -d
![img01](https://github.com/Edissonfierro/yml/blob/main/1.jpg)

![img01](https://github.com/Edissonfierro/yml/blob/main/2.jpg)

![img01](https://github.com/Edissonfierro/yml/blob/main/3.jpg)

![img01](https://github.com/Edissonfierro/yml/blob/main/4.jpg)


## 9. Resultados esperados

- WordPress accesible en el navegador.
- Acceso exitoso a pgAdmin.
- Conexión establecida entre WordPress y PostgreSQL.
- Servidor registrado en pgAdmin.
- Tabla creada correctamente y datos insertados.
- Contenedores en estado “Up” usando `docker ps`.

## 10. Bibliografía

- Docker. (n.d.). *Docker networking overview*. https://docs.docker.com/network/
- pgAdmin. (n.d.). *pgAdmin documentation*. https://www.pgadmin.org/docs/
- PostgreSQL. (n.d.). *PostgreSQL documentation*. https://www.postgresql.org/docs/
- WordPress. (n.d.). *WordPress support*. https://wordpress.org/support/

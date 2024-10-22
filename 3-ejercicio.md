### Crear contenedor de Postgres sin que exponga los puertos. Usar la imagen: postgres:11.21-alpine3.17
# COMPLETAR
docker run -d --name postgresContainer --env-file=varPostgres.env postgres:11.21-alpine3.17

![Imagen](img/varPostgres.PNG)


### Crear un cliente de postgres. Usar la imagen: dpage/pgadmin4

# COMPLETAR

docker run -d -p 8080:80 --name pgadminContainer --env-file=postgresAdmin.env dpage/pgadmin4

![Imagen](img/postgresAdmin.PNG)


La figura presenta el esquema creado en donde los puertos son:
- a: (completar con el valor)
- b: (completar con el valor)
- c: (completar con el valor)

![Imagen](img/esquema-ejercicio3.PNG)

## Desde el cliente
### Acceder desde el cliente al servidor postgres creado.
# COMPLETAR CON UNA CAPTURA DEL LOGIN

![Imagen](img/loginpgadmin.PNG)
### Crear la base de datos info, y dentro de esa base la tabla personas, con id (serial) y nombre (varchar), agregar un par de registros en la tabla, obligatorio incluir su nombre.


docker exec -it postgres psql -U postgres -d postgres

![Imagen](img/datosDB.PNG)

## Desde el servidor postgresl
### Acceder al servidor
### Conectarse a la base de datos info
# COMPLETAR

docker exec -it postgres /bin/bash

psql -h 172.17.0.2 -p 5432 -U postgres -d info
### Realizar un select *from personas
# AGREGAR UNA CAPTURA DE PANTALLA DEL RESULTADO

![Imagen](img/postgres.PNG)


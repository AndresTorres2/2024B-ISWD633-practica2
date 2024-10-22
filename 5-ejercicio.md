## Esquema para el ejercicio
![Imagen](img/esquema-ejercicio5.PNG)

### Crear la red
# COMPLETAR

docker network create net-wp


### Crear el contenedor mysql a partir de la imagen mysql:8, configurar las variables de entorno necesarias
# COMPLETAR

docker run -P -d --name mysql --env-file=variableEntorno.env --network net-wp mysql:8

### Crear el contenedor wordpress a partir de la imagen: wordpress, configurar las variables de entorno necesarias
# COMPLETAR

docker run -d --name wordpress -p 7500:80 --network net-wp wordpress

De acuerdo con el trabajo realizado, en la el esquema de ejercicio el puerto a es 7500

Ingresar desde el navegador al wordpress y finalizar la configuración de instalación.
# COLOCAR UNA CAPTURA DE LA CONFIGURACIÓN

![Imagen](img/configuracion.PNG)


Desde el panel de admin: cambiar el tema y crear una nueva publicación.
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
# COLOCAR UNA CAPTURA DEL SITO EN DONDE SEA VISIBLE LA PUBLICACIÓN.

![Imagen](img/wordpress.PNG)

![Imagen](img/tema.PNG)

![Imagen](img/pagina.PNG)

### Eliminar el contenedor wordpress
# COMPLETAR

docker rm wordpress

### Crear nuevamente el contenedor wordpress
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress

### ¿Qué ha sucedido, qué puede observar?
# COMPLETAR

Que al borrar el wordpress, tocaria volver a configurar todo desde 0






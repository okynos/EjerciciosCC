# Ejercicio 6 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Reproducir los contenedores creados anteriormente usando un Dockerfile.

Para realizar este ejercicio es necesario crear un fichero llamado "Dockerfile" sin comillas en algún directorio de nuestra preferencia y rellenarlo con el contenido que necesitemos en cada caso, en el nuestro particular nuestro Dockerfile es el siguiente:

```
FROM alpine
MAINTAINER Okynos <pylott@gmail.com>
WORKDIR /root
CMD ["/bin/ash"]

RUN apk update && apk upgrade
RUN apk add git
RUN apk add curl
RUN apk add python
```

Después de generar nuestro Dockerfile podemos construir el contenedor asociado y iniciarlo con los comandos:
```
sudo docker build -t okynos/alpine .
sudo docker run -it okynos/alpine
```

Finalmente si todo ha funcionado correctamente entrará en la terminal del contenedor por si queremos realizar alguna acción con el mismo y ya hemos desplegado un contenedor con el Dockerfile que hemos escrito de manera totalmente automática.

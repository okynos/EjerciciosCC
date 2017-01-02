# Ejercicio 4 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Instalar una imagen alternativa de Ubuntu y alguna adicional, por ejemplo de CentOS.

Para instalar una imagen alternativa de ubuntu que ya hemos buscado en el repositorio de imágenes solo es necesario descargarla con el siguiente comando:
```
sudo docker pull rastasheep/ubuntu-sshd
```
Esta distribución es un Ubuntu base con acceso ssh.

Para instalar otra distro pero esta vez basada en CentOS tras buscarla de nuevo en la [página de Docker](https://hub.docker.com) se puede descargar de la siguiente manera:
```
sudo docker pull nimmis/java-centos
```
En este caso es una distribución de centOS mínima con las dependencias de java ya instaladas y configuradas.

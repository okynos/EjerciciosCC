# Ejercicio 5 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Crear a partir del contenedor anterior una imagen persistente con commit.

Para este ejercicio es necesario tener instalado Docker que con este simple comando se instalará una version más o menos reciente de manera muy fácil:
```
sudo apt-get install docker.io
```

Una vez se ha instalado Docker podemos empezar a descargar y crear contenedores para almacenar en ellos los servicios que se necesiten en nuestro caso vamos a instalar Alpine dado que es muy liviana y ocupa poco espacio en disco:
```
sudo docker pull alpine
```
Si quisieramos eliminar una imagen que no necesitemos con:
```
sudo docker rmi alpine
```
Es posible eliminarla del sistema y liberar ese espacio.

Una vez la imagen se ha descargado debemos actualizarla y ponerla a punto para nuestras necesidades, en el caso de alpine se puede realizar de la siguiente manera:
```
sudo docker run -it alpine sh
```
Arrancamos el contenedor y ejecutamos dentro de el un terminal shell interactivo una vez está todo listo dentro de ese terminal podemos ejecutar:
```
apk update
apk upgrade
```
Para actualizar nuestra distribución y dejarlo todo preparado.
Ahora podemos provisionarla de manera manual instalando por ejemplo python:
```
apk add python
```
Ya tendríamos nuestro contenedor preparado para guardarse para ello cojemos el ID del contenedor que lo podemos obtener ejecutando la siguiente orden:
```
sudo docker ps -a
```
Lo arrancamos si estaba parado con el comando:
```
sudo docker start CID
```
Donde CID es el string que nos ha dado al ejecutar la orden anterior, y luego la guardamos con:
```
sudo docker commit CID
```

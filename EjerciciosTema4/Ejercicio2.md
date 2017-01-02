# Ejercicio 2 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Crear una instancia de una máquina virtual Debian y provisionarla usando alguna de las aplicaciones vistas en el tema sobre herramientas de aprovisionamiento

Para este ejercicio vamos a utilizar openStack para crear las máquinas que se necesiten, en nuestro caso vamos a crear una imagen de Debian a través del interfaz web de OpenStack.
Una vez creada la imagen y asignada una IP a la misma podemos provisionarla de manera sencilla con Rex, pero antes debemos modificar el fichero Rexfile para añadir la IP del servidor que vamos a provisionar y le usuario además de la clave privada igual que en ansible una vez este fichero está configurado podemos provisionar la máquina ejecutando el siguiente comando de Rex:
```
rex deployServers
```

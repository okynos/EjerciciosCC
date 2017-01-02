# Ejercicio 1 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Instala LXC en tu versión de Linux favorita. Normalmente la versión en desarrollo, disponible tanto en GitHub como en el sitio web está bastante más avanzada; para evitar problemas sobre todo con las herramientas que vamos a ver más adelante, conviene que te instales la última versión y si es posible una igual o mayor a la 2.0.

Para instalar lxc en nuestra distribución(En este caso Ubuntu 16.04) se puede realizar de dos formas:
* Instalando desde el repositorio oficial de Ubuntu, en este caso solo es necesario ejecutar la siguiente orden en la terminal:
```
sudo apt-get install lxc
```
Y nos instalará lxc en su versión 2.0.6

* Si deseamos utilizar una versión más actual podemos descargar la última desde su [rama](https://launchpad.net/~ubuntu-lxc/+archive/ubuntu/lxc-git-master) añadiendo un repositorio ppa del cual poder instalar hasta la versión la cual en estos momentos es la misma que en los repositorios de Ubuntu la 2.0.6.

Una vez realizados estos pasos es posible utilizar los comandos comunes de lxc.

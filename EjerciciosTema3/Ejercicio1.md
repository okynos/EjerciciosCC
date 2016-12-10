# Ejercicio 1 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Instalar una máquina virtual Debian usando Vagrant y conectar con ella.

Para realizar este ejercicio se han seguido una serie de pasos que vamos a detallar a continuación:

1. Se instala vagrant descargando la última versión disponible en la [página de vagrant](https://www.vagrantup.com/downloads.html)
Se puede instalar vagrant en debian o ubuntu simplemente ejecutando la orden
```
sudo dpkg -i paquete.deb
```

2. Si necesitas instalar alguna libreria o dependencia (en mi caso era necesario instalar la libreria libqt5x11extras5)
con este comando se instala
```
 sudo apt-get install libqt5x11extras5
```
Podeis sustituir esa dependencia por cualquier otra.

3. Nos vamos a la página [Vagrant boxes](http://www.vagrantbox.es/) y buscamos una distribución que nos interese, mínimo que tenga guest additions en mi caso he escogido esta [Debian-Jessie](https://atlas.hashicorp.com/ARTACK/boxes/debian-jessie) la añadimos a vagrant con el comando:
```
vagrant box add https://atlas.hashicorp.com/ARTACK/boxes/debian-jessie
```

4. Tras esperar a que se descargue la imagen del servidor, nos dirigimos a una carpeta preferiblemente vacía en la que crearemos nuestros archivos de vagrant para orquestar y ejecutamos la siguiente orden:
```
vagrant init ARTACK/debian-jessie
```
Este es el nombre de mi caja pero se debe cambiar al que tenga cada uno, nos creará el archivo vagrantfile que especifica la configuración de la máquina.

5. Si hemos hecho todo bien con la orden
```
vagrant up
```
Comenzará a crear, configurar y provisionar la máquina que hemos descargado bajo el entorno virtualbox que deberemos tener instalado si no es así se puede instalar desde la página o con el comando
```
sudo apt-get install virtualbox
```

6. Una vez se ha iniciado la máquina nos podemos conectar a ella a través del siguiente comando para acceder por ssh
```
vagrant ssh
```

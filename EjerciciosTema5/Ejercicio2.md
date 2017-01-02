# Ejercicio 2 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Instalar una distro tal como Alpine y conectarse a ella usando el nombre de usuario y clave que indicará en su creación

Para realizar este ejercicio es necesario tener instalado en nuestra distribución lxc, tras ello es posible crear un contenedor con alpine dentro con la siguiente orden:
```
sudo lxc-create -t alpine -n alpineDock
```

Esto pondrá a punto el contenedor pero no lo iniciará, para ello necesitamos ejecutar el siguiente comando:
```
sudo lxc-start -n alpineDock
```

Si no hemos tenido ningún error iniciando la máquina y si nos ha dado un usuario y clave nos logueamos por ssh de manera normal, en caso contrario podemos como nos indica el propio lxc acceder con el siguiente comando:
```
sudo lxc-attach -n alpineDock
```

Si por el contrario se ha presentado un error de appArmor edita el fichero que se encuentra en /var/lib/lxc/alpineDock/config y añádele la siguiente línea:
```
lxc.aa_allow_incomplete = 1
```

con esto ya estará nuestro contenedor iniciado y nos podremos conectar correctamente.

# Ejercicio 2 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Instalar una máquina virtual ArchLinux o FreeBSD para KVM, otro hipervisor libre, usando Vagrant y conectar con ella. 

Para realizar este ejercicio es necesario descargar una caja desde la página de vagrant box en mi caso he escogido una distribución con kvm de centos6 dado que la de arch daba algunos problemas.

Descargamos la imagen con el siguiente comando:
```
vagrant box add viniciusfs/centos6 https://atlas.hashicorp.com/viniciusfs/boxes/centos6/
```

Seguidamente nos vamos a un directorio limpio y ejecutamos las ordenes
```
vagrant init viniciusfs/centos6
sudo vagrant up --provider=libvirt
```

Esperamos a que se inicie la máquina virtual y si toda la configuración es correcta ya tendremos iniciada nuestra máquina virtual.

Finalmente nos conectamos con la máquina instanciada con el comando:
```
sudo vagrant ssh
```


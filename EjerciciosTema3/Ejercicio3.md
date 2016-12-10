# Ejercicio 3 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Crear un script para provisionar `nginx` o cualquier otro servidor web que pueda ser útil para alguna otra práctica


Para provisionar una máquina lanzada con vagrant la manera más simple es modificando el fichero vagrantfile que se ha creado al hacer vagrant init y dejamos el archivo para provisionar la máquina como este:

```
Vagrant.configure("2") do |config|
  config.vm.box = "viniciusfs/centos6"

  config.vm.provision "shell", inline: "yum install -y nginx nodejs"

end
```

Si la máquina virtual esta en marcha podemos provisionarla ejecutando:

```
vagrant provision
```

Al final del provisionamiento obtendremos un mensaje que nos indica si se ha completado la ejecución con éxito.

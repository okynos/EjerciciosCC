# Ejercicio 4 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Configurar tu máquina virtual usando `vagrant` con el provisionador ansible


Para provisionar la máquina que hemos lanzado con vagrant (Centos6) es necesario que tengamos instalado en nuestra máquina anfitrión el provisionador ansible el cual nos va a instalar todos los archivos y la configuración necesaria vamos a utilizar el script realizado en el hito anterior para provisionar con ansible:


```
---
- hosts: stack
  become: yes
  remote_user: ubuntu
  tasks:
  - name: Update repo
    apt: 
      update_cache: yes
  - name: Install MongoDB Server
    apt: pkg=mongodb-server state=installed
  - name: Install Mysql Server
    apt: pkg=mysql-server state=installed
  - name: Install RabbitMQ Server
    apt: pkg=rabbitmq-server state=installed

```

antes de ejecutar este script es necesario editar el fichero ansible_host si lo teniamos definido solo es necesario modificar el comando ansible añadiendole la ip de la máquina a provisionar

Finalmente ejecutamos la orden siguiente para provisionar la máquina
```
ansible-playbook scriptAnsible.yml
```

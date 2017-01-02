# Ejercicio 3 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Provisionar un contenedor LXC usando Ansible o alguna otra herramienta de configuración que ya se haya usado

En este caso vamos a provisionar nuestro contenedor ubuntuDock con Ansible para probar el provisionamiento desde alguna herramienta externa de provisionamiento, para llevar a cabo el provisionamiento solo es necesario modificar el script de Ansible indicandole los parámetros del contenedor que hemos creado, nuestro script podría quedar así:

```
---
- hosts: stack
  become: yes
  remote_user: ubuntu
  tasks:
  - name: Update repo
    apt: 
      update_cache: yes
  - name: Install RabbitMQ Server
    apt: pkg=rabbitmq-server state=installed
```
Como en este caso los contenedores se provisionan con pocos servicios hemos añadido únicamente RabbitMQ.
A continuación hay que modificar el fichero de hosts para añadirle si no lo tuvieramos el grupo que hemos definido en el script "stack" y definir las direcciones que tiene que provisionar en nuestro caso al provisionar solo un contenedor puede quedar así:
```
[stack]
10.0.3.115
```
Y lo exportamos con el comando:
```
export ANSIBLE_HOSTS=`pwd`/ansible_hosts
```

Para finalizar ejecutamos la llamada al script de Ansible con el siguiente comando:
```
ansible-playbook scriptRabbit.yml --ask-pass --ask-sudo-pass
```
En este caso hemos añadido las opciones --ask-pass para conectarnos por ssh sin fichero de clave y --ask-sudo-pass para especificarle la clave para acceder como superusuario, si en el contenedor añadimos un par de claves o una clave secreta es posible hacerlo sin escribir a contraseña cada vez.

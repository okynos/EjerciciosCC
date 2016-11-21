# Ejercicio 6 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Desplegar la aplicación que se haya usado anteriormente con todos los módulos necesarios usando un playbook de Ansible.

Se han realizado un par de playbooks para realizar el provisonamiento de varios microservicios por separado, son los siguientes:

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

y el siguiente:

```
---
- hosts: stack
  become: yes
  remote_user: ubuntu
  tasks:
  - name: Install NodeJS
    apt: pkg=nodejs state=installed
  - name: Install NodeJS dev
    apt: pkg=nodejs-dev state=installed
  - name: Install Npm utilities
    apt: pkg=npm state=installed
  
  - name: Install Socket.io dependency
    npm: name=socket.io global=yes path=~/nodejs/socket.io 

  - name: Install Express dependency
    npm: name=express global=yes path=~/nodejs/express
```

ambos ficheros se pueden ejecutar ejecutando el siguiente comando:

```
ansible-playbook scriptAnsible.yml --private-key keypair.pem
```

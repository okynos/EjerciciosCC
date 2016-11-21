# Ejercicio 5 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Desplegar los fuentes de una aplicación cualquiera, propia o libre, que se encuentre en un servidor git público en la máquina virtual Azure (o una máquina virtual local) usando ansible.

Para realizar un provisionamiento en Ansible es necesario realizar los siguientes pasos:

1. Instalamos ansible y sus dependencias con:
```
sudo pip install paramiko PyYAML jinja2 httplib2 ansible
```

2. Tras esto podemos crear un fichero para almacenar los hosts de ansible en nuestro caso hemos utilizado el siguiente código:
```
[stack]
XXX.XXX.XXX.XXX
```
Donde las X delimita la dirección IP del host.
Para finalizar con la configuración exportamos la variable de Ansible.

```
export ANSIBLE_HOSTS=~/ansible/ansible_hosts
```

Se prueba la conexión de ansible con:
```
ansible stack -m ping -u ubuntu -i keypair.pem
```

Si por casualidad da algún error probad a instalar python y sus dependencias a través de ssh.

Para finalizar descargamos los fuentes a desplegar y los ejecutamos con los comandos siguientes:
```
ansible stack -m git -a "repo=https://github.com/okynos/ProyectoCC.git dest=~/okynos/proyectoCC version=HEAD" -i keypair.pem

ansible stack -m command -a "sudo python proyecto/main.py" --ask-sudo-pass
```

Y comprobamos que funciona correctamente intentando conectar con el servidor.

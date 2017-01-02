# Ejercicio 1 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Crear una máquina virtual Ubuntu e instalar en ella un servidor nginx para poder acceder mediante web.

Para este ejercicio vamos a utilizar openStack para crear las máquinas que se necesiten, en nuestro caso vamos a crear una imagen de ubuntu a través del interfaz web de OpenStack.
Una vez creada la imagen y asignada una IP a la misma podemos provisionarla de manera sencilla con ansible añadiendo la IP al grupo que administramos y con el comando siguiente provisionarla:
```
ansible-playbook scriptAnsible.yml --private-key keypair.pem
```

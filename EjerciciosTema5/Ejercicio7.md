# Ejercicio 7 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Crear con docker-machine un entorno local y ejecutar en él contenedores creados con antelación.

Para este ejercicio es necesario tener instalado virtualbox y docker machine para ello podemos ejecutar el comando:
```
sudo apt-get install docker.io virtualbox-5.1
```
Con esto se nos instalarían los componentes necesarios para empezar a trabajar.
Tras ello comenzamos creando una máquina docker con el comando:
```
sudo docker-machine create --driver=virtualbox dockerMachine
```
Se nos creará una máquina virtual que podremos acceder y modificar con el sigiente comando:
```
sudo docker-machine ssh dockerMachine
```

Una vez la máquina entra en funcionamiento la podemos administrar remotamente estableciendo el siguiente comando con sus parámetros en la shell, este comando se debe ejecutar en cada shell que se abra:
```
eval $(sudo docker-machine env dockerMachine)
```

Ya podemos desplegar máquinas ya creadas anteriormente con el comando general de docker y añadiendole -E:
```
sudo -E docker pull okynos/alpine
```

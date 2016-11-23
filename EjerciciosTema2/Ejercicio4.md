# Ejercicio 4 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Provisionar una máquina virtual en algún entorno con los que trabajemos habitualmente usando Salt.

Para este ejercicio dado que Salt no se ha provisionado en el hito 2 realizaremos un provisionamiento con el lengauaje Rex, en nuestro caso provisionamos las máquinas que se encuentran en trystack creadas por nosotros.

En nuestro caso para instalar Rex solo es necesario instalar el paquete llamado rex desde línea de comandos en Ubuntu, en otros casos será necesario ejecutar la siguiente orden:

```
curl -L https://get.rexify.org | perl - --sudo -n Rex
```

Esto descargará e instalará Rex en nuestro equipo, una vez hecho esto ya podemos empezar a escribir un script de provisionamiento.

Rex utiliza un lenguaje descriptivo al igual que otras aplicaciones el script de provisionamiento que nosotros hemos creado es el siguiente:

```
use Rex -feature => ['1.3'];

user "ubuntu";
private_key "/home/okynos/keys/keypair.pem";
sudo -on;

group stack => "8.43.86.216";

desc "Install dependencies for deploy some microservices (MongoDB, Mysql and RabbitMQ Servers";
task "deployServers", group => "stack", sub {
   run "sudo apt-get update";
   say "System updated";

   pkg "mongodb-server", ensure => "present";
   say "MongoDB Server installed";

   pkg "mysql-server", ensure => "present";
   say "MySQL Server installed";

   pkg "rabbitmq-server", ensure => "present";
   say "RabbitMQ Server installed";
};

desc "Install all dependencies and modules required for NodeJs execuion (NodeJs, NodeJs-dev, Npm, Socket.io and Express)";
task "deployNode", group => "stack", sub {
   pkg "nodejs", ensure => "present";
   say "NodeJs installed";

   pkg "nodejs-dev", ensure => "present";
   say "NodeJs-dev installed";

   pkg "npm", ensure => "present";
   say "Npm installed";

   run "sudo npm install socket.io";
   say "Socket.io installed";
   run "sudo npm install express";
   say "Express installed";
};
```

Este script se debe llamar Rexfile y está dividido en dos tareas dependiendo del tipo de servicio que queramos provisionar en nuestro caso son "deployServers" para instalar todos los servidores (RabbitMQ, Mysql, Mongo) y "deployNode" para instalar NodeJs y todas las dependencias requeridas.

Y el resultado de la ejecución del mismo en una máquina en Trystack es el siguiente:
[Provisionando con Rex captura]()

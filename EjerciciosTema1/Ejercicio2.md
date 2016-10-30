# Ejercicio 2 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### En la aplicación que se ha usado como ejemplo en el ejercicio anterior, ¿podría usar diferentes lenguajes? ¿Qué almacenes de datos serían los más convenientes?
Como hemos comentado en el ejercicio anterior nuestra aplicación era una aplicación para dispositivos Android, en aquel momento se desarrolló en un solo lenguaje por su ya mencionada estructura monolítica y java era el único que se podía aplicar a la estructura. Si se adaptase a una estructura de microservicios como la que hemos comentado en el ejercicio 1, al usar un controlador central que se comunica mediante APIs REST no sería necesario restringirse a un lenguaje determinado y múltiples partes del programa si que hubieran podido tener otros lenguajes como python o ruby los cuales son más dinámicos y más sencillos de implementar.

En cuanto a los almacenes de datos que se utilizaron en la aplicación fueron únicamente SQLite.
Ampliando el desarrollo del programa se podría haber incorporado una base de datos tipo no relacional como MongoDB, para almacenar las posibles respuestas del usuario y poder así realizar minería de datos posterior al uso de la aplicación o incluso, una base de datos relacional como puede ser MaríaDB para almacenar el registro de los usuarios, en cuanto al apartado de la persistencia no se necesitó en un primer momento para la aplicación y no se incorporó en el sistema.


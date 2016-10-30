# Ejercicio 2 - Jos� Luis Fern�ndez Aguilera - Cloud Computing
## Enunciado
### En la aplicaci�n que se ha usado como ejemplo en el ejercicio anterior, �podr�a usar diferentes lenguajes? �Qu� almacenes de datos ser�an los m�s convenientes?
Como hemos comentado en el ejercicio anterior nuestra aplicaci�n era una aplicaci�n para dispositivos Android, en aquel momento se desarroll� en un solo lenguaje por su ya mencionada estructura monol�tica y java era el �nico que se pod�a aplicar a la estructura. Si se adaptase a una estructura de microservicios como la que hemos comentado en el ejercicio 1, al usar un controlador central que se comunica mediante APIs REST no ser�a necesario restringirse a un lenguaje determinado y m�ltiples partes del programa si que hubieran podido tener otros lenguajes como python o ruby los cuales son m�s din�micos y m�s sencillos de implementar.

En cuanto a los almacenes de datos que se utilizaron en la aplicaci�n fueron �nicamente SQLite.
Ampliando el desarrollo del programa se podr�a haber incorporado una base de datos tipo no relacional como MongoDB, para almacenar las posibles respuestas del usuario y poder as� realizar miner�a de datos posterior al uso de la aplicaci�n o incluso, una base de datos relacional como puede ser Mar�aDB para almacenar el registro de los usuarios, en cuanto al apartado de la persistencia no se necesit� en un primer momento para la aplicaci�n y no se incorpor� en el sistema.


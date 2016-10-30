# Ejercicio 1 - Jos� Luis Fern�ndez Aguilera
## Enunciado
### Buscar una aplicaci�n de ejemplo, preferiblemente propia, y deducir qu� patr�n es el que usa. �Qu� habr�a que hacer para evolucionar a un patr�n tipo microservicios?
Para este ejercicio vamos a analizar una aplicaci�n Android realizada para la asignatura de desarrollo de software esta aplicaci�n consist�a en una aplicaci�n tipo juego en la cual se realizaban preguntas y al usuario se le presentaban cuatro posibles respuestas, una de ellas era la acertada.

En esta aplicaci�n se utiliz� el patr�n MVC (Modelo, Vista, Controlador) el cual no es un patr�n muy escalable pero que funciona bien dentro de una aplicaci�n Android, adem�s del patr�n MVC se utiliz�n una arquitectura monol�tica la cual no podr�a ser desplegada correctamente en la red y necesitar�a bastantes cambios.

Para evolucionar a un patr�n centrado en los microservicios habr�a que partir el patr�n MVC y separar cada parte en un microservicio o dejar una parte, normalmente la de control, para controlar a los dem�s microservicios que formar�an la estructura del c�digo por lo que habr�a que remodelar la estructura monol�tica y separar cada actividad que realiza la aplicaci�n en un fragmento de c�digo ejecutable y escalable para formar as� una buena estructura de microservicios y que todo est� bien gestionado mediante el controlador y con la utilizaci�n de APIs REST.


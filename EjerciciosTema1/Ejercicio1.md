# Ejercicio 1 - José Luis Fernández Aguilera
## Enunciado
### Buscar una aplicación de ejemplo, preferiblemente propia, y deducir qué patrón es el que usa. ¿Qué habría que hacer para evolucionar a un patrón tipo microservicios?
Para este ejercicio vamos a analizar una aplicación Android realizada para la asignatura de desarrollo de software esta aplicación consistía en una aplicación tipo juego en la cual se realizaban preguntas y al usuario se le presentaban cuatro posibles respuestas, una de ellas era la acertada.

En esta aplicación se utilizó el patrón MVC (Modelo, Vista, Controlador) el cual no es un patrón muy escalable pero que funciona bien dentro de una aplicación Android, además del patrón MVC se utilizón una arquitectura monolítica la cual no podría ser desplegada correctamente en la red y necesitaría bastantes cambios.

Para evolucionar a un patrón centrado en los microservicios habría que partir el patrón MVC y separar cada parte en un microservicio o dejar una parte, normalmente la de control, para controlar a los demás microservicios que formarían la estructura del código por lo que habría que remodelar la estructura monolítica y separar cada actividad que realiza la aplicación en un fragmento de código ejecutable y escalable para formar así una buena estructura de microservicios y que todo esté bien gestionado mediante el controlador y con la utilización de APIs REST.


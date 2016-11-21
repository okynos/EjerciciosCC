# Ejercicio 2 - José Luis Fernández Aguilera - Cloud Computing
## Enunciado
### Crear una receta para instalar nginx, tu editor favorito y algún directorio y fichero que uses de forma habitual.


Para este ejercicio vamos a realizar un pequeño script de provisionamiento en Chef el cual instala nginx, el editor de texto emacs, el programa principal de python2.7 y la utilidad de python pip para instalar módulos python, finalmente se crea un fichero llamado README y se incorpora un pequeño texto al mismo.

```
package 'nginx'
package 'emacs'
package 'python2.7'
package 'pip'
directory '/home/ubuntu/ejercicios'
file "/home/ubuntu/ejercicios/README.txt" do
  owner "ubuntu"
  group "ubuntu"
  mode 00754
  action :create
  content "Ejercicios del Tema 2 - 1 ~ 6"
end
```

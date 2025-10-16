
<center>

# TÍTULO DE LA PRÁCTICA


</center>

***Nombre: Iván Pérez González***
***Curso: 1DAW 2025-2026*** 

### ÍNDICE

+ [Introducción](#id1)
+ [Objetivos](#id2)
+ [Material empleado](#id3)
+ [Desarrollo](#id4)
+ [Conclusiones](#id5)


#### ***Introducción***. <a name="id1"></a>

Aqui en este trabajo vamos a crear varios `.txt` y integrarlos dentro de unas ramas y realizar varios `git add .` y `git commit -m " "`


#### ***Objetivos***. <a name="id2"></a>

  1. Crear un README.md principal en el cual vamos a explicar los pasos.
  2. Ignorar distintos archivos para nuestro control de versiones.
  3. Añadimos varios ficheros y tag para complementar nuestro proyecto.
  4. Subimos todos nuestros cambios para que nuestro repositorio local y remoto esten en las mismas versiones.
  5. Hacemos un merge para unir nuestro repositorio local y el de la nube.
  6. Realizamos un listado de los cambios. `git config --global alias.list 'log --oneline --decorate --graph --all'`


#### ***Material empleado***. <a name="id3"></a>

Para la realización de este proyecto hemos hecho uso de un software de sistema de versiones como git, mas tarde una maquina virtual para asi poder clonar nuestro repositorio en clase.
Y luego un guardado en la nube como github y asi poder guardar nuestro repositorio con todas nuestras carpetas sin tener la necesidad de gastar espacio.


#### ***Desarrollo***. <a name="id4"></a>

  1. En primer lugar creamos el repositorio de manera publica para aue asi pueda acceder quien quiera:
  2. Luego ignoramos archivos para no subirlos a la rama remota con: `touch privado.txt`
  3. Aparte de ignorar ese archivos hacemos para ignorar tambien la carpeta: `echo "/privada" >> .gitignore`
  4. Añadimos un fichero 1.txt y un tag seguidamente:
       ```
       git tag v0.1
       touch 1.txt
       ```
  5. Subimos el tag a nuestro main: `git push origin main`
  6. Creamos una rama nueva y nos metemos dentro de la rama respectiva: `git branch v0.2` y `git checkout v0.2`
  7. Subimos la rama **Ojo** solo a la rama de v0.2: `git push origin v0.2`
  8. Creamos un conflicto entrando en el mismo archivo desde esta rama y la main, para asi mas tarde mergearlos:
     - Rama main `echo "Hola" >> 1.txt` y en la rama v0.2 `echo "Adios" >> 1.txt`
         - Realizamos el merge `git branch --merged`
         - Arreglamos el error con `nano 1.txt`
         - Y subimos los cambios
  9. Creamos una rama nueva para luego eliminarla:
      - git tag v0.2
        - git branch -d v0.2
  10. Listamos el repositorio para ver si todo esta correcto: `git config --global alias.list 'log --oneline --decorate --graph --all'`
      
         


#### ***Conclusiones***. <a name="id5"></a>

En esta practica he aprendido a manejarme mejor con el control de versiones de git y asi poder realizar `git add .` y `git commit -m ""`.
A su vez hemos creado un conflicto para poder solucionarlo y asi saber que hacer en esos casos. Y por ultimo un uso en general de todo git junto con la terminal para bajarnos nuestro repositorio a nuestra maquina y poder trabajar con ella en cualquier ordenador y poder subir los cambios.

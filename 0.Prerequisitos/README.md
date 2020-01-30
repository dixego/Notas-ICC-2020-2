* [Introducción](#introducción)
* [Linux y la terminal](#linux-y-la-terminal)
* [Manipulando el sistema de archivos](#manipulando-el-sistema-de-archivos)

# Introducción

El curso de Introducción a Ciencias de la Computación supone que los alumnos asistieron al
curso propedéutico que se imparte en la semana previa a la semana previa a la primera
semana de los semestres impares, para los de nuevo ingreso a la carrera de Ciencias de la
Computación.

El propósito del curso propedéutico es enseñar a los estudiantes varias habilidades
relacionadas con el uso de su computadora que resultan indispensables de saber durante el
transcurso de la carrera, tales como el manejo esencial de la terminal, el sistema de
archivos en Linux, el editor de texto Emacs, y el uso básico de Git.

Dada la aparente composición de este grupo, muchos de los alumnos inscritos podrían no
tener este conocimiento antecedente. Con el fin de alivianar tal situación, este documento
pretende mostrar aquél conocimiento esencial para poder elaborar las prácitcas de
laboratorio cómodamente.

# Linux y la terminal

Es honorable tradición de la carrera de Ciencias de la Computación utilizar como sistema
operativo alguna distribución de Linux. Esto ofrece diversas ventajas; entre ellas,
instalar y configurar herramientas de desarrollo de software tiende a ser
considerablemente más fácil en sistemas Linux que en, por ejemplo, Windows.

Se recomienda a los estudiantes instalar en sus computadoras una distribución de Linux con
el fin de más fácilmente acoplarse a las actividades del curso (**NOTA:** el procedimiento
de instalación se llevará a cabo bajo su propio riesgo). Se les recomienda instalar
[Fedora](https://getfedora.org/en/workstation/download/), si bien existen muchas
alternativas tales como [Manjaro](https://manjaro.org/) o
[Ubuntu](https://ubuntu.com/download/desktop).

Si por alguna razón usted se encuentra dudoso de despegarse de su sistema operativo
actual, y tal sistema es Windows 10 actualizado, una alternativa sub-óptima pero aceptable
es utilizar el Subsistema de Windows para Linux (por ejemplo, instalando [Ubuntu para
Windows 10](https://tutorials.ubuntu.com/tutorial/tutorial-ubuntu-on-windows#0) , con el
cual podrán utilizar una terminal ejecutando un kernel de Linux como si fuera una
aplicación cualquiera en su computadora con Windows 10.

Una vez instalada una distribución de Linux, habrá que familiarizarse con el uso de la
terminal para manipular el sistema de archivos e invocar comandos. 

Busque usted un programa llamado "Terminal" (o algo parecido) en su computadora y
ejecútelo. El resultado debería ser una ventana con texto como el siguiente (o similar):

```
usuario@computadora:~$
```

En esta ventana podremos utilizar el teclado para escribir comandos y presionar `Enter`
para ejecutarlos y observar el resultado. Aprendamos a ahora a hacer algunas cosas útiles
con la terminal.

# Manipulando el sistema de archivos

En cualquier momento dado al usar una terminal, nos encontramos "parados" en algún punto
del sistema de archivos de nuestra computadora. A este punto típicamente se le conoce como
*Directorio Actual* o *Working Directory*. Podemos saber la *ruta* completa del directorio
actual con el comando `pwd`:

(En adelante, los ejemplos de comandos siguen el siguiente formato: el *prompt* del shell
es aquello que precede al símbolo `$`, lo que lo sucede es el comando que se debe entrar,
y las líneas siguientes que no estén precedidas por el *prompt* representan la salida del
comando).

```
usuario@computadora:~$ pwd
/home/usuario
```

En donde el `/` inicial representa la raíz del sistema de archivos (el punto inicial de la
jerarquía) y las subsiguientes palabras separadas por `/` son directorios. La salida de
`pwd` (`p`rint `w`orking `d`irectory) nos indica que estamos en la carpeta principal del
usuario `usuario`, que en Linux comunmente se conoce comúnmente como `~`.

A continuación podemos enlistar todos los archivos y directorios contenidos en el
directorio actual con el comando `ls`:

```
usuario@computadora:~$ ls
Desktop   Documents   Music   Picutres    Templates   Videos
```

Podemos crear un directorio nuevo con el comando `mkdir`:

```
usuario@computadora:~$ mkdir Directorio
usuario@computadora:~$ ls
Desktop   Directorio    Documents   Music   Pictures    Templates   Videos
```

Podemos cambiar el directorio actual con el comando `cd`:

```
usuario@computadora:~$ cd Directorio
usuario@computadora:~/Directorio$ pwd
/home/usuario/Directorio
```

Todo lo que se pueda hacer con un mouse desde un explorador de archivos con interfaz
gráfica se puede hacer de manera equivalente con algún comando desde la terminal (y una
vez que uno se acostumbra, hacerlo desde la terminal suele ser más rápido).

Para una *overview* un poco más a profundidad de la términal y los comandos, se recomienda
leer [esta *cheat sheet*](https://www.git-tower.com/blog/command-line-cheat-sheet/). Más
allá de eso, se les recuerda que Google (o DuckDuckGo, o su buscador de preferencia) es su
amigo. 

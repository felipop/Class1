# FIRST CLASS
## GIT - GITHUB
### Temas
- [x] ¿Qué es GIT y GitHub?
- [x] Instalar git
- [x] Crear un proyecto
- [x] Crear un repositorio
- [x] Crear una cuenta en github
- [x] Enlazar el repositorio con github
- [x] Crear una rama de trabajo
- [x] Guardar los cambios del proyecto
- [x] Aplicar cambios en la rama principal

### 1. **¿Qué es GIT y GitHub?**
Git es un sistema que nos permite almacenar y gestionar los cambios de nuestros proyectos. Esto nos sirve para trabajar en equipo un mismo proyecto y saber quién hizo cada modificación. También para volver a una versión anterior en caso de que alguien haga un cambio que genere un error en el programa o en caso de que queramos ver cómo estaba el código antes.  
GitHub es una plataforma que nos permite trabajar con git facilmente y tener un lugar principal en donde se encuentra el código, lo cual permite trabajar en equipo facilmente.
### 2. **Instalar git**
Vas a la página de git y en la parte de descargas buscas tu sistema operativo.
En el caso de windows viene un instalador con muchas opciones, esto es lo que debes seleccionar:
  - En select components seleccionar todas
  - En choosing the default editor seleccionar VS Code
  - En adjusting your PATH seleccionar la tercera opción 
  - En choosing HTTP seleccionar la primera
  - En configure the line seleccionar la primera
  - en confugure the terminal seleccionar la primera
  - en Configuring extra opt seleccionar todas
Con esta configuraciónte bajará una terminal especial para trabajar con git
Para trabajar con git se usa la terminal, con la que se instala es más fácil.
Usar el siguiente comando para comprobar que se instaló.
```
git --version 
```
Se puede usar cualquier consola para trabajar con git
### 3. **Crear un proyecto**
Para crear un repositorio te posicionas en la carpeta en donde tienes el proyecto así
```
cd <FOLDER PATH>
```
Por ejemplo:
```
cd Documents/proyecto
```
Otra forma es hacer click derecho y seleccionar 'GIT Bash Here', eso te abre la consola ubicada en el directorio que seleccionaste
El comando `cd` nos sirve para movernos entre diectorios.  
Algunos ejemplos:
```
cd ..       //Nos manda al directorio anterior
cd ~        //Nos manda al firectorio padre
cd carpeta  //Nos manda a la carpeta que se encuentra dentro del directorio actual
```
Con la flecha arriba del teclado podemos acceder a comandos que hayamos usado antes.  
El comando `ls` nos dice qué carpetas y archivos hay en el directorio actual.  
Algunos ejemplos
```
ls          //Lista los archivos y carpetas
ls -l       //Lista los archivos y carpetas con sus permisos y fechas de creación
ls -h       //Lista los archivos y carpetas en formato legible
ls -a       //Lista los archivos y carpetas incluyendo archivos ocultos
ls carpeta  //Lista los archivos y carpetas que se encuentren dentro de la carpeta que le indiques
ls -lha     // Combina los 4 primeros comandos
```
El comando `mkdir carpeta` crea una carpeta con ese nombre.  
El comando `touch archivo` crea un archivo con ese nombre y si ya existe le cambia la fecha de creación.

### 4. **Crear un repositorio**
##### Config
Para que tu equipo pueda saber quién eres debes configurar git para que te reconozca.  
El comando `git config --global user.name "TU NOMBRE"` guarda tu nombre.  
El comando `git config --global user.email correo@dominio.com` guarda tu correo.  
##### Init
El comando `git init` crea un repositorio en la carpeta actual.  
El comando `git init carpeta` crea un repositorio en la carpeta que le digas.  
La carpeta que guarda el repositorio se llama .git y se encuentra oculta.  
El comando `rm archivo` elimina un archivo.  
El comando `rm -rf carpeta` elimina una carpeta.  
##### Iteración básica
El comando `git status` nos dice cuales cambios no se han guardado.  
El comando `git add -A` prepara los cambios para ser guardados.  
El comando `git commit -m "mensaje"` guarda los cambios con el mensaje que le digamos.  
### 5. **Crear una cuenta en github**
Registro básico
### 6. **Enlazar el repositorio con github**
1. Creamos un nuevo repositorion en github con el nombre del proyecto.  
2. Lo inicializamos con un README.  
3. Elegimos la licencia que queremos que tenga el proyecto, en github todo es público.  
4. Abrimos el readme y le damos una descripción al proyecto con un formato https://help.github.com/articles/basic-writing-and-formatting-syntax/  
5. Ahora vamos al repositorio en github, le damos en clonar/descargar.  
6. Copiamos el link https
7. Vamos a nuestra consola, en la carpeta del proyecto y ponemos:
```
git remote add origin URL_QUE_COPIASTE
```
8. hacemos `git branch --set-upstream-to=origin/master master` para que enlace nuestra rama principal con la rama principal de github.
9. Hacemos `git pull -r` para traer los archivos de github.
10. hacemos cambios en nuestro proyecto
##### Iteración completa
11. hacemos la iteración básica
12. Hacemos `git push --all` para subir nuestros cambios a github
13. comprobamos en github
### 7. **Crear una rama de trabajo**
Podemos subir nuestras páginas web a github y hacer que él la muestre.
1. subir los cambios de nuestra página web
2. crear la rama gh-pages con el comando `git branch gh-pages`
3. hacemos `git push --all`
4. revisamos en github
### 8. **Aplicar cambios en la rama principal**
Podemos añadir contenido a master y luego aplicar los cambios en gh-pages.
1. Hacer cambios
2. Hacemos la iteración básica
3. Vamos a la rama gh-pages con el comando `git checkout gh-pages`
> El comando `git checkout rama` sirve para cambiarnos de rama
4. Estando en la rama gh-pages aplicamos lo cambios con el comando `git merge master`Hacemos 
5. hacemos `git push --all` para subir los cambios
> Para aplicar cambios de una rama a otra, por ejemplo, aplicar los cambios de develop a master hacemos
> `git chechout master`
> `git merge develop`
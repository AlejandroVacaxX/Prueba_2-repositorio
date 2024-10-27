# Tarea 1: Introducción a Git

## Descripcion de la tarea

En el presente trabajo se busco tener una introduccion a GitHub, conocer la sintaxis basica para crear un 'repositorio' asi como agregar archivos al mismo, modificarlos y crear 'commits' para ayudarnos a conocer las modificaciones, gracias a esta tarea se reconocer los comandos basicos para la creacion de repositorios en GitHub, modificarlos y excluir archivos que no se quieren en el repositorio.

## Instrucciones de uso

### 1 lo primero sera tener instalada la ultima version de JAVA
Utiliza la siguiente linea de comando para saber tu versiond de JAVA 'java -version'

### 2 Compilaremos el codigo 
usando el siguiente comando 'javac "nombre_del_archivo".java', en este caso el comando para este archivo sera 
'javac HolaMundo.java'

### 3 EJECUCION
usando el siguiente comando ejecutaras el codigo
'java HolaMundo', si hiciste esos pasos al pie de la letra la consola 
mandara el siguiente texto en consola: "Hola Git"

## COMANDOS UTILIZADOS
#### Para inicializar el repositorio local:
'git init': debemos estar en la carpeta que queramos crear como repositorio, utiliza 'cd' para 
moverte entre las carpetas de tu cumputadora

git remote add ALIAS URL-GIT-REPOSITORIO-REMOTO: aqui agregaremos el URL del repositorio 
para agregarlo a nuestra cuenta de GitHub, aconsejo utilizar el SSH y no HTTP, en el 2021 se debo de poder 
inicializar con contraseña desde consola por seguridad, ahora debes tener un TOKEN, a mi me salto un error
al utilizar el TOKEN desde HTTP y resulto mas facil usarlo via SSH.

TOUCH .gitignore: Con esto creamos el archivo donde pondremos el nombre de todos los archivos que queremos
se ignoren y no sean enviados al repositorio, la sintaxis para ignorar archivos es bastante sencilla:

*.log si queremos ignorar todo archivo que termine asi
/nombrearchivo.log si solo queremos ignorar ese archivo
nombrearchivo.loh si queremos ignorar todo archivo con ese nombre

#### ENVIAR CAMBIOS AL REPOSITORIO REMOTO:
git add -A: Con este comando volveremos a enviar todo archivo de nuevo al 'stagin area'
git commit -m "mensaje del commit": con esto mandaremos los archivos al 'local repo'
git push ALIAS NOMBRE-RAMA: Con esto enviaremos nuestros archivos al 'remote repo'

En cualquier momento podemos utlizar el comando 'git status' para conocer el status de 
nuestros archivos, si esta en rojo aun no esta dentro del stagin area
con el color verde estara en el 'local repo' y si nuestra rama aparece vacia nuestros archivos
ya se encuentrar en el 'repositorio remoto'

'NOTA: en ALIAS regularmente usamos la palabra origin
       y NOMBRE-RAMA utilizamos master'

## Notas sobre el archivo .gitignore:
La creacion de este archivo se hizo con el siguiente comando
'touch .gitignore', dentro del archivo desde Visual Studio Code escribiremos los archivos que no queremos en el repositorio
en este ejercicio el archivo 'debug.log' no debe llegar al repositorio remoto
al poner en consola el comando 'git status' el archivo 'debug.log' debe aparecer en el apartado llamado 
"Untracked files".
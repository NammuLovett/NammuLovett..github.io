# nammulovett.github.io


# Readme
 
## _Guía GITHUB para principiantes_
 
> La guía definitiva que todo hijo de vecino desearía.
> Aquí describiré de forma sencilla
> El proceso que hemos seguido 
> En la clase de Despligue 
> del ciclo de Desarrollo de Aplicaciones Web
> Para testear como funciona el MarkDown
 
 
 
 
[![Logo](https://avatars.githubusercontent.com/u/113581148?v=4)](https://github.com/NammuLovett)
 
[![N|gitHub](https://lh3.googleusercontent.com/t9YJC7pOpFFQHVbOuJjp5znnMljFfz1-OL6k_arR-EWVFuAgO2k0d3Jdjho8-x6jeih73lQUv-haPE6DDLlLFr4vmoU=w128-h128-e365-rj-sc0x00ffffff)](https://github.com)
 
 
## GIT & GITHUB    
- PASO 0 - Creamos una cuenta en GITHUB    
- PASO 1 - Creamos repositorio en GITHUB    
- PASO 2 - Configuración SSH    
  - 2.1 Preferencias / SSH    
  - 2.2 Terminal
- PASO 3 - Comandos Git/GitHub  
  - PASO 3.1 - Sincronización entre GIT/GITHUB Terminal    
  - PASO 3.2 - VSCode - Sincronización entre GIT/GITHUB    
    - 3.2.1 Creamos un archivo    
    - 3.2.2  Source Control    
    - 3.2.3 Comentario    
    - 3.2.4 Sync Changes    
    - 3.2.5 Sincronización de repos    
    - 3.2.6 Clonar repositorio
  - PASO 4 - GIT BRANCHES
  - PASO 5 - GITFORK
  
    

 
 
# PASO 0 - Creamos una cuenta en GITHUB    
 
Introducimos en el navegador [GitHub.com](https://github.com/) y en sign in creamos la cuenta.
 
# PASO 1 - Creamos repositorio en GITHUB    
 
Pulsamos sobre la pestaña Repositorios y le damos al botón de Nuevo.
 - Se debe usar un nombre que no haya sido usado en otro repositorio de la cuenta.
 - Dejamos la opción pública por defecto.
 - Añadimos el README.md para poder hacer archivos como el que estás leyendo.
 
[![N|gitHub](https://csharpcorner-mindcrackerinc.netdna-ssl.com/article/steps-to-initialize-a-git-repository-and-push-the-changes-to-github-in-deta/Images/2841.png)](https://github.com)
 
    
# PASO 2 - Configuración SSH
 
Hacemos Click sobre el icono de usuario, a continuación en preferencias y en la columna de la izquierda buscamos SSH y GPG keys
 
[![N|gitHub](https://www.diegocalvo.es/wp-content/uploads/2020/04/image.png)](https://github.com)
 
- 2.0 Abre el terminal de Linux. Usaré los enlaces que nos proporciona GitHub para configurar la SSH
 
| SSH | Enlace |
| ------ | ------ |
| Comprobar SSH |  [Enlace 1](https://docs.github.com/es/authentication/connecting-to-github-with-ssh/checking-for-existing-ssh-keys) |
| Generar Clave |  [Enlace 2](https://docs.github.com/es/authentication/connecting-to-github-with-ssh/generating-a-new-ssh-key-and-adding-it-to-the-ssh-agent) |
| Añadir SSH |  [Enlace 3](https://docs.github.com/es/authentication/connecting-to-github-with-ssh/adding-a-new-ssh-key-to-your-github-account) |
 
 
 
 
- 2.1  Sustituye por su dirección de correo electrónico de GitHub.
 
```sh
$ ssh-keygen -t ed25519 -C "your_email@example.com"
```
- 2.2 Copie la clave pública SSH en su portapapeles. Si su archivo de clave pública SSH tiene un nombre diferente al del código de ejemplo, modifique el nombre del archivo para que coincida con su configuración actual. Al copiar su clave, no agregue líneas nuevas ni espacios en blanco. En la foto del ejemplo sería: 
| SHA256: AIAvK8wfeA8M+2rW2H21kF1H+f/eiN1g0BaEiju334 |
 
```sh
cat ~/.ssh/id_ed25519.pub
```
 
 
[![N|SSH](https://www.cyberciti.biz/media/new/faq/2018/10/Ubuntu-18.04-create-the-RSA-or-ed25519-key-pair.png)](https://github.com)
 
- 2.3 Añadir la clave SSH a GitHub
[![N|SSH](https://https://www.freecodecamp.org/news/content/images/2020/02/image-15.png)
 
 
# PASO 3 - Comandos Git/GitHub
 
- 3.1 Terminal
 
  - 3.1.1 Desde el terminal, comprobamos si está instalado Git.
 
```sh
git --version
```
Debería salir por el terminal algo parecido a lo que se mostrará a continuación, de lo contrario no tiene instalado Git.
```sh
Output
git version 2.33.0
```
 
- 3.1.2 Instalación GIT 
Antes de comenzar, debe instalar el software necesario para Git. Todo se encuentra disponible en los repositorios predeterminados, de modo que podemos actualizar nuestro índice local de paquetes y luego instalar los paquetes pertinentes.
```sh
sudo apt update
sudo apt install git
 
```
Ahora al comprobar si está la git debería aparecer el Output citado anteriormente.
 
- 3.1.3 Comandos de Git para repositorios
Para inicializar un repositorio, debes ubicarte en la carpeta en la que quieras iniciar el repositorio y pulsar el siguiente comando:
 
```sh
git init
```
Para añadir documentos al repositorio debes usar el comando add, si quieres preparar todos, debes poner un punto, de lo contrario, debes nombrar archivo a archivo
```sh
git add .
```
Commit es para confirmar que son esos archivos los que vas a enviarlos a GitHub, el -m sirve para poner el mensaje, sin esto no te deja realizar el commit y debes poner el siguiente comando:
```sh
git commit -m "Initial Commit" -a
```
 
Para enviar los archivos desde tu repositorio local al de tu usuario de GitHub debes  
```sh
git push origin main
```


# PASO 4 - GIT Branches

[![N|SSH](https://wac-cdn.atlassian.com/dam/jcr:389059a7-214c-46a3-bc52-7781b4730301/hero.svg?cdnVersion=549)

Una rama representa una línea independiente de desarrollo. Las ramas sirven como una abstracción para el proceso de edición/etapa/confirmación. Puede pensar en ellos como una forma de solicitar un directorio de trabajo, un área de preparación y un historial de proyectos completamente nuevos. Las nuevas confirmaciones se registran en el historial de la rama actual, lo que da como resultado una bifurcación en el historial del proyecto.

El comando git branch le permite crear, enumerar, renombrar y eliminar ramas. No le permite cambiar entre ramas o volver a armar un historial bifurcado. Por esta razón, git branch está estrechamente integrado con los comandos git checkout y git merge.

# 4.1 Comandos

## Crear rama
```sh
branch <branch>
```
Crea una nueva rama llamada ＜rama＞. 
No verifica la nueva rama.

## Listar ramas
```sh
git branch 
```
Haz una lista de todas las ramas en tu repositorio. Esto es sinónimo de git branch --list.

## Cambiar nombre de la rama
```sh
git branch -m <branch>
```
Cambie el nombre de la rama actual a ＜rama＞. 

## Borrar rama
```sh
git branch -d <branch>
```
Eliminar la rama especificada. Esta es una operación "segura" en la que Git evita que elimine la rama si tiene cambios no fusionados.

## Forzar a borrar una rama
```sh
git branch -D <branch>
```
Fuerce la eliminación de la rama especificada, incluso si tiene cambios no combinados. Este es el comando que debe usar si desea descartar permanentemente todas las confirmaciones asociadas con una línea de desarrollo en particular.

## Listar ramas remotas

```sh
git branch -a
```
Lista todas las ramas remotas.

## Cambiar de rama

```sh
git checkout ＜branchname＞
```
Conmutación de ramas. Al ejecutar lo siguiente, HEAD apuntará a la rama de ＜branchname＞. Añadiendo -b creas una nueva rama y la selecciona.
git checkout -b ＜new-branch＞
git switch tambien cambia la rama y añadiendo -c la crea.

##Fusionar (merge) cambios con Main

```sh
git merge
```

# Paso 5 - Git Fork (Bifurcar Proyecto)

Una bifurcación es una copia de un repositorio. Bifurcar un repositorio te permite experimentar libremente con cambios sin afectar el proyecto original.

Proponer cambios para el proyecto de otra persona

Por ejemplo, puedes utilizar ramificaciones para proponer cambios relacionados con arreglar un error. En lugar de registrar una incidencia para un error que has encontrado, puedes hacer lo siguiente:

   - Bifurque el repositorio.
   - Solucionar el problema.
   - Emitir solicitudes de cambios al propietario del proyecto.
   
## Bifurcar un repositorio (Hacer un fork)

Puedes ramificar un proyecto para proponer cambios en los repositorios precedentes u originales. En este caso, es una buena práctica sincronizar tu bifurcación periódicamente con el repositorio ascendente. Para hacerlo, deberás usar Git en la línea de comando. 

- Ve al repositorio específico.
- En la esquina superior derecha de la página, haga clic en Fork (Bifurcar). 

![](https://docs.github.com/assets/cb-23088/images/help/repository/fork_button.png)

- Selecciona un propietario para el repositorio bifurcado

![](https://docs.github.com/assets/cb-151543/images/help/repository/fork-choose-owner.png)

- De forma predeterminada, las bifurcaciones tienen el mismo nombre que sus repositorios primarios. Puedes cambiar el nombre de la bifurcación para distinguirlo aún más. 

![](https://docs.github.com/assets/cb-151542/images/help/repository/fork-choose-repo-name.png)

- Opcionalmente, puedes agregar una descripción de la bifurcación. 

![](https://docs.github.com/assets/cb-177452/images/help/repository/fork-description.png)

- Elige si quieres copiar solo la rama predeterminada, o bien todas las ramas en la nueva bifurcación. En muchos escenarios de bifurcación, como los de contribución a proyectos de código abierto, solo tienes que copiar la rama predeterminada. De forma predeterminada, solo se copia la rama predeterminada. 

![](https://docs.github.com/assets/cb-59189/images/help/repository/copy-default-branch-only.png)

- Haz clic en Crear bifurcación.

![](https://docs.github.com/assets/cb-80721/images/help/repository/fork-create-button.png)



#Clonar tu repositorio bifurcado

Ahora mismo, tienes una bifurcación del repositorio Spoon-Knife, pero no tienes los archivos de ese repositorio localmente en tu equipo.

 - En GitHub.com, vaya a la bifurcación del repositorio.

 - Encima de la lista de archivos, haga clic en Código. 
 
 ![](https://docs.github.com/assets/cb-20363/images/help/repository/code-button.png)
 
- Copia la dirección URL del repositorio.
   - Para clonar el repositorio con HTTPS, en «HTTPS» haz clic en

   - Para clonar el repositorio mediante una clave SSH, incluido un certificado emitido por la entidad de certificación SSH de la organización, haga clic en Usar SSH y luego en

   - Para clonar un repositorio mediante GitHub CLI, haz clic en GitHub CLI y, después, haz clic en

 ![](https://docs.github.com/assets/cb-33207/images/help/repository/https-url-clone-cli.png)
 
 
 - Abra Terminal. Cambia el directorio de trabajo actual a la ubicación en donde quieres clonar el directorio.
 
- Escriba git clone y pegue la dirección URL que ha copiado antes. Tendrá este aspecto, con su nombre de usuario de GitHub en lugar de YOUR-USERNAME:

```sh
$ git clone https://github.com/YOUR-USERNAME/nombre-fork
```

- Presione ENTRAR. Se creará tu clonación local.
```sh
$ git clone https://github.com/YOUR-USERNAME/nombre-fork
> Cloning into `nombre-fork`...
> remote: Counting objects: 10, done.
> remote: Compressing objects: 100% (8/8), done.
> remote: Total 10 (delta 1), reused 10 (delta 1)
> Unpacking objects: 100% (10/10), done.

```

#Hacer y subir cambios
Cuando estés listo para enviar tus cambios, pruébalos y confírmalos. git add . indica a Git que quiere incluir todos sus cambios en la siguiente confirmación. git commit toma una instantánea de esos cambios.

```sh
git add .
git commit -m "a short description of the change"
```

Cuando pruebas y confirmas archivos, esencialmente le dices a Git "¡Ok, toma una captura de mis cambios!" Puedes seguir haciendo más cambios y tomando más capturas de las confirmaciones.

Ahora mismo, tus cambios solo existen localmente. Cuando estés listo para subir tus cambios a GitHub, sube tus cambios al remoto.

```sh
git push
```

# Paso 6 - Pull Request - Hacer una solicitud de cambios

Para hacerlo, dirígete al repositorio de GitHub en donde vive tu proyecto. En este ejemplo, sería https://www.github.com/<your_username>/nombre-fork. Verá un banner que indica que la rama está una confirmación por delante de octocat:main. Haga clic en Contribute (Contribuir) y,después, en Open a pull request (Abrir una solicitud de incorporación de cambios).

GitHub le dirigirá a una página que muestra las diferencias entre la bifurcación y el repositorio octocat/Spoon-Knife. Haga clic en Create pull request (Crear solicitud de incorporación de cambios).


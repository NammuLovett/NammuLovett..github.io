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
 

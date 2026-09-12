# Elliutth Isaac Guevara Liñan
###### 2630015
## *Creación y sincronización de repositorios con Git y GitHub*
### *objetivo:*
Crear un repositorio local utilizando Git, sincronizarlo con un repositorio remoto en GitHub y comprobar el flujo de trabajo en ambos sentidos:  
__*Repositorio local → GitHub*__  
__*GitHub → Repositorio local*__
## *procedimiento* 
# __*1.0.- Crear el repositorio local*__
__1.1.-__ para crear el repositorio local lo primero que debemos hacer es entrar en powershell y con el comando mkdir crear una carpeta con el nombre de nuestro proyecto en mi caso ***"practica-git-elliutth-guevara"***.

__1.2.-__ una vez creada la carpeta debemos ingresar en ella desde la terminal para esto debemos utilizar el comando `cd "nombre de la carpera"`.

__1.3.-__ ahora que estamos dentro de la carpeta debemos inicializar el repositorio de git para esto es nesesario utilisar el comando `git init`.

__1.4.-__ ahora con el comando `git branch -M main` estableceremos main como la rama principal.

__1.5.-__ ahora nesesitamos 2 archivos uno con el nombre datos.txt y otro con el nombre README.md que casualmente es este archivo que estas leyendo para crearlos podemos hacerlo de la forma tradicional o con el comando `New-Item -Path "datos.txt" -ItemType File` en el caso de el otro archivo cambiamos datos.txt por README.md en el comando.

__1.6.-__ ahora podemos comenzar a editar el archivo .txt en su contenido escribi "git es una herramienta que funciona en conjunto con github para la creacion de repositorios y control de versiones".
# __*2.0.-Registra los primeros cambios*__
__2.1.-__ con el comando `git status` verificamos el estado de el repositorio asi veremos si hay archivos nuevos para añadir a la staging area.

__2.2.-__ ahora para añadir esos archivos a la staging area utilizamos el comando `git add -A` para añadir todos los nuevos archivos.

__2.3.-__ con `git status` volvemos a verificar el estado del repositorio y veremos ambos archivos de color verde lo que quiere decir que estan listos para realizar un commit.

__2.4.-__ ahora tenemos todo listo para realizar el primer commit para esto usamos el comando `git commit -m "primer commit"`.

# __*3.0.-crear un repositorio en github*__
__3.1.-__ crear un repositorio en github con el mismo nombre que el repositorio local el repositorio lo pondremos publico y mantendremos README. gitignore Licencia inactivos.

__3.2.-__ vincularemos el repositorio de github con el repositorio local para eso en github nos da 3 opciones yo utilize ssh y debemos usar el comando `git remote add origin "el url que te da la opcion ssh"` en la powershell, en mi caso queda:  
 __`git remote add origin git@github.com:Elliutth/practica-git-elliutth-guevara.git`__.

__3.3.-__ con `git remote -v` confirmaremos que el repositorio se ha vinculado correctamente.

__3.4.-__ Ahora enviaremos el repositorio a github por primera vez utilizando el comando git push -u origin main y podemos entrar a github a confirmar que los cambios se realizaron.

# __*4.0.0-realiza cambios desde github y desde el repositorio local*__
__4.1.1.-__ dede github realiza un cambio en el archibo datos.txt agrega una nueva linea que diga "este archivo fue modificado desde github" y guarda los cambios.

__4.1.2.-__ regresa al repositorio local en powershell y descarga los cambios para eso usa el comando `git pull origin main`, ahora puedes verificar los cambios en el archivo.

__4.2.1.-__ ahora realiza un cambio desde el repositorio local en el mismo archivo datos.txt ahora añade una line que diga "este archivo fue editado desde el repositorio local".

__4.2.2.-__ ahora en powershell verifica el estado del repositorio con git status y aparecera que el archivo datos.txt fue editado.

__4.2.3.-__ añadimos los cambios con `git add -A`.

__4.2.4.-__ y procedemos a hacer un nuevo commit con el comando `git commit -m "Actualización desde repositorio local"`.

__4.2.5.-__ con `git push` enviamos los cambios de regreso a github una ves enviados los cambios podemos ir a github a verificar que el cambio se aya realizado.
# __*5.-comandos de git y breve explicacion*__
```bash
git init 
# inicialisa un repositorio de git
```
```bash
git branch -M main
# establece main como la rama principal
```
```bash
git status
# te muestra el estado de tu repositorio
```
```bash
git add -A
# añade todos los archivos de el repositorio a la Staging Area
```
```bash
git commit -m "primer commit"
# guarda los cambios en un commit
```
```bash
git log
# muestra el historial completo de commits en orden cronológico inverso
```
```bash
git remote add origin git@github.com:Elliutth/practica-git-elliutth-guevara.git
# vincula un repositorio local con un repositorio de github
```
```bash
git remote -v
# muestra los nombres de los remotos configurados
```
```bash
git push -u origin main
# enviar los commits de tu repositorio local a un repositorio remoto
```
```bash
git commit -m "edite el arcivo datos.txt"
# se genera un commit con un comentario cualquiera
```
```bash
git pull origin main
# actualizar tu rama local con los últimos cambios de la rama main en el repositorio remoto
```
```bash
git commit -m "Actualización desde repositorio local"
# guarde un cambio desde el repositorio local
```
# sincronisacion local a github
la sincronisacion local a github se usa cuando hisiste un cambio desde el escritorio a alguno de los archivos de tu repositorio de git, si quieres sincronisar los cambios o refrescar los cambios nesesitas realizar los siguientes pasos en la terminal.

```bash
git add -A
```
                          ↓
```bash
git commit -m "mensaje"  
```
                          ↓
```bash
git push
```
y despues de seguir esos pasos ya deberiamos de ser capases de visualisar cambios en nuestro repositorio de github.
# sincronisacion github a local
la sincronisacion de github a local se da cuando editamos alguno de los archivos de nuestro repositorio desde github y guardamos los cambios, para sincronisar hay que usar git pull.

```bash
git pull
```
lo que hace este comando es bajar los archivos de la nube de github y los guarda en el repositorio que le corresponde.

# descripcion  de los archivos
## el archibo datos.txt
No debe incluir código ejecutable de Python, solo la materia prima de información (números, textos, fechas) que el script se encargará de parsear.  
pero en este caso solo contiene mi nombre matricula una breve descripcion de git y github y que fue modificado en 2 ocaciones una desde github y otra desde el repositorio local.
## el archibo README.md
README.md debe contener una descripción clara del proyecto, junto con instrucciones de instalación y uso para que cualquier persona pueda entenderlo y ejecutarlo rápidamente.  
pero en mi caso es tecnicamente un instructivo de uso de git y github en conjunto.
### concluciones
esta practica me ayudo a entender de mejor manera el funcionamiento y uso de git y github ademas de mejorar la forma en que uso la terminal.   
tambien entender un poco mas como se conforman los archivos nesesarios para un proyecto y poder trbajar mas facilmente a futuro.
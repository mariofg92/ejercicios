#Documentación de la práctica 0
### 1. Creación y subida de la clave de github.

Creamos la clave con:
> $ ssh-keygen -t rsa -b 4096 -C "your_email@example.com"

y completamos todos los pasos de localización y passphrase.
Una vez hecho esto añadimos la clave al cliente de ssh con:
> $ ssh-add "ruta de la clave"

Por ultimo añadimos la clave a la cuenta de github copiando la clave con:

> $ pbcopy < ~/.ssh/id_rsa.pub

y agregandola a la web de github en *Settings>SSH and GPG keys>New SSH key* 

### 2. Configuración del nombre y correo para la aparición en los commits.

> $ git config --global user.name "Tu_nombre"

> $ git config --global user.email "tu_correo"

Adicionalmente podemos también activar el coloreado de consola para los mensajes proporcionados por git con:

> $ git config --global color.ui true

### 3. Editamos nuestro perfil de github.

Para ello desde la web de github en la parde de nuestro perfil lo editamos y completamos al menos los datos más relevantes en "add a bio"(foto, nombre y bio).

### 4. Creamos hitos e isuess.

Desde la web del repositorio en github añadimos los correspondientes issues y hito (aquí llamados millestones, que también se crean desde la pestaña de issues). 

### 5. Usando nuestro repositorio en nuestro pc.

> $ git clone https://github.com/mariofg92/ivmario

Tras modificar el readme.md y el gitignore.md, hacemos:

> $ git add .
> 
> $ git commit -m "Actualizando README.md y subiendo .gitignore"
> 
> $ git push

Creamos una nueva rama en el proyecto para la documentación:

> $ git checkout -b rama0

Una vez tenemos editada esta misma documentación hacemos:

> $ git add hito0.md
> 
> $ git commit -m "Añadida la documentación closes #1"
> 
> $ git push origin rama0

### 6.Trabajando con el repositorio común de la asignatura.

Hacemos un fork del repositorio desde la web de github.

En el directorio donde queramos tener este repositorio hacemos:

> $ git clone https://github.com/mariofg92/IV16-17


Antes de modificar el 0.md y realizar el pull request hacemos un git remote add upstream para asegurarnos de que todo está al día en nuestra maquina local.

> $ git remote add upstream https://github.com/JJ/IV16-17
> 
> $ git fetch upstream
> 
> $ git checkout master
> 
> $ git merge upstream/master
> 
> $ git push


Por último modificamos el 0.md y realizamos el pull request.


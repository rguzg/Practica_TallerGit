# Cheatsheet de Git y Markdown

En esta cheatsheet podrás encontrar significados de conceptos y comandos de Git y Markdown.

## Conceptos de Git

### Sistema de Control de Versiones
También conocidos como Version Control System. Aplicación que permite mantener un historial de los cambios que se le hayan realizado a una colección de archivos. Los sistemas de control de versiones te permiten deshacer cambios y restaurar versiones anteriores de los archivos, además de facilitar la colaboración entre personas.

### Git
Sistema de control de versiones creado por Linus Torvalds en 2004. Se caracteriza por ser bueno con proyectos grandes, ser rápido y tener buen manejo de ramas

### Repositorio
Carpeta donde se está utilizando Git. Los repositorios tienen una carpeta escondida llamada `.git` donde se almacenan las estructuras que usa Git para funcionar. 

### Commit
Colección de cambios. Para registrar los cambios de uno o más archivos se debe crear un nuevo commit. 

### Working Directory
Área actual donde se encuentran los archivos con los que estamos trabajando (normalmente son la versión más reciente de los archivos)

### Estados de archivos en el Working Directory
Git le asigna un estado a cada archivo, dependiendo de su relación con la versión anterior del archivo:
- Untracked: Archivo nuevo. Git no tiene ninguna versión anterior de este archivo
- Modified: Archivo diferente a la versión anterior del archivo. Es posible ver que ha cambiado de la versión anterior a la actual
- Deleted: El archivo se eliminó

### Staging Area
Área donde se agregan los cambios que se agregarán al siguiente commit

### gitignore
Archivo que le dice a git que archivos no tomar en cuenta. Solo puede ignorar archivos untracked

### gitkeep
Archivo que se puede colocar dentro de una carpeta vacía para que Git la tome en cuenta

### GitHub
Servicio que permite subir repositorios a la nube

### Repositorio Remoto
Copia de un repositorio en la nube 

### Branch/Rama
Línea del tiempo alternas utilizada para trabajar de forma separada

### Merge
Acción de juntar los cambios de una rama a otra

### Merge Conflict
Problema que ocurre cuando se editan la(s) misma(s) línea(s) de un archivo en dos ramas separadas

### Fork
Copia de un repositorio que mantiene su conexión con el repositorio original

### Pull Request
Los pull request sirven para pedir permiso de hacer merge de un rama a otra o de un fork de un repositorio al repositorio original

## Comandos de Git
Los argumentos de los comandos se muestran dentro de llaves.

### git
Muestra una lista de algunos comandos que puedes utilizar con Git y sirve para saber si Git se instaló correctamente

### git init
Crea un repositorio dentro de la carpeta donde ejecutemos este comando

### git status
Muestra el estado actual del repositorio:
- Muestra la rama actual en la que nos encontramos
- Muestra si la rama está al corriente con respecto a la rama remota
- Muestra los archivos que están en el staging area y los archivos untracked 

### git add [nombre del archivo]
Agrega un archivo al staging area. Para agregar todos los archivos de una carpeta se debe utilizar el comando `git add .`

### git commit -m "[mensaje]"
Crea un nuevo commit a partir de lo que se encuentre en el staging area

### git log
Muestra un resumen de todos los commits que se hayan hecho en un repositorio

### git log [nombre del archivo]
Muestra un resumen de todos los commits que hayan modificado a un archivo en especifico

### git remote
Muestra una lista de los repositorios remotos relacionados con el repositorio actual

### git remote add [alias del repositorio remoto] [URL del repositorio remoto]
Añade un nuevo repositorio remoto

### git pull
Sincroniza los cambios del repositorio remoto con tu repositorio local

### git push
Sincroniza los cambios de tu repositorio local con tu repositorio remoto

### git push --set-upstream [alias del repositorio remoto] [nombre de la rama]
Crea una nueva rama en el repositorio remoto y la sincroniza con la rama local

### git clone [URL del repositorio]
Copia un repositorio en la nube a tu computadora

### git branch
Muestra una lista de las ramas existentes en el repositorio actual

### git branch [nombre de la rama]
Crea una nueva rama. El commit que tomará como base será el commit más reciente

### git checkout [nombre de la rama]
Permite cambiarte de rama

### git merge [nombre de la rama]
Realiza un merge entre la rama actual y la rama especificada 

## Sintaxis de gitignore
Todas las rutas que se encuentren dentro del archivo `.gitignore` son relativas al folder donde se ubique el archivo `.gitignore`

### Ignorar archivos y folders
Utiliza el nombre del archivo o folder que quieras ignorar. Por ejemplo, para ignorar el archivo **README.md**: <br>

```
README.md
```

Recuerda que debes de incluir la ruta completa del archivo. Por ejemplo, si quisieras ignorar el archivo **Contraseñas.txt** que está dentro de la carpeta **Archivos**: <br>
```
Archivos/Contraseñas.txt
```

### Comodines
También puedes utilizar el comodín `*`. Este comodín indica que en esa sección puede ir cualquier carácter. Por ejemplo:

- Para ignorar todos los archivos que tengan la extensión **txt**: <br>
```
*.txt
```
- Para ignorar todos los archivos que tengan el nombre **contraseñas**, sin importar su extensión: <br>
```
contraseñas.*
```

Para ignorar archivos dentro de todos los folders, se utiliza el comodín `**`. Por ejemplo, para ignorar los archivos **Contraseñas.txt** dentro de todas las carpetas: <br>
```
**/Contraseñas.txt
```

### Carácter `!`
- Para no ignorar un archivo se utiliza el carácter `!`. Por ejemplo, para **no** ignorar el archivo **README.md**: <br>
```
!README.md
```
- Las reglas de gitignore se aplican de arriba para abajo, por ejemplo, estas reglas ignorarán **README.md**, incluso si se incluye **!README.md**: <br>
```
!README.md
*.md
```

- La forma correcta de ignorar todos los archivos con extensión **.md** excepto por **README.md** es: <br>
```
*.md
!README.md
```

## Sintaxis de Markdown

Markdown es un lenguaje que permite darle formato a texto. Se caracteriza por ser fácil de leer y por ser utilizado para escribir la documentación de proyectos de programación

### Texto normal

- Sintaxis en Markdown:
```markdown
Texto normal
```

- Markdown renderizado: <br>
Texto normal

### Texto en negritas

- Sintaxis en Markdown:
```markdown
**Texto en negritas**
```

- Markdown renderizado: <br>
**Texto en negritas**

### Texto en cursiva

- Sintaxis en Markdown:
```markdown
_Texto en cursiva_
```

- Markdown renderizado: <br>
_Texto en cursiva_

### Headers
Los headers permiten indicar las secciones y subsecciones de un documento. Existen seis niveles de headers

- Sintaxis en Markdown:
```markdown
# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6
```

- Markdown renderizado:
# Header 1
## Header 2
### Header 3
#### Header 4
##### Header 5
###### Header 6

### Imágenes

- Sintaxis en Markdown:
```markdown
![Descripción de la imagen. Es utilizada por lectores de texto o cuando la imagen no carga](URL de la imagen)
```

- Markdown renderizado: <br>
![Carby. Kirby fused with a car](https://external-content.duckduckgo.com/iu/?u=https%3A%2F%2Ftechnology.thenewsupdate.co%2Fupdate-https-cdn.wccftech.com%2Fwp-content%2Fuploads%2F2022%2F02%2FWCCFkirbyandtheforgottenland2.jpg&f=1&nofb=1)

### Link

- Sintaxis en Markdown:
```markdown
[Texto del link](URL al link)
```

- Markdown renderizado: <br>
[Trailer oficial de Half Life 3](https://www.youtube.com/watch?v=dQw4w9WgXcQ)

### In-Line Code

- Sintaxis en Markdown:
```markdown
`Texto que tendrá formato de código`
```

- Markdown renderizado: <br>
`Texto que tendrá formato de código`

### Code Block

- Sintaxis en Markdown:
```markdown
`‎`‎`‎Lenguaje de programación que se está utilizando
// Código de JavaScript
let message = "Hello World!";
console.log("Hello World!");
`‎`‎`‎
```

- Markdown renderizado:
```JavaScript
// Código de JavaScript
let message = "Hello World!";
console.log("Hello World!");
```


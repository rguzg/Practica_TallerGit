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

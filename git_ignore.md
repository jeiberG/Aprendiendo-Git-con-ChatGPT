En el contexto del uso de Git, un **archivo** .gitignore es un archivo de texto que especifica qué archivos y directorios Git debe ignorar intencionalmente. Esto significa que .**gitignore** Git no rastreará los archivos o directorios enumerados en, y los cambios en ellos no se prepararán para confirmaciones a menos que se agreguen explícitamente usando git add.

## Propósito de .gitignore:
* **Ignorar archivos generados:** muchos entornos de programación generan archivos que no son necesarios para el proyecto en sí, como archivos binarios compilados, archivos de registro o archivos temporales creados por IDE. Estos archivos saturan el repositorio y, a menudo, no es necesario compartirlos ni controlar las versiones.

* **Evitar información confidencial:** los archivos de configuración que contienen información confidencial, como claves API o contraseñas, no deben incluirse en el repositorio por razones de seguridad. **.gitignore** ayuda a evitar la inclusión accidental de datos tan confidenciales.

* **Mejorar la claridad del repositorio:** al excluir archivos irrelevantes, .gitignore se ayuda a mantener un repositorio más limpio y enfocado, lo que facilita que los contribuyentes comprendan qué es esencial para el proyecto.

## Cómo utilizar .gitignore:
Para utilizar .gitignore, siga estos pasos:

* **Cree o modifique el archivo:** cree un .gitignore archivo en el directorio raíz de su repositorio Git si aún no existe ninguno. Puede modificarlo en cualquier momento para agregar o eliminar patrones.

* **Especificar patrones:** dentro de .gitignore, especifique patrones de archivos y directorios utilizando patrones globales o nombres de archivos exactos. Cada patrón debe estar en una nueva línea.

* **Confirmar .gitignore:** después de configurarlo .gitignore, confírmelo en su repositorio. Luego, Git comenzará a ignorar archivos y directorios de acuerdo con las reglas especificadas en .gitignore.

Archivo de ejemplo .gitignore:
```sh
    # Ignore compiled binaries
    *.exe
    *.o

    # Ignore log files
    *.log

    # Ignore directory
    /build/
```

En este ejemplo:

*.exee *.o ignorará todos los archivos con .exey .oextensiones respectivamente.

*.log ignora todos los archivos de registro.
/build/ignora todo el builddirectorio.

**Notas:**

**Comentarios:** Las líneas que comienzan con #son comentarios.

**Espacios en blanco:** se ignoran las líneas en blanco o los espacios en blanco finales.

El uso .gitignoreeficaz garantiza que su repositorio Git contenga solo los archivos necesarios y permanezca centrado en el código fuente del proyecto y los recursos esenciales.

## Archivo general de .ignore
```sh
    # Archivos de sistema
    .DS_Store
    Thumbs.db

    # Archivos temporales
    *~
    *.swp

    # Archivos de compilación
    *.o
    *.obj
    *.class
    *.dll
    *.exe

    # Archivos de configuración local
    *.log
    *.sql
    *.sqlite
    *.sqlite3
    *.env

    # Directorios de dependencias o generados automáticamente
    /node_modules/
    /vendor/
    /dist/
    /build/
    /out/
    /.idea/
    /.vscode/
    /.vs/

    # Archivos de IDEs y editores
    *.sublime-project
    *.sublime-workspace
    *.suo
    *.user
    *.sln
    *.csproj
    *.xcodeproj
    *.xcworkspace

    # Archivos de archivos de logs
    *.log

    # Ignorar todo un subdirectorio
    logs/

```
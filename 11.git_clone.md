# git clone
es un comando de Git que se utiliza para crear una copia local de un repositorio remoto. Básicamente, descarga el contenido del repositorio y todos sus archivos asociados a tu máquina local, permitiéndote trabajar con ellos.

## Uso Básico
El comando básico para clonar un repositorio es:
```sh
    git clone <URL-del-repositorio>
```
## Ejemplo
Si quieres clonar un repositorio desde GitHub, por ejemplo:
```sh
    git clone https://github.com/usuario/nombre-del-repositorio.git
```
Esto creará una copia local del repositorio en una carpeta llamada nombre-del-repositorio en tu directorio actual.

## Opciones Comunes
* ``--branch <nombre-de-la-rama>``: Clona una rama específica del repositorio.
```sh
    git clone --branch develop https://github.com/usuario/nombre-del-repositorio.git
```

* ``-depth <n>``: Clona solo los últimos ``n`` commits de la historia.
```sh
    git clone --depth 1 https://github.com/usuario/nombre-del-repositorio.git
```
* ``--single-branch``: Clona solo la rama especificada, sin las demás ramas.
```sh
    git clone --single-branch --branch main https://github.com/usuario/nombre-del-repositorio.git
```

## Resumen
git clone es una herramienta esencial para empezar a trabajar con un proyecto que ya está alojado en un repositorio remoto, permitiéndote obtener una copia local completa para desarrollar, revisar y contribuir al proyecto.
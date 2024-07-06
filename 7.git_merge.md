# ¿Qué es git merge?
git merge es un comando en Git que se utiliza para combinar cambios de diferentes ramas en una sola. Es una herramienta esencial para integrar el trabajo de múltiples ramas en un repositorio y mantener una línea de tiempo de desarrollo coherente.

## Funcionalidades de git merge
* **Fusionar ramas:** Combina el historial de commits de una rama en otra.

* **Resolver conflictos:** Durante la fusión, si hay cambios conflictivos en ambas ramas, Git señalará los conflictos para que puedan resolverse manualmente.

* **Mantener historial:** A diferencia de git rebase, que reescribe el historial, git merge mantiene el historial de ambas ramas.

## Uso básico de git merge
**1. Fusionar una rama en la rama actual**

Para fusionar una rama llamada feature-branch en la rama actual:
```sh
    git checkout main
    git merge feature-branch
```
**2. Resolver conflictos de fusión**

Si hay conflictos durante la fusión, Git señalará los archivos conflictivos. Puedes resolver los conflictos editando los archivos y luego completando la fusión:
```sh
    # Editar los archivos conflictivos
    git add archivos_resueltos
    git commit -m "Resolver conflictos de fusión"
```

## Ejemplos prácticos
Aquí hay algunos ejemplos prácticos para entender mejor el uso de git merge:

**Ejemplo 1: Fusionar una rama sin conflictos**

Crear y cambiar a una nueva rama:
```sh
    git checkout -b feature-a
```
Hacer algunos cambios y confirmar:
```sh
    echo "Cambios en feature-a" > archivo.txt
    git add archivo.txt
    git commit -m "Cambios en feature-a"
```
Cambiar de vuelta a la rama main y fusionar feature-a:
```sh
    git checkout main
    git merge feature-a
```
Eliminar la rama feature-a si ya no es necesaria:
```sh
    git branch -d feature-a
```

**Ejemplo 2: Fusionar una rama con conflictos**
Crear dos ramas y hacer cambios conflictivos:
```sh
    git checkout -b feature-b
    echo "Cambios en feature-b" > archivo.txt
    git add archivo.txt
    git commit -m "Cambios en feature-b"

    git checkout main
    git checkout -b feature-c
    echo "Cambios en feature-c" > archivo.txt
    git add archivo.txt
    git commit -m "Cambios en feature-c"
```

Intentar fusionar feature-c en main, lo que producirá un conflicto:
```sh  
    git checkout main
    git merge feature-c
```

Resolver el conflicto editando archivo.txt:
```sh
    # Editar archivo.txt para resolver el conflicto
    git add archivo.txt
    git commit -m "Resolver conflicto de fusión"
```
**Ejemplo 3: Crear un commit de fusión sin hacer cambios**

Crear y cambiar a una nueva rama:
```sh
    git checkout -b feature-d
```
Hacer algunos cambios y confirmar:
```sh
    echo "Cambios en feature-d" > archivo.txt
    git add archivo.txt
    git commit -m "Cambios en feature-d"
```

Cambiar de vuelta a la rama main y fusionar feature-d sin conflictos:
```sh
    git checkout main
    git merge feature-d
```

## Opciones útiles de git merge
**1. Fusión sin commit automático**

Si deseas fusionar y revisar los cambios antes de hacer un commit, usa la opción --no-commit:
```sh
    git merge --no-commit feature-branch
```

**2. Fusión sin avance rápido (fast-forward)**

Para forzar una fusión con un commit de merge incluso si podría hacerse un fast-forward, usa la opción --no-ff:
```sh
    git merge --no-ff feature-branch
```

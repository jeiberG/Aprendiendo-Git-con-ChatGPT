# ¿Qué son las ramas (branches) en Git?
Las ramas (branches) en Git son una característica fundamental que permite desarrollar diferentes versiones de un proyecto de forma simultánea. Cada rama puede contener una serie de commits que representan una línea de desarrollo independiente de la rama principal (generalmente main o master). Esto facilita la implementación de nuevas funcionalidades, la corrección de errores y la experimentación sin afectar el código principal del proyecto.

## Conceptos clave
* **main o master:** La rama principal del proyecto.
* **Rama de características (feature branch):** Una rama creada para desarrollar una nueva funcionalidad.
* **Rama de corrección de errores (bugfix branch):** Una rama creada para corregir un error específico.
* **Rama de lanzamiento (release branch):** Una rama creada para preparar un lanzamiento.
## Funcionalidades de las ramas
* **Aislamiento de desarrollo:** Permite trabajar en nuevas características, corregir errores o realizar experimentos sin afectar la rama principal.
* **Colaboración:** Facilita la colaboración en equipo, ya que cada desarrollador puede trabajar en su propia rama y luego fusionar los cambios.
* **Historial limpio:** Ayuda a mantener un historial de commits más limpio y organizado.
## Comandos básicos para trabajar con ramas
1. Crear una nueva rama
```sh
    git branch nombre_de_la_rama
```
2. Cambiar a una rama
```sh
    git checkout nombre_de_la_rama
```

3. Crear y cambiar a una nueva rama
```sh
    git checkout -b nombre_de_la_rama
```
4. Listar todas las ramas
```sh
    git branch
```
5. Eliminar una rama
```sh
    git branch -d nombre_de_la_rama
```
6. Para forzar la eliminación de una rama que no ha sido fusionada:
```sh
    git branch -D nombre_de_la_rama
```
7. Fusionar una rama con otra
```sh
    git checkout main
    git merge nombre_de_la_rama
```
8. cambiar nombre de una rama

* cuando estamos en una rama diferente a la que queremos cambiar el nombre.
```sh
    git branch -m nombre-de-la-rama nombre-nuevo
```
    
* cuando estamos en la rama que queremos cambiar el nombre
```sh
    git branch -m nombre-nuevo 
```
    
# git switch
El comando git switch se introdujo en Git 2.23 como una alternativa más intuitiva a git checkout para cambiar de ramas.
**1. Cambiar a una rama existente**
```sh
    git switch nombre-de-la-rama
```
Este comando cambia la rama actual a nombre-de-la-rama.

**2. Crear y cambiar a una nueva rama**
```sh
    git switch -c nombre-de-la-rama
```
Este comando crea una nueva rama llamada ``nombre-de-la-rama`` y luego cambia a ella.

## Ejemplos prácticos
**Ejemplo 1:** Cambiar a una rama existente

Si tienes una rama llamada develop y quieres cambiar a ella:
```sh
    git switch develop
```
**Ejemplo 2:** Crear y cambiar a una nueva rama

Si quieres crear una nueva rama llamada ``feature-x`` y cambiar a ella:
```sh
    git switch -c feature-x
```
**Ejemplo 3:** Eliminar una rama

Si tienes una rama llamada old-branch que ya no necesitas y quieres eliminarla:
```sh
    git branch -d old-branch
```

**Ejemplo 4:** Renombrar una rama específica

Si quieres renombrar la rama ``old-name`` a ``new-name``:
```sh
    git branch -m old-name new-name
```
**Ejemplo 5:** Renombrar la rama actual

Si estás en una rama y quieres renombrarla a ``new-branch``:
```sh
    git branch -m new-branch
```
q

En Git, los conflictos de fusión ocurren cuando dos ramas que se están fusionando tienen cambios en la misma parte de un archivo, o cambios que entran en conflicto de alguna manera. Esto puede suceder cuando varias personas trabajan en la misma base de código. A continuación se ofrece una descripción general de qué son los conflictos de fusión y las mejores prácticas para manejarlos:

# ¿Qué es un conflicto de fusión?
Un conflicto de fusión ocurre cuando:

* **Ediciones en la misma línea :** dos ramas tienen cambios en la misma línea de un archivo.
* **Ediciones del mismo archivo :** dos ramas tienen cambios en el mismo archivo y Git no puede determinar automáticamente qué cambios se deben aplicar.
* **Eliminación y modificación :** una rama elimina un archivo mientras que otra rama lo modifica.
* **Manejo de conflictos de fusión**
Cuando encuentre un conflicto de fusión, Git pausará el proceso de fusión y marcará los conflictos en los archivos afectados, lo que le permitirá resolverlos manualmente. El archivo incluirá marcadores de conflicto con este aspecto:


```sh
    <<<<<<< HEAD
    Changes from the current branch
    =======
    Changes from the branch being merged in
    >>>>>>> branch-to-merge
```
Debes decidir cómo integrar estos cambios.

A continuación se muestra un proceso paso a paso para resolver conflictos de fusión:

* **Identificar conflictos :** utilícelo git statuspara ver qué archivos tienen conflictos.
* **Abrir archivos en conflicto :** abra cada archivo en conflicto en un editor de texto.
* **Resolver conflictos :** edite manualmente el archivo para resolver conflictos. Elimine los marcadores de conflicto ( <<<<<<<, =======, >>>>>>>) y realice los cambios necesarios.
* **Preparar los archivos resueltos :** después de resolver los conflictos, preparar los archivos resueltos usando git add <file>.
* **Complete la combinación :** después de preparar todos los archivos resueltos, complete la combinación con git commit.
## Ejemplo
Suponiendo que está en la rama main y fusionando la rama feature con ella:
```sh
    git checkout main
    git pull origin main
    git merge feature
```
Si hay conflictos, verá un resultado que indica los archivos con conflictos. Por ejemplo:
```sh
    Auto-merging file.txt
    CONFLICT (content): Merge conflict in file.txt
    Automatic merge failed; fix conflicts and then commit the result.
```

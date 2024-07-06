# Git Reflog
El reflog en Git es una característica que te permite ver el historial de cambios en los referentes de Git, como ramas y HEAD. Es una herramienta muy útil para recuperar commits perdidos y entender los movimientos recientes de tu repositorio. Cada vez que realizas una acción que afecta el historial de tu repositorio (como commit, checkout, merge, rebase, etc.), Git guarda una entrada en el reflog.

## Comandos Básicos de reflog
* Ver el reflog: ``git reflog``.

    Este comando muestra una lista de todos los movimientos y acciones que han cambiado el puntero de HEAD.

* Ver el reflog de una rama específica:
    ```sh
        git reflog show nombre_de_la_rama
    ```

    Muestra el reflog de la rama especificada.

* Resetear HEAD a un estado anterior usando reflog:
    ```sh
        git reset --hard HEAD@{n}
    ```

    Donde n es el índice de la entrada en el reflog a la que deseas volver.

## Ejemplo de Uso
Imagina que realizaste varios commits y, accidentalmente, hiciste un reset que eliminó algunos de ellos. Puedes usar el reflog para ver el historial de esos commits y recuperarlos.

* Comprobación del reflog:
    ```sh
        git reflog
    ```

    Esto puede mostrar algo como:

    ```sh
        5c6d7e3 (HEAD -> main) HEAD@{0}: reset: moving to HEAD~1
        8b9d3f2 HEAD@{1}: commit: Added new feature
        4e2a1b7 HEAD@{2}: commit: Fixed bug
        1a2c3e4 HEAD@{3}: commit: Initial commit
    ```
* Recuperación de un commit perdido:

    Supongamos que quieres recuperar el commit con el mensaje "Added new feature". Puedes resetear HEAD a ese commit específico usando su referencia en el reflog:
    ```sh
        git reset --hard HEAD@{1}
    ```
## Más Detalles sobre reflog
* Tiempo de Retención: 

    Por defecto, Git mantiene el reflog por 90 días para referencias de HEAD y por 30 días para referencias de otras ramas y remotos.
* Seguridad y Recuperación: 

    El reflog es una herramienta poderosa para la recuperación. Incluso si eliminas una rama, el reflog aún puede tener información sobre los commits recientes de esa rama, permitiéndote recuperar datos aparentemente perdidos.
## Usos Comunes del reflog
* Recuperar Cambios Perdidos: Si accidentalmente has hecho un reset o un checkout que ha hecho que pierdas commits, el reflog puede ayudarte a encontrar y restaurar esos commits.
* Auditar el Historial de Acciones: Puedes usar el reflog para ver una auditoría de las acciones que han cambiado el historial de tu repositorio.
* Depuración: Si algo ha salido mal y no estás seguro de lo que hiciste, el reflog puede ayudarte a rastrear tus pasos y entender lo que sucedió.
## Ejemplo Adicional
Si accidentalmente hiciste un git reset --hard y perdiste tu último commit, puedes usar el reflog para recuperarlo:
```sh
    git reflog
```
Supongamos que el reflog muestra lo siguiente:
```
    a1b2c3d (HEAD -> main) HEAD@{0}: reset: moving to HEAD~1
    e4f5g6h HEAD@{1}: commit: Added important feature
    i7j8k9l HEAD@{2}: commit: Fixed typo
    m0n1o2p HEAD@{3}: commit: Initial commit
```

Para volver al commit "Added important feature", puedes hacer:
```sh
    git reset --hard e4f5g6h
```

O usar el índice del reflog:
```sh
    git reset --hard HEAD@{1}
```

Esto restaurará tu repositorio al estado del commit "Added important feature".
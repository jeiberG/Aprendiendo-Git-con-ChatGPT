# ¿Qué es git reset?
git reset es un comando poderoso y potencialmente peligroso en Git que se utiliza para deshacer cambios en el índice **(staging area)** y en el historial de commits. Tiene varias modalidades que permiten diferentes niveles de deshacer cambios, desde simplemente quitar archivos del índice hasta mover el puntero de la rama actual a un commit específico y cambiar el árbol de trabajo (working directory).

## Funcionalidades de git reset
**1. Resetear el índice:** Remueve archivos del área de preparación sin afectar el árbol de trabajo.

**2. Resetear el índice y el árbol de trabajo:** Cambia el puntero de la rama actual a un commit específico y actualiza el índice y el árbol de trabajo.

**3.Resetear el historial de commits:** Deshace commits moviendo el puntero de la rama actual.

## Tipos de git reset
1. **--soft:** Mueve el puntero de la rama actual a un commit específico, pero mantiene los cambios en el índice y el árbol de trabajo.

2. **--mixed (por defecto):** Mueve el puntero de la rama actual a un commit específico y restablece el índice, pero mantiene los cambios en el árbol de trabajo.

3. **--hard:** Mueve el puntero de la rama actual a un commit específico y restablece tanto el índice como el árbol de trabajo.

## Uso básico de git reset
1. **Resetear el índice (--soft)**

```sh
    git reset --soft <commit>
```

Esto mantiene los cambios en el índice y el árbol de trabajo, pero mueve el puntero de la rama actual a ``<commit>``.

2. **Resetear el índice y el árbol de trabajo (--mixed)**

```sh
    git reset --mixed <commit>
```

Esto mueve el puntero de la rama actual a ``<commit>`` y restablece el índice, pero mantiene los cambios en el árbol de trabajo.

3. **Resetear el índice y el árbol de trabajo (--hard)**

```sh
    git reset --hard <commit>
```

Esto mueve el puntero de la rama actual a ``<commit>`` y restablece tanto el índice como el árbol de trabajo, perdiendo todos los cambios no confirmados.

## Ejemplos prácticos
Aquí hay algunos escenarios prácticos para entender mejor el uso de git reset:

**Ejemplo 1:** Deshacer un commit pero mantener los cambios en el índice y el árbol de trabajo
Imagina que has hecho un commit que quieres deshacer, pero mantener los cambios para hacer un nuevo commit:

```sh
    git reset --soft HEAD~1
```

**Ejemplo 2:** Quitar cambios del área de preparación pero mantenerlos en el árbol de trabajo
Si has añadido archivos al área de preparación y deseas quitarlos pero mantener los cambios:

```sh
    git reset
```

Este comando es equivalente a ``git reset --mixed HEAD``.

**Ejemplo 3:** Deshacer cambios no confirmados en el índice y el árbol de trabajo
Si has hecho cambios que deseas deshacer completamente, incluyendo los cambios no confirmados:

```sh
    git reset --hard HEAD
```

**Ejemplo 4:** Mover el puntero de la rama a un commit específico y deshacer todos los cambios desde entonces
Para mover la rama a un commit específico y deshacer todos los cambios desde ese commit:

```sh
    git reset --hard <commit>
```

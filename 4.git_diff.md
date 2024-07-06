# ¿Qué es git diff?
git diff es un comando en Git que muestra las diferencias entre commits, ramas, archivos y el árbol de trabajo. Es una herramienta esencial para revisar y entender los cambios en tu código antes de confirmarlos o para comparar diferentes versiones de tu proyecto.

## Funcionalidades de git diff
1. **Comparar el árbol de trabajo con el índice:** Muestra cambios no añadidos al área de preparación.
2. **Comparar el índice con el último commit:**
Muestra cambios añadidos al área de preparación pero no confirmados.
3. **Comparar el árbol de trabajo con el último commit:** Muestra todos los cambios no confirmados.
4. **Comparar dos commits específicos:** Muestra diferencias entre dos commits en el historial.
5. **Comparar dos ramas:** Muestra diferencias entre dos ramas en el repositorio.

## Uso básico de git diff
1. **Comparar el árbol de trabajo con el índice**

Para ver los cambios en el árbol de trabajo que aún no se han añadido al área de preparación:

```sh
    git diff
```

2. **Comparar el índice con el último commit**
Para ver los cambios que se han añadido al área de preparación pero no se han confirmado:

```sh
    git diff --staged
```

3. **Comparar el árbol de trabajo con el último commit**

Para ver todos los cambios no confirmados:

```sh
    git diff HEAD
```

4. **Comparar dos commits específicos**
Para ver las diferencias entre dos commits, usa sus hashes o referencias:

```sh
    git diff commit1 commit2
```

5. **Comparar dos ramas**
Para ver las diferencias entre dos ramas, usa sus nombres:

```sh
    git diff rama1 rama2
```

## Ejemplos prácticos
Aquí hay algunos escenarios prácticos para entender mejor el uso de git diff:

**Ejemplo 1:** Ver cambios no añadidos al área de preparación

Si has hecho cambios en ``archivo.txt`` pero no los has añadido al área de preparación:

```sh
    git diff archivo.txt
```

**Ejemplo 2:** Ver cambios añadidos al área de preparación

Si has añadido cambios en archivo.txt al área de preparación pero no los has confirmado:

```sh
    git add archivo.txt
    git diff --staged archivo.txt
```

**Ejemplo 3:** Ver todos los cambios no confirmados

Para ver todos los cambios en el árbol de trabajo y en el área de preparación:

```sh
    git diff HEAD
```

**Ejemplo 4:** Comparar dos commits específicos

Para comparar las diferencias entre dos commits específicos:

```sh
    git diff abc123 def456
```

**Ejemplo 5:** Comparar dos ramas

Para comparar las diferencias entre dos ramas:

```sh
    git diff main develop
```
## Opciones utiles de git ``diff``

**Ejemplo 1:** Ver cambios no confirmados en el árbol de trabajo
```sh
    git diff
```

**Ejemplo 2:** Ver cambios en el área de preparación
```sh
    git diff --staged
```

**Ejemplo 3:** Comparar dos commits específicos
```sh
    git diff abc123 def456
```

**Ejemplo 4:** Comparar dos ramas
```sh
    git diff main develop
```

**Ejemplo 5:** Ver diferencias en un archivo específico entre dos commits
```sh
    git diff abc123 def456 -- archivo.txt
```

**Ejemplo 6:** Ver un resumen de cambios
```sh
    git diff --stat
```

**Ejemplo 7:** Ver nombres de archivos modificados
```sh
    git diff --name-only
```

**Ejemplo 8:** Ver diferencias con 10 líneas de contexto
```sh
    git diff -U10
```

**Ejemplo 9:** Ver diferencias a nivel de palabras
```sh
    git diff --word-diff
```

**Ejemplo 10:** Ver diferencias ignorando cambios de espacios en blanco
```sh
    git diff --ignore-space-change
```

# ¿Qué es git restore?
El comando git restore se introdujo en Git 2.23 (agosto de 2019) y se utiliza para restaurar archivos de diferentes estados en el historial de Git. Este comando puede usarse para deshacer cambios en el árbol de trabajo (working directory) y en el índice (staging area).

## Funcionalidades de git restore
1. **Restaurar cambios en el árbol de trabajo:** 

    Deshace cambios no confirmados en un archivo.
2. **Restaurar cambios en el índice:** 

    Quita archivos del área de preparación (staging area) y los restaura a su estado en el historial de Git.
## Uso básico de git restore
1. **Restaurar un archivo a su última confirmación (commit)**

    Si has hecho cambios en un archivo pero no quieres conservarlos, puedes restaurar el archivo a su estado en el último commit:

    ```sh
        git restore nombre_del_archivo
    ```


2. **Restaurar un archivo en el área de preparación**

    Si has añadido un archivo al área de preparación y deseas deshacer eso, restaurando el archivo a su estado no modificado en el índice:

    ```sh
        git restore --staged nombre_del_archivo
    ```

3. **Restaurar un archivo de una confirmación específica**

    Puedes restaurar un archivo a su estado en un commit específico:

    ```sh
        git restore --source=<commit> nombre_del_archivo
    ```

4. **Restaurar todos los archivos en el árbol de trabajo**

    Si deseas deshacer todos los cambios no confirmados en todos los archivos:

    ```sh
        git restore .
    ```


## Ejemplos prácticos
Aquí hay algunos escenarios prácticos para entender mejor el uso de git restore:

**Ejemplo 1: Deshacer cambios no confirmados en un archivo**

Imagina que tienes un archivo main.c y has hecho algunos cambios que deseas deshacer:

```sh
    git restore main.c
```

**Ejemplo 2: Quitar un archivo del área de preparación**

Si has añadido un archivo index.html al área de preparación pero decides no confirmarlo aún:

```sh
   git restore --staged index.html
```

**Ejemplo 3: Restaurar un archivo a una versión específica de un commit**

Si necesitas restaurar un archivo styles.css a su estado en un commit específico con el hash abc123:

```sh
    git restore --source=abc123 styles.css
```

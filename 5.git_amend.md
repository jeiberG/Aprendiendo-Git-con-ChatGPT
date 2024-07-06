# ¿Qué es git commit --amend?
``git commit --amend`` es un comando en Git que permite modificar el último commit. Puedes usarlo para cambiar el mensaje del commit, agregar archivos olvidados o corregir errores en el contenido del commit más reciente. Es útil para hacer correcciones rápidas antes de que el commit sea enviado a un repositorio remoto.

## Funcionalidades de git commit --amend
* **Modificar el mensaje del último commit:** Cambia el mensaje asociado con el commit más reciente.
* **Agregar o quitar archivos del último commit:** Incluye archivos que se olvidaron agregar o elimina archivos que no debían estar en el commit.
* **Combinar cambios en un solo commit:** Permite combinar cambios adicionales con el commit más reciente.

## Uso básico de git commit --amend
**1. Modificar el mensaje del último commit
Si deseas cambiar el mensaje del último commit:**

```sh
    git commit --amend
```
Esto abrirá el editor de texto predeterminado, donde puedes modificar el mensaje del commit.

**2. Agregar archivos olvidados al último commit
Si olvidaste agregar archivos al último commit:**
```sh
    git add archivo_olvidado.txt
    git commit --amend
```
Esto incluirá el archivo añadido en el último commit y te permitirá modificar el mensaje del commit si es necesario.

**3. Eliminar archivos del último commit
Si un archivo fue añadido por error en el último commit, puedes eliminarlo y enmendar el commit:**

```sh
    git reset HEAD^ archivo_erroneo.txt
    git commit --amend
```

## Git Pull y Git Fetch

Git pull y Git fetch son dos comandos que se utilizan para actualizar un repositorio local con cambios desde un repositorio remoto, pero funcionan de maneras ligeramente diferentes:

## Git fetch
El git fetch comando se utiliza para descargar confirmaciones, archivos y referencias de un repositorio remoto a su repositorio local. Sin embargo, no fusiona estos cambios en su rama local. Esto le permite ver qué cambios están disponibles en el repositorio remoto antes de integrarlos en su trabajo. Así es como funciona:

* **Descargar actualizaciones** : git fetch descarga todos los datos nuevos del repositorio remoto que aún no tiene.
* **Sin fusión automática** : no fusiona ninguno de estos nuevos datos en sus archivos de trabajo. Tienes que fusionarlo manualmente si quieres.
* **Actualizaciones seguras** : es una forma segura de obtener actualizaciones sin afectar su trabajo actual.
## Ejemplo de comando:
```sh
    git fetch origin
```
Este comando obtiene actualizaciones del repositorio remoto llamado origin.

## Git Pull
* **El comando git pull es en realidad una combinación de dos comandos:** git fetch seguido de git merge. Cuando usas git pull, Git obtiene los cambios del repositorio remoto y luego intenta inmediatamente fusionar esos cambios en la rama en la que estás trabajando actualmente.

* **Obtener y combinar** : git pull descarga los nuevos datos del repositorio remoto y los integra directamente en su sucursal local.
* **Conflictos potenciales** : debido a que fusiona cambios automáticamente, es posible que enfrente conflictos que deban resolverse.
* **Actualizaciones rápidas** : es una forma rápida de actualizar su sucursal local con cambios desde el repositorio remoto.
## Ejemplo de comando:
```sh
    git pull origin main
```
Este comando obtiene actualizaciones del repositorio remoto nombrado origin y las fusiona en la main rama.

## Resumen
* **git fetch**: Descarga los cambios de un repositorio remoto pero no los fusiona automáticamente. Permite revisar los cambios antes de integrarlos.
* **git pull**:Descarga y fusiona inmediatamente los cambios desde un repositorio remoto en su rama actual.

Ambos comandos son útiles en diferentes escenarios. Úselo git fetch cuando desee ver qué cambios están disponibles antes de fusionarlos y úselo git pull cuando esté listo para integrar cambios remotos en su sucursal local.
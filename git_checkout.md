# ¿Qué es git checkout?

git checkout es un comando versátil en Git que se utiliza para cambiar ramas, restaurar archivos y commits específicos en el árbol de trabajo y en el índice (staging area). Aunque algunos de sus usos han sido reemplazados o complementados por **git switch** y **git restore**, sigue siendo una herramienta esencial en Git.

## Funcionalidades de git checkout

**Cambiar de rama:** Permite cambiar entre diferentes ramas en un repositorio.

**Crear y cambiar a una nueva rama:** Puedes crear una nueva rama y cambiarte a ella en un solo comando.

**Restaurar archivos o commits:**
Permite restaurar archivos a un estado específico o cambiar el árbol de trabajo a un commit específico.

## Uso básico de git checkout

**1. Cambiar de rama
Para cambiar a una rama existente, usa:**

```sh
    git checkout nombre_de_la_rama
```

**2. Crear y cambiar a una nueva rama
Para crear una nueva rama y cambiarte a ella inmediatamente:**

```sh
    git checkout -b nueva_rama
```

**3. Restaurar un archivo a su última confirmación (commit)**

Para deshacer los cambios no confirmados en un archivo y restaurarlo a su último estado confirmado:

```sh
    git checkout -- nombre_del_archivo
```

**4. Restaurar un archivo de un commit específico**

Para restaurar un archivo a su estado en un commit específico:

```sh
    git checkout <commit> -- nombre_del_archivo
```

**5. Cambiar el árbol de trabajo a un commit específico**

Para cambiar todo el árbol de trabajo a un commit específico (detached HEAD):

```sh
    git checkout <commit>
```

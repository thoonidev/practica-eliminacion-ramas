# Práctica de ramas en Git

Repositorio de aprendizaje para explorar ramas, cambios entre versiones y sincronización con un repositorio remoto. Utiliza pequeños scripts de Python que imprimen mensajes en consola.

## Contenido

- `master`: rama principal con `archivo1.py`, `archivo2.py`, `archivo3.py` y `archivo4.py`.
- `rama2`: rama con eliminación de `archivo1.py` y modificación de `archivo3.py`.
- Un commit en `master` incorpora `archivo4.py` para practicar `git fetch`.

## Requisitos

Git y, si deseas ejecutar los archivos, Python 3.

## Cómo practicar

```bash
git clone https://github.com/thoonidev/practica-eliminacion-ramas.git
cd practica-eliminacion-ramas
git branch -a
git log --all --oneline --graph --decorate
git diff master origin/rama2
```

Para revisar la rama alternativa y regresar a la principal:

```bash
git switch rama2
git switch master
```

Para actualizar las referencias remotas sin modificar tu rama de trabajo:

```bash
git fetch origin
```

## Eliminación de una rama local

Crea una rama temporal para practicar sin eliminar las ramas del ejercicio:

```bash
git branch rama-prueba
git branch -d rama-prueba
```

`git branch -d` elimina una rama local y evita borrar cambios que Git considera pendientes de integrar. No elimina la rama del repositorio remoto.

## Ejecutar un ejemplo

```bash
python archivo1.py
```

Los scripts son ejemplos independientes y no requieren bibliotecas adicionales.

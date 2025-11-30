# ⚡ Alias Esenciales para el Flujo de Trabajo

Este documento lista los alias de terminal más comunes y útiles para la navegación, manipulación de archivos y el flujo de trabajo básico con Git, diseñados para acelerar las tareas diarias.

---

## 🧭 Alias de Navegación y Archivos

Estos alias simplifican la visualización de archivos y el movimiento entre directorios.

|   Alias   | Comando Ejecutado |                                                Descripción                                                |             Ejemplo de Uso Sencillo              |
| :-------: | :---------------: | :-------------------------------------------------------------------------------------------------------: | :----------------------------------------------: |
|  **`l`**  |     `ls -lah`     | **Listar archivos** con detalle, incluyendo ocultos (`-a`), formato largo (`-l`) y tamaño legible (`-h`). |            `l` (Ver listado completo)            |
| **`ll`**  |     `ls -lh`      |             Listar archivos con formato largo y tamaño legible (no muestra archivos ocultos).             |           `ll` (Ver listado detallado)           |
| **`la`**  |     `ls -lAh`     |         Listar archivos, formato largo y legible, incluyendo ocultos, pero excluyendo `.` y `..`.         |                       `la`                       |
|  **`-`**  |      `cd -`       |                                 Volver al **último directorio** visitado.                                 |                       `-`                        |
| **`...`** |      `../..`      |                             **Subir dos niveles** de directorio rápidamente.                              | `cd components` y luego `...` (sube dos niveles) |
| **`md`**  |    `mkdir -p`     |                           **Crear un directorio** (y sus padres si no existen).                           |             `md proyectos/nuevo-app`             |
| **`gh`**  |   `cd ~/GitHub`   |               **Redirige** a la carpeta principal donde tienes tus repositorios de GitHub.                |                       `gh`                       |
|  **`_`**  |      `sudo `      |                      Ejecutar el siguiente comando con **permisos de superusuario**.                      |                  `_ apt update`                  |

---

## 🐍 Alias de Entorno Python (Tus Alias)

Estos alias fueron configurados para la gestión rápida y aislada de los entornos de Python (venv).

|      Alias       |           Comando Ejecutado           |                                    Descripción                                    |            Ejemplo de Uso Sencillo            |
| :--------------: | :-----------------------------------: | :-------------------------------------------------------------------------------: | :-------------------------------------------: |
|  **`pycreate`**  |        `python3 -m venv .venv`        |     **Crea** la carpeta del entorno virtual (`.venv`) en el proyecto actual.      |                  `pycreate`                   |
| **`pyactivate`** |      `source .venv/bin/activate`      |     **Activa** el entorno virtual para aislar las dependencias del proyecto.      | `pyactivate` (Verás `(.venv)` en tu _prompt_) |
|   **`ginit`**    | `cp ~/.gitignore_global ./.gitignore` | **Inicializa** el archivo `.gitignore` copiando tus reglas de exclusión globales. |                    `ginit`                    |

---

## 🐙 Alias Esenciales de Git

El alias `g=git` es la base para todos estos comandos. Dominar estos seis alias te permitirá realizar el ciclo de vida de cualquier _feature_.

|    Alias    |   Comando Ejecutado    |                                   Descripción                                   |   Ejemplo de Uso Sencillo    |
| :---------: | :--------------------: | :-----------------------------------------------------------------------------: | :--------------------------: |
|   **`g`**   |         `git`          |        El comando base. Úsalo como prefijo para todos los comandos Git.         |           `g help`           |
|  **`gst`**  |      `git status`      |  **Ver el estado** del repositorio (archivos modificados, en _staging_, etc.).  |            `gst`             |
|  **`ga`**   |       `git add`        |      **Añadir archivos** al _staging area_ (prepararlos para el _commit_).      |   `ga archivo.py` o `ga .`   |
|  **`gaa`**  |    `git add --all`     | **Añadir todos los archivos** al _staging area_ (prepararlos para el _commit_). |            `gaa`             |
|  **`gc`**   | `git commit --verbose` |         **Crear un _commit_**. Abre tu editor para escribir el mensaje.         |             `gc`             |
| **`gcmsg`** | `git commit --message` |          **Crear un _commit_**. abres commillas y escribes el mensaje.          | `gcmsg "mensaje del commit"` |
|  **`gl`**   |       `git pull`       |   **Descargar y fusionar** cambios desde el repositorio remoto (sincronizar).   |             `gl`             |
|  **`gp`**   |       `git push`       |             **Subir** tus _commits_ locales al repositorio remoto.              |             `gp`             |

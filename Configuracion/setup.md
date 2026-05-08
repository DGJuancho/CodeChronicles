# 💻 Configuración del Entorno de Desarrollo (WSL/Windows)

Este documento registra los pasos y herramientas esenciales instaladas para configurar mi entorno de desarrollo. La infraestructura se ejecuta en **WSL (Ubuntu)** para los entornos de ejecución, mientras que los IDEs y herramientas gráficas se ejecutan en el sistema operativo host (Windows), interconectados vía Desarrollo Remoto/Gateway.

---

## 🛠️ Herramientas Instaladas en WSL (Ubuntu)

### 1. Sistema Operativo y Utilidades Base

| Categoría      | Detalle                        | Comandos de Instalación/Actualización |
| :------------- | :----------------------------- | :------------------------------------ |
| **Sistema**    | Actualización de paquetes base | sudo apt update && sudo apt upgrade   |
| **Utilidades** | Herramientas de red y descarga | sudo apt install curl wget            |

### 2. Configuración del Shell (Zsh)

Personalización de la línea de comandos para mejorar la productividad y la estética.

| Componente     | Detalle                                            | Comandos Clave                        |
| :------------- | :------------------------------------------------- | :------------------------------------ |
| **Shell Base** | Zsh (instalado y configurado)                      |                                       |
| **Framework**  | Oh My Zsh                                          |                                       |
| **Fuente**     | MeslowLGS NF                                       |                                       |
| **Tema**       | Power10k (o el tema de shell utilizado)            |                                       |
| **Plugins**    | Autosuggestions, Syntax Highlighting, Autocomplete | git clone ... (comandos de clonación) |

### 3. Lenguajes de Programación y SDKs

| Lenguaje   | Versión Instalada | Paquetes Clave             | Comando de Instalación (apt)                      |
| :--------- | :---------------- | :------------------------- | :------------------------------------------------ |
| **Python** | 3.12.3 / Pip 24.0 | python3, pip, python3-venv | sudo apt install python3 python3-pip python3-venv |
| **Java**   | OpenJDK 17 (LTS)  | openjdk-17-jdk             | sudo apt install openjdk-17-jdk                   |

### 4. Bases de Datos y Clientes

| Herramienta | Tipo            | Ubicación | Comando de Instalación (apt)     |
| :---------- | :-------------- | :-------- | :------------------------------- |
| **MySQL**   | Servidor DB     | WSL       | sudo apt install mysql-server    |
| **PostgreSQL** | Servidor DB/ | WSL       | sudo apt install postgresql postgresql-contrib         |
| **SQLite3** | Servidor DB/CLI | WSL       | sudo apt install sqlite3         |
| **DBeaver** | Cliente Gráfico | WSLg      | Instalado y ejecutándose en WSLg |

---

## ⚙️ Herramientas de Productividad (Windows Host)

| Herramienta       | Función                 | Configuración con WSL                                        |
| :---------------- | :---------------------- | :----------------------------------------------------------- |
| **VSCode**        | Editor principal        | Usa Extensión WSL para backend en Ubuntu (Settings Sync).    |
| **IntelliJ IDEA** | IDE principal para Java | Usa Remote Development Gateway para acceder a JDK 17 de WSL. |

---

## 🔑 Configuración de Git/SSH (WSL)

| Componente    | Detalle                           | Comandos de Configuración (Ejemplo)             |
| :------------ | :-------------------------------- | :---------------------------------------------- |
| **Git**       | Configurado en WSL (preinstalado) | git config --global user.name "..."             |
| **SSH**       | Llave ed25519 para GitHub         | ssh-keygen -t ed25519 -C "tu_email@ejemplo.com" |
| **SSH Agent** | Inicio automático y `ssh-add`     | eval "$(ssh-agent -s)"                          |

## 🚀 Alias de Terminal (Flujo de Trabajo Rápido)

Para acelerar el inicio de proyectos Python y la gestión de dependencias, se han configurado los siguientes alias en el archivo de configuración del shell (`~/.zshrc` o `~/.bashrc`).

|    Alias     |           Comando Ejecutado           |                                                       Descripción                                                       |
| :----------: | :-----------------------------------: | :---------------------------------------------------------------------------------------------------------------------: |
|     `gh`     |             `cd ~/GitHub`             |                            **Redirige** al contenedorde los repositorio de proyectos GitHub                             |
|  `pycreate`  |        `python3 -m venv .venv`        | **Crea** la carpeta del entorno virtual (`.venv`) en el directorio actual. Usar solo en la inicialización del proyecto. |
| `pyactivate` |      `source .venv/bin/activate`      |                           **Activa** el entorno virtual para usar las dependencias aisladas.                            |
|   `ginit`    | `cp ~/.gitignore_global ./.gitignore` |                      Inicializa el archivo `.gitignore` copiando las reglas de exclusión globales.                      |

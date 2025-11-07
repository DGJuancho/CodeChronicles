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

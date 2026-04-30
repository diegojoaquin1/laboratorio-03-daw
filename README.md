# 📅 Agenda Personal - Laboratorio 03 (DAW)

Este proyecto es una aplicación web de administración de eventos desarrollada con **Node.js** y **Express**, diseñada para ser ejecutada de manera portátil y consistente mediante **Docker**. El laboratorio cumple con los objetivos de despliegue y gestión de servidores web estipulados en la guía de práctica.

## 🚀 Características Principales
- **Arquitectura REST**: API para crear, listar, editar y eliminar eventos.
- **Persistencia en Markdown**: Los eventos se guardan físicamente en el servidor organizados por fecha y hora.
- **Contenedorización**: Configuración completa con Docker para evitar problemas de dependencias locales.
- **Interfaz Web**: Frontend dinámico que consume la API del servidor..

---

## 📂 Estructura del Proyecto

El proyecto está organizado siguiendo el principio de separación de responsabilidades:

```text
lab-03-daw/
├── agenda/             # Almacenamiento persistente de eventos (.md)
├── pub/                # Archivos estáticos servidos al cliente
│   ├── css/            # Estilos visuales
│   ├── js/             # Lógica del frontend (agenda.js)
│   └── index.html      # Interfaz de usuario principal
├── app.js              # Servidor principal y definición de API Express
├── Dockerfile          # Instrucciones para construir la imagen Docker
├── .dockerignore       # Archivos excluidos del contenedor (node_modules)
├── package.json        # Dependencias del proyecto (Express)
└── package-lock.json   # Registro de versiones exactas
```

## 🐳 Despliegue con Docker

Sigue estos pasos para construir y ejecutar la aplicación en un contenedor aislado:

### 1. Construcción de la Imagen
Desde la raíz del proyecto (donde se encuentra el `Dockerfile`), ejecuta el siguiente comando para compilar la imagen:
```bash
docker build -t lab03-agenda .
```
## 📸 Demostración de Funcionamiento

### 1. Creación de Tareas
Para probar el sistema, se crearon tres tareas de ejemplo mediante la interfaz web:
![Creación de tareas](./img/creacion_tareas.jpeg)

### 2. Persistencia en el Servidor
Se puede observar cómo Docker crea los archivos `.md` dentro de la carpeta `agenda/` automáticamente:
![Archivos generados](./img/carpetas_agendas.png)

### 3. Eliminación de Tareas
Al presionar el botón de eliminar, el sistema borra los archivos físicos del contenedor:
![Eliminación de tareas](./img/eliminacion_tareas.png)

## 📺 Demostración en Video del proyecto del presente laboratorio
Para una explicación detallada del funcionamiento, el despliegue en Docker y la estructura del proyecto, puedes ver el siguiente video:

[![Demostración del Proyecto](https://img.youtube.com/vi/40_GmMuA1Ms/0.jpg)](https://www.youtube.com/watch?v=40_GmMuA1Ms)

> **Nota:** Haz clic en la imagen de arriba para reproducir el video en YouTube.

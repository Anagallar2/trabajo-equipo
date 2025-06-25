---
title: Apuntes 25/06/25
created: '2025-06-25T06:31:00.137Z'
modified: '2025-06-25T07:58:23.873Z'
---

# Apuntes 25/06/25

# 🐳 Docker: Concepto, características y comandos

## 📘 ¿Qué es Docker?

**Docker** es una plataforma que permite empaquetar una aplicación con todas sus dependencias en un **contenedor**, garantizando que funcione igual en cualquier entorno.  
Es rápido, ligero y facilita el desarrollo, despliegue y escalado de software.

---

## 🚀 Características de Docker

- **Portabilidad**: Los contenedores se ejecutan igual en cualquier sistema con Docker.
- **Aislamiento**: Cada contenedor funciona de forma independiente.
- **Eficiencia**: Más ligeros y rápidos que las máquinas virtuales.
- **Escalabilidad**: Ideal para microservicios y despliegues masivos.
- **Reproducibilidad**: La aplicación se comporta siempre igual.
- **Rapidez**: Los contenedores inician en segundos.

---

## 🛠️ Herramientas relacionadas

- **Docker Engine**: Motor principal que ejecuta los contenedores.
- **Docker Compose**: Define y gestiona múltiples contenedores con archivos YAML.
- **Docker Hub**: Repositorio para compartir y descargar imágenes.
- **Docker CLI**: Línea de comandos para gestionar Docker.
- **Kubernetes**: Orquestación de contenedores a gran escala (complementario a Docker).

---

## 🧪 Ejemplos de comandos con Docker

### 🔍 Verificar instalación

## 🧪 Comandos básicos de Docker

```bash
# Verificar la versión de Docker instalada
docker --version

# Descargar una imagen (por ejemplo, nginx)
docker pull nginx

# Crear y ejecutar un contenedor en segundo plano, mapeando puertos y con nombre
docker run -d -p 8080:80 --name mi-nginx nginx

# Ver contenedores activos
docker ps

# Ver todas las imágenes descargadas localmente
docker images

# Detener un contenedor por nombre o ID
docker stop mi-nginx

# Eliminar un contenedor por nombre o ID
docker rm mi-nginx

# Construir una imagen Docker desde un Dockerfile en el directorio actual
docker build -t mi-imagen .

# Limpiar contenedores detenidos, imágenes sin uso, redes y caché
docker system prune

# Esquema estructura de proyecto Docker


      mi-proyecto/
      │
      ├── Dockerfile # Archivo con instrucciones para construir la imagen Docker
      │
      ├── docker-compose.yml # (Opcional) Archivo para orquestar múltiples contenedores
      │
      ├── app/ # Carpeta con código fuente de la aplicación
      │ ├── main.py # (Ejemplo) Archivo principal de la app
      │ └── requirements.txt # (Ejemplo) Dependencias si usas Python
      │
      └── README.md # Documentación del proyecto







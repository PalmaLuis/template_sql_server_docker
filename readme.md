# SQL Server Docker Setup

Este proyecto proporciona un entorno Dockerizado para ejecutar SQL Server, ideal para entornos de desarrollo y pruebas.

## Descripción

Este archivo `docker-compose.yml` define un servicio Docker para ejecutar una instancia de SQL Server 2022. Incluye configuraciones básicas de autenticación y persistencia de datos en volúmenes locales.

## Requisitos previos

- [Docker](https://www.docker.com/products/docker-desktop) (versión 3.8 o superior)
- [Docker Compose](https://docs.docker.com/compose/) 

## Uso

### 1. Clonar el repositorio

```bash
git clone git@github.com:PalmaLuis/template_sql_server_docker.git
cd sql_server_docker_compose
```

### 2. Configuracion de contraseña
Por seguridad, actualiza la contraseña de administrador de SQL Server en el archivo `docker-compose.yml` en la sección:
```bash
environment:
  - MSSQL_SA_PASSWORD=tu_contraseña_segura
```

### 3. Iniciar el contenedor
```bash
    docker-compose up -d
```

### 4. Conectar a SQL Server
Puedes conectar cualquier cliente SQL Server al contenedor, usando las siguientes credenciales de ejemplo:

* Host: localhost,1433
* Usuario: sa
* Contraseña: La contraseña especificada en MSSQL_SA_PASSWORD

### Estructura de volúmenes
* ./data - Almacena los archivos de la base de datos.
* ./backups - Almacena los archivos de respaldo de la base de datos.
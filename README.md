# Proyecto de Migración de Datos con API REST

Este proyecto permite cargar datos históricos desde archivos CSV a una base de datos utilizando una API REST. Soporta la inserción de datos en las tablas `departments`, `jobs` y `employees`, y permite la inserción de transacciones en lote.

---

## Tabla de Contenidos

1. [Requisitos](#requisitos)
2. [Instalación](#instalación)
3. [Configuración](#configuración)
4. [Estructura del Proyecto](#estructura-del-proyecto)
5. [Endpoints de la API](#endpoints-de-la-api)
6. [Contribución](#contribución)
7. [Licencia](#licencia)

---

## Requisitos

Para ejecutar este proyecto, necesitas:

- Python 3.8 o superior.
- Las siguientes librerías de Python:
  - Flask
  - SQLAlchemy
  - Pandas

---

## Instalación

1. Clona este repositorio:
   ```bash
   git clone https://github.com/tu-usuario/proyecto-migracion.git
   cd proyecto-migracion

2. Instala las dependencias corriendo el siguiente código: 
    -- pip install -r requirements.txt
3. Configurar: 
Base de datos:

El proyecto utiliza SQLite por defecto. La base de datos se creará automáticamente en el archivo migration.db.
Puedes cambiar el nombre, estructura y ruta del archivo adaptandolo a tus necesidades.

Si deseas usar otra base de datos, modifica la variable DATABASE_URI en db_params.py.

Archivos CSV:

Asegúrate de que los archivos CSV tengan el formato correcto para cada tabla:

departments.csv: id,department

jobs.csv: id,job

employees.csv: name,datetime,department_id,job_id

4. Estructura:
├── app.py                                # Código principal de la API
├── db_params.py                          # Creación de las bases de datos
├── requirements.txt                      # Dependencias del proyecto
├── README.md                             # Este archivo
├── api_testing.postman_collection.json   # Archivo para realizar el testeo del API
└── data/                                 # Carpeta para almacenar archivos CSV (opcional)
5. Endpoints de la API:
Se toma como ejemplo un endpoint creado localmente para realizar el ejercicio, se recomienda cambiar a un end point productivo con protocolos de seguridad para su uso correcto.

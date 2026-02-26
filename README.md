# DevOps Capstone Project

![Build Status](https://github.com/AddOn2394/devops-capstone-project/actions/workflows/ci-build.yaml/badge.svg)
[![License](https://img.shields.io/badge/License-Apache%202.0-blue.svg)](https://opensource.org/licenses/Apache-2.0)
[![Python 3.9](https://img.shields.io/badge/Python-3.9-green.svg)](https://shields.io/)
[![Flask](https://img.shields.io/badge/Flask-2.x-lightgrey.svg)](https://flask.palletsprojects.com/)
[![Docker](https://img.shields.io/badge/Docker-ready-blue.svg)](https://www.docker.com/)
[![OpenShift](https://img.shields.io/badge/OpenShift-Kubernetes-red.svg)](https://www.redhat.com/en/technologies/cloud-computing/openshift)

Este repositorio contiene el código necesario para completar el proyecto **"DevOps Capstone Project"** del curso [**IBM-CD0285EN-SkillsNetwork DevOps Capstone Project**](https://www.coursera.org/learn/devops-capstone-project?specialization=devops-and-software-engineering), que es parte del certificado profesional [**IBM DevOps and Software Engineering Professional Certificate**](https://www.coursera.org/professional-certificates/devops-and-software-engineering).

---

## 📋 Descripción

Este proyecto implementa un microservicio de **gestión de cuentas de clientes** para una tienda en línea, permitiendo realizar todas las operaciones CRUD (Crear, Leer, Actualizar, Eliminar) a través de una **RESTful API** desarrollada con Flask.

A lo largo del proyecto se aplican prácticas modernas de DevOps, incluyendo desarrollo ágil, integración y entrega continua (CI/CD), contenedorización y despliegue en la nube.

---

## 🗂️ Módulos del Proyecto

### Módulo 1 — Planificación Ágil
- Creación del repositorio GitHub y tablero Kanban
- Definición de historias de usuario (User Stories)
- Configuración del Product Backlog y Sprint Backlog con estimación de story points

### Módulo 2 — Sprint 1: Desarrollo con TDD
- Configuración del entorno de desarrollo
- Implementación del microservicio usando **Test-Driven Development (TDD)**
- Escritura de casos de prueba para operaciones CRUD (leer, actualizar, eliminar, listar)
- Ejecución de **nosetests** con cobertura mínima del **95%**
- Gestión de ramas y pull requests en GitHub

### Módulo 3 — Sprint 2: CI y Seguridad
- Configuración de un flujo de **GitHub Actions** para integración continua (CI)
  - Linting con **Flake8**
  - Ejecución de pruebas y validación de cobertura
- Implementación de prácticas de codificación segura:
  - **Flask-Talisman** para cabeceras de seguridad
  - **Flask-CORS** para políticas de Cross-Origin Resource Sharing

### Módulo 4 — Sprint 3: Despliegue en la Nube
- Creación del **Dockerfile** y construcción de imagen Docker
- Publicación de la imagen en **IBM Cloud Container Registry**
- Despliegue manual en un clúster **OpenShift/Kubernetes**
- Configuración de servicio **PostgreSQL** en OpenShift
- Escritura de manifiestos YAML (Deployment y Service)

### Módulo 5 — Pipeline de Entrega Continua (CD)
- Creación de un pipeline **Tekton** para automatizar el despliegue
  - Clonado del repositorio
  - Linting y pruebas
  - Construcción y publicación de imagen Docker
  - Despliegue automático al clúster Kubernetes

### Módulo 6 — Recolección de Evidencias
- Capturas de pantalla, URLs de GitHub y outputs de laboratorios para evaluación final

### Módulo 7 — Examen Final
- Validación de conocimientos en DevOps aplicados durante el proyecto

---

## 🛠️ Tecnologías Utilizadas

| Categoría | Tecnología |
|---|---|
| Lenguaje | Python 3.9 |
| Framework | Flask |
| Base de datos | PostgreSQL |
| Pruebas | Nosetests, Coverage |
| Calidad de código | Flake8 |
| Seguridad | Flask-Talisman, Flask-CORS |
| CI/CD | GitHub Actions, Tekton |
| Contenedores | Docker |
| Orquestación | Kubernetes / OpenShift |
| Registro de imágenes | IBM Cloud Container Registry |
| Gestión de proyecto | GitHub Kanban Board |

---

## 🚀 Instalación y Ejecución Local

```bash
# Clonar el repositorio
git clone https://github.com/<tu-usuario>/devops-capstone-project.git
cd devops-capstone-project

# Instalar dependencias
pip install -r requirements.txt

# Ejecutar la aplicación
flask run
```

---

## 🧪 Ejecutar Pruebas

```bash
# Ejecutar pruebas con cobertura
nosetests --with-coverage --cover-package=service
```

---

## 🐳 Ejecutar con Docker

```bash
# Construir la imagen
docker build -t customer-accounts .

# Ejecutar el contenedor
docker run -p 8080:8080 customer-accounts
```

---

## 📁 Estructura del Proyecto

```
devops-capstone-project/
├── service/                  # Código principal del microservicio
│   ├── __init__.py
│   ├── models.py             # Modelos de datos
│   └── routes.py             # Endpoints de la API
├── tests/                    # Casos de prueba
│   └── test_routes.py
├── .github/
│   └── workflows/            # GitHub Actions CI/CD
├── k8s/                      # Manifiestos Kubernetes
│   ├── deployment.yaml
│   └── service.yaml
├── Dockerfile
├── requirements.txt
└── README.md
```

---

## 📄 Licencia

Este proyecto está licenciado bajo la [Apache License 2.0](https://opensource.org/licenses/Apache-2.0).

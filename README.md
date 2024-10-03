# Test Web App - A2O Dev 2024

This project is a full-stack web application developed as a technical test for Web App Developers. It includes a Django-based API as the backend (`problems_api`) and a React-based frontend (`problems-frontend`). The goal is to solve two specific problems (Chess Queen attack and String Value) by creating a responsive, user-friendly interface that interacts with a backend API.

## Project Structure
```bash
test-webapp/ 
├── problems_api/ # Backend (Django API) 
│ ├── manage.py 
│ ├── requirements.txt # Python dependencies 
│ └── problems/ # Main Django application 
├── problems-frontend/ # Frontend (React) 
│ ├── package.json # Node dependencies 
│ └── src/ # React components and pages 
├── .gitignore 
└── README.md # This file
```

## Prerequisites

Make sure you have the following installed on your system:

- **Python 3.x** (preferably 3.8 or later)
- **Node.js** (preferably v16 or later) and npm
- **Virtualenv** for Python
- **Git**

## Backend Setup (Django API)

### Step 1: Create a Python Virtual Environment

Navigate to the `problems_api` folder:

```bash
cd problems_api
```
Create a virtual environment:
- On Linux/macOS:
  ```bash
  source venv/bin/activate
  ```
- On Windows:
  ```bash
  venv\Scripts\activate
   ```
### Step 2: Install Dependencies
Once the virtual environment is active, install the necessary dependencies using `requirements.txt`:
```bash
pip install -r requirements.txt
```
### Step 3: Run Django Migrations
Apply the migrations to set up the structure:
```bash
python manage.py migrate
```
### Step 4: Run the Backend Server
To start the Django development server, run:
```bash
python manage.py runserver
```
The Django API will be available at `http://localhost:8000`.

## Frontend Setup (React)
### Step 1: Install Node.js Dependencies
Navigate to the `problems-frontend` folder:
### Step 2: Run the Frontend Development Server
Start the React development server:
```bash
npm start
```
The React application will be available at `http://localhost:3000` and will communicate with the Django backend via API.

## CORS Configuration
To allow communication between the frontend (React) and the backend (Django API), CORS is enabled in the Django project.

Ensure that in `settings.py` of your Django project (`problems_api/problems/`), you have configured the allowed origins as follows:

```python
# settings.py
CORS_ALLOWED_ORIGINS = [
    "http://localhost:3000",
]
```
This allows requests from the React development server to access the Django API.

## Running the Project
### Step 1: Start the Backend Server (Django API)
In a terminal, navigate to the `problems_api` folder and run:
```bash
python manage.py runserver
```
### Step 2: Start the Frontend Server (React)
In a separate terminal, navigate to the `problems-frontend` folder and run:

```bash
npm start
```
Both the frontend and backend servers should now be running. The frontend will be accessible at `http://localhost:3000`, and the API will be available at `http://localhost:8000`.

## API Endpoints
The following endpoints are available for each problem:

### 1. Chess Queen Attack Calculation:

- Endpoint: `/api/problem-1/`
- Method: POST
- Request Payload:
  ```json
  {
    "n": 4,
    "k": 0,
    "rq": 4,
    "cq": 4,
    "obstacles": []
  }
  ```
### 2. String Value Calculation:

- Endpoint: `/api/problem-2/`
- Method: POST
- Request Payload:
  ```json
  {
    "string": "abcabcddd"
  }
  ```



## Plantilla de Documentación de Soporte y Uso de herramientas digitales - README.md
Esta es una plantilla basada en los estándares de la Guía de publicacion de herramientas digitales del BID. Sabemos que no existe un solo estándar para la documentación de soporte y uso de herramientas digitales pero hemos recopilado estas características importantes que debe tener un readme.md para facilitar el uso y amplificar el potencial de impacto de las mismas. Cualquier comentario o recomendación les pedimos generar un issue de consulta o escribirnos directamente a code@iadb.org.

## La plantilla empieza aquí 👇


*Esta herramienta digital forma parte del catálogo de herramientas del **Banco Interamericano de Desarrollo**. Puedes conocer más sobre la iniciativa del BID en [code.iadb.org](https://code.iadb.org)*

<h1 align="center">Nombre de la herramienta</h1>
<p align="center"> Logo e imagen o gif de la interfaz principal de la herramienta</p>
<p align="center"><img src="https://www.webdevelopersnotes.com/wp-content/uploads/create-a-simple-home-page.png"/></p> 

## Tabla de contenidos:
---

- [Badges o escudos](#badges-o-escudos)
- [Descripción y contexto](#descripción-y-contexto)
- [Guía de usuario](#guía-de-usuario)
- [Guía de instalación](#guía-de-instalación)
- [Cómo contribuir](#cómo-contribuir)
- [Código de conducta](#código-de-conducta)
- [Autor/es](#autores)
- [Información adicional](#información-adicional)
- [Licencia](#licencia)
- [Limitación de responsabilidades - Solo BID](#limitación-de-responsabilidades)

## Badges o escudos
---
Es común en muchos repositorios open source el uso de badges o escudos para dar visbilidad el uso de microservicios, licencias, descargas, etc. Recomendamos revisar la iniciativa https://shields.io/ donde según consideres necesario podrás generar badges para tu repo. 

### Ejemplos de badges

- code coverage percentage: ![coverage](https://img.shields.io/badge/coverage-80%25-yellowgreen)
- stable release version: ![version](https://img.shields.io/badge/version-1.2.3-blue)
- package manager release: ![gem](https://img.shields.io/badge/gem-2.2.0-blue)
- status of third-party dependencies: ![dependencies](https://img.shields.io/badge/dependencies-out%20of%20date-orange)
- static code analysis grade: ![codacy](https://img.shields.io/badge/codacy-B-green)
- [SemVer](https://semver.org/) version observance: ![semver](https://img.shields.io/badge/semver-2.0.0-blue)
- amount of [Liberapay](https://liberapay.com/) donations per week: ![receives](https://img.shields.io/badge/receives-2.00%20USD%2Fweek-yellow)
- Python package downloads: ![downloads](https://img.shields.io/badge/downloads-13k%2Fmonth-brightgreen)
- Chrome Web Store extension rating: ![rating](https://img.shields.io/badge/rating-★★★★☆-brightgreen)
- [Uptime Robot](https://uptimerobot.com) percentage: ![uptime](https://img.shields.io/badge/uptime-100%25-brightgreen)

### Badges que solicitamos:
---

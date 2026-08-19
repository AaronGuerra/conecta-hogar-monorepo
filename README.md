<h1 align="center">🏡 Conecta Hogar</h1>

<p align="center">
  <img width="180" alt="Conecta Hogar" src="https://github.com/user-attachments/assets/b37cbc69-3681-4d0e-8096-198e8ff5dc0d" />
</p>

<p align="center">
  Plataforma web Full Stack que conecta personas que necesitan servicios para el hogar con profesionales especializados.
</p>

<p align="center">
  <strong>Monorepo · Frontend + Backend · API REST · Autenticación JWT</strong>
</p>

---

<h2 align="center">💻 Stack Tecnológico</h2>

<h3 align="center">Frontend</h3>

<p align="center">
  <img src="https://img.shields.io/badge/React-18+-61DAFB?style=for-the-badge&logo=react&logoColor=black" alt="React" />
  <img src="https://img.shields.io/badge/TypeScript-5+-3178C6?style=for-the-badge&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Vite-6+-646CFF?style=for-the-badge&logo=vite&logoColor=white" alt="Vite" />
  <img src="https://img.shields.io/badge/React_Router-7+-CA4245?style=for-the-badge&logo=react-router&logoColor=white" alt="React Router" />
  <img src="https://img.shields.io/badge/Material_UI-7+-007FFF?style=for-the-badge&logo=mui&logoColor=white" alt="Material UI" />
  <img src="https://img.shields.io/badge/Tailwind_CSS-4+-06B6D4?style=for-the-badge&logo=tailwindcss&logoColor=white" alt="Tailwind CSS" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Motion-Animations-000000?style=for-the-badge&logo=framer&logoColor=white" alt="Motion" />
  <img src="https://img.shields.io/badge/Lucide_React-Icons-F56565?style=for-the-badge&logo=lucide&logoColor=white" alt="Lucide React" />
  <img src="https://img.shields.io/badge/HTML5-E34F26?style=for-the-badge&logo=html5&logoColor=white" alt="HTML5" />
  <img src="https://img.shields.io/badge/CSS3-1572B6?style=for-the-badge&logo=css3&logoColor=white" alt="CSS3" />
</p>

<h3 align="center">Backend</h3>

<p align="center">
  <img src="https://img.shields.io/badge/Java-17+-ED8B00?style=for-the-badge&logo=openjdk&logoColor=white" alt="Java" />
  <img src="https://img.shields.io/badge/Spring_Boot-3+-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white" alt="Spring Boot" />
  <img src="https://img.shields.io/badge/Spring_Security-JWT-6DB33F?style=for-the-badge&logo=spring-security&logoColor=white" alt="Spring Security" />
  <img src="https://img.shields.io/badge/Apache_Maven-C71A36?style=for-the-badge&logo=apache-maven&logoColor=white" alt="Apache Maven" />
  <img src="https://img.shields.io/badge/Hibernate-59666C?style=for-the-badge&logo=hibernate&logoColor=white" alt="Hibernate" />
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Spring_Data_JPA-6DB33F?style=for-the-badge&logo=spring&logoColor=white" alt="Spring Data JPA" />
  <img src="https://img.shields.io/badge/Lombok-BC4521?style=for-the-badge&logo=lombok&logoColor=white" alt="Lombok" />
  <img src="https://img.shields.io/badge/MapStruct-DTO_Mapping-FF6B35?style=for-the-badge" alt="MapStruct" />
  <img src="https://img.shields.io/badge/REST_API-JSON-000000?style=for-the-badge" alt="REST API" />
</p>

<h3 align="center">Base de Datos y Herramientas</h3>

<p align="center">
  <img src="https://img.shields.io/badge/NEON-Database-00E699?style=for-the-badge&logo=postgresql&logoColor=black" alt="NEON Database" />
  <img src="https://img.shields.io/badge/Git-F05032?style=for-the-badge&logo=git&logoColor=white" alt="Git" />
  <img src="https://img.shields.io/badge/GitHub-181717?style=for-the-badge&logo=github&logoColor=white" alt="GitHub" />
</p>

---

<h2 align="center">📌 Descripción</h2>

**Conecta Hogar** es una aplicación web desarrollada como proyecto Full Stack, cuyo objetivo es facilitar la búsqueda y gestión de profesionales que ofrecen servicios para el hogar.

El proyecto integra un **frontend desarrollado con React + TypeScript** y un **backend desarrollado con Java + Spring Boot**, comunicados mediante una API REST.

La aplicación está organizada como un **monorepo**, centralizando el frontend y el backend en un mismo repositorio para facilitar el desarrollo, integración y mantenimiento del proyecto.

### Principales funcionalidades

* 🔐 Registro e inicio de sesión de usuarios.
* 🛡️ Autenticación y autorización mediante JWT.
* 👷 Gestión y consulta de profesionales.
* ⭐ Sistema de valoraciones.
* 🖼️ Carga y actualización de imágenes.
* 🔎 Consulta de profesionales mejor valorados.
* 📱 Interfaz responsive.
* 🔗 Comunicación mediante API REST.
* 🧩 Componentes reutilizables en React.
* 🗂️ Arquitectura organizada por capas en el backend.

---

<h2 align="center">🏗️ Arquitectura</h2>

El proyecto está dividido en dos aplicaciones principales:

```text
conecta-hogar-monorepo/
│
├── backend/                 # API REST - Java + Spring Boot
│   ├── src/
│   ├── uploads/
│   ├── .mvn/
│   ├── pom.xml
│   ├── mvnw
│   └── mvnw.cmd
│
├── frontend/                # Aplicación web - React + TypeScript
│   ├── src/
│   ├── package.json
│   ├── vite.config.ts
│   ├── tailwind.config.js
│   └── tsconfig.json
│
├── .gitignore
└── README.md
```

### Flujo general

```text
                    ┌─────────────────────┐
                    │       Usuario       │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │  React + TypeScript │
                    │       Frontend      │
                    └──────────┬──────────┘
                               │
                           HTTP / JSON
                               │
                               ▼
                    ┌─────────────────────┐
                    │    Spring Boot      │
                    │      REST API       │
                    └──────────┬──────────┘
                               │
                    ┌──────────▼──────────┐
                    │     Spring Data     │
                    │     JPA / Hibernate │
                    └──────────┬──────────┘
                               │
                               ▼
                    ┌─────────────────────┐
                    │      NEON DB        │
                    │    PostgreSQL       │
                    └─────────────────────┘
```

---

<h2 align="center">📂 Estructura del Backend</h2>

El backend utiliza una **arquitectura en capas**, separando responsabilidades entre controladores, servicios, repositorios, modelos, DTOs y componentes de seguridad.

```text
backend/
└── src/
    └── main/
        ├── java/
        │   └── com/example/conecta_hogar/
        │       ├── auth/
        │       ├── config/
        │       ├── controller/
        │       ├── dto/
        │       ├── mapper/
        │       ├── model/
        │       ├── repository/
        │       ├── security/
        │       ├── service/
        │       └── ConectaHogarApplication.java
        │
        └── resources/
            └── application.yaml
```

### Flujo de una petición

```text
Controller
    ↓
Service
    ↓
Repository
    ↓
Database
```

Esta separación permite mantener la lógica de negocio aislada de la exposición de los endpoints y del acceso a los datos.

---

<h2 align="center">📂 Estructura del Frontend</h2>

El frontend utiliza una arquitectura basada en componentes reutilizables y separación entre páginas, servicios, rutas, hooks y tipos.

```text
frontend/
└── src/
    ├── assets/
    │   ├── images/
    │   ├── icons/
    │   └── styles/
    │
    ├── components/
    │   ├── Navbar/
    │   ├── Footer/
    │   ├── Cards/
    │   └── UI/
    │
    ├── pages/
    │   ├── Home/
    │   ├── Login/
    │   ├── Register/
    │   ├── Services/
    │   ├── Contact/
    │   └── Profile/
    │
    ├── routes/
    ├── services/
    ├── hooks/
    ├── types/
    ├── App.tsx
    └── main.tsx
```

---

<h2 align="center">🚀 Instalación y Ejecución</h2>

### 1. Clonar el repositorio

```bash
git clone https://github.com/AaronGuerra/conecta-hogar-monorepo.git
cd conecta-hogar-monorepo
```

### 2. Ejecutar el Backend

Ingresar al directorio:

```bash
cd backend
```

#### Windows

```bash
mvnw.cmd spring-boot:run
```

#### Linux / macOS

```bash
./mvnw spring-boot:run
```

Por defecto, la API estará disponible en:

```text
http://localhost:8080
```

### 3. Ejecutar el Frontend

Desde la raíz del proyecto:

```bash
cd frontend
npm install
npm run dev
```

La aplicación estará disponible en:

```text
http://localhost:5173
```

---

<h2 align="center">⚙️ Variables de Entorno</h2>

El backend utiliza variables de entorno para configurar información sensible, como las credenciales de la base de datos y la clave utilizada para la autenticación mediante JWT.

### Backend

```env
DB_URL=...
DB_USERNAME=...
DB_PASSWORD=...
JWT_SECRET=...
```

### Frontend

```env
VITE_API_URL=http://localhost:8080
```

> ⚠️ No incluir archivos `.env` con credenciales reales dentro del repositorio.

---

<h2 align="center">🔐 Autenticación</h2>

La autenticación se implementa mediante **Spring Security + JWT**.

El flujo general es:

```text
Usuario
   │
   ▼
Login / Registro
   │
   ▼
Spring Security
   │
   ▼
JWT
   │
   ▼
Petición autenticada
   │
   ▼
Endpoint protegido
```

---

<h2 align="center">🌐 Principales Endpoints</h2>

### Autenticación

```http
POST /auth/login
POST /auth/register
```

### Profesionales

```http
GET /maestros
GET /maestros/top

POST /maestros/con-foto

PUT /maestros/{id}/foto

PATCH /maestros/{id}/me-gusta
PATCH /maestros/{id}/no-me-gusta
```

---

<h2 align="center">🎯 Objetivos del Proyecto</h2>

El proyecto busca aplicar conocimientos de desarrollo Full Stack mediante la integración de:

* Desarrollo de APIs REST.
* Arquitectura en capas.
* Desarrollo de interfaces con React.
* TypeScript.
* Autenticación y autorización.
* Persistencia de datos.
* Consumo de APIs.
* Manejo de rutas protegidas.
* Componentización.
* Diseño responsive.
* Trabajo colaborativo con Git.

---

<h2 align="center">📚 Aprendizajes</h2>

Durante el desarrollo de **Conecta Hogar** se trabajaron conceptos relacionados con:

### Backend

* Java y Spring Boot.
* Diseño de APIs REST.
* Spring Security y JWT.
* JPA / Hibernate.
* DTOs y mapeo de objetos.
* Arquitectura en capas.
* Manejo de archivos.

### Frontend

* React y TypeScript.
* Componentes reutilizables.
* React Router.
* Consumo de APIs REST.
* Manejo de estados.
* Rutas protegidas.
* Diseño responsive.

---

<h2 align="center">👥 Equipo</h2>

<h3 align="center">CODE TO CA$H</h3>

|    Integrante   |   Área   |
| :-------------: | :------: |
| Valentina Lulic | Frontend |
| Denisse Labrana | Frontend |
|  Benjamin Pinto | Frontend |
|   Nicolas Luna  |  Backend |
|   Jorge Gatica  |  Backend |
|   Aaron Guerra  |  Backend |

---

<h2 align="center">📄 Licencia</h2>

Este proyecto fue desarrollado con fines académicos y de aprendizaje como parte del proceso de formación en desarrollo Full Stack.

---

<p align="center">
  <strong>🏡 Conecta Hogar · CODE TO CA$H</strong>
</p>

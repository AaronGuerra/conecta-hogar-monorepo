<h1 align="center">🏡 Conecta Hogar</h1>

<p align="center">
  Plataforma web Full Stack que conecta personas que necesitan servicios para el hogar con profesionales especializados.
</p>

<p align="center">
  <strong>React + TypeScript · Java + Spring Boot · REST API · JWT</strong>
</p>

---

<h2 align="center">📌 Descripción</h2>

**Conecta Hogar** es una aplicación web desarrollada como proyecto Full Stack, cuyo objetivo es facilitar la búsqueda y gestión de profesionales que ofrecen servicios para el hogar.

El proyecto integra un **frontend desarrollado con React + TypeScript** y un **backend desarrollado con Java + Spring Boot**, comunicados mediante una API REST.

El proyecto está organizado como un **monorepo**, centralizando frontend y backend en un mismo repositorio para facilitar el desarrollo y mantenimiento.

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
├── backend/          # API REST - Java + Spring Boot
│   ├── src/
│   ├── uploads/
│   ├── .mvn/
│   ├── pom.xml
│   ├── mvnw
│   └── mvnw.cmd
│
├── frontend/         # Aplicación web - React + TypeScript
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
                    │ React + TypeScript  │
                    │      Frontend       │
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
                    │      Database       │
                    └─────────────────────┘
```

---

<h2 align="center">🛠️ Tecnologías</h2>

### Frontend

| Tecnología   | Uso                         |
| ------------ | --------------------------- |
| React        | Desarrollo de la interfaz   |
| TypeScript   | Tipado estático             |
| Vite         | Desarrollo y construcción   |
| React Router | Navegación y rutas          |
| Material UI  | Componentes de interfaz     |
| Tailwind CSS | Estilos y diseño responsive |
| Motion       | Animaciones                 |
| Lucide React | Iconografía                 |
| HTML5 / CSS3 | Estructura y estilos        |

### Backend

| Tecnología              | Uso                                 |
| ----------------------- | ----------------------------------- |
| Java 17+                | Lenguaje principal                  |
| Spring Boot 3           | Desarrollo de la API REST           |
| Spring Security         | Seguridad y autorización            |
| JWT                     | Autenticación mediante tokens       |
| Spring Data JPA         | Persistencia de datos               |
| Hibernate               | ORM                                 |
| Apache Maven            | Gestión del proyecto y dependencias |
| Lombok                  | Reducción de código repetitivo      |
| MapStruct / ModelMapper | Conversión entre DTOs y entidades   |

---

<h2 align="center">📂 Estructura del Backend</h2>

El backend utiliza una **arquitectura en capas**, separando responsabilidades entre controladores, servicios, repositorios, modelos y componentes de seguridad.

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

<h2 align="center">🚀 Instalación y ejecución</h2>

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

En Windows:

```bash
mvnw.cmd spring-boot:run
```

En Linux/macOS:

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

<h2 align="center">⚙️ Variables de entorno</h2>

El backend utiliza variables de entorno para configurar información sensible como las credenciales de la base de datos y la clave utilizada para JWT.

Ejemplo:

```env
DB_URL=...
DB_USERNAME=...
DB_PASSWORD=...
JWT_SECRET=...
```

Para el frontend:

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

**CODE TO CA$H**

| Integrante      | Área     |
| --------------- | -------- |
| Valentina Lulic | Frontend |
| Denisse Labrana | Frontend |
| Benjamin Pinto  | Frontend |
| Nicolas Luna    | Backend  |
| Jorge Gatica    | Backend  |
| Aaron Guerra    | Backend  |

---

<h2 align="center">📄 Licencia</h2>

Este proyecto fue desarrollado con fines académicos y de aprendizaje como parte del proceso de formación en desarrollo Full Stack.

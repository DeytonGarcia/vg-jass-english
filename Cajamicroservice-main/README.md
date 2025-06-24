# 💧 JASS Microservice System – Technical Overview

## 🔧 Project Stack
- **Backend**: Java 17 (IntelliJ IDEA, Spring Boot)
- **Frontend**: Angular (latest stable version, Visual Studio Code)
- **Database**: PostgreSQL
- **Prototyping**: Figma

---

## ✅ PURPOSE OF THE PROJECT
This community-focused system aims to modernize water administration in Rinconada Roma through a **microservice architecture**. Each microservice is designed to manage a specific domain, such as users, payments, distribution, and notifications, helping the local JASS organization operate efficiently and transparently.

---

## ✨ PROJECT PROGRESS
- We have **now created** the microservices assigned to each of us.  
- The team has **just** completed the frontend and backend microservices with their respective databases.  
- We have **not yet** implemented the project merger.  
- This project has **never** been deployed to production.  

---

## 🛠️ SETUP INSTRUCTIONS 
1. **Clone** the repository:  
   `git clone https://github.com/DeytonGarcia/vg-jass-english.git`

2. **Navigate** into a microservice folder (e.g., `ms-cajas`):  
   `cd vg-jass-english/ms-cajas`

3. **Run** the backend with Spring Boot:  
   `./mvnw spring-boot:run`

4. **Navigate** into frontend app:  
   `cd ../frontend`

5. **Install** dependencies and **serve** the Angular app:  
   `npm install`  
   `ng serve`

---

## 🧩 HOW TO USE THE APP?
- You **should** open `http://localhost:4200` after both backend and frontend are running.  
- You **should** log in or register as a user to access the dashboard.  
- You **should** report issues or improvements via the "Feedback" module.

---

## 🎯 FUTURE PLANS 
- We **should** implement role-based access (admin, user, supervisor).  
- We **should** integrate PDF invoice generation with QR codes.  
- We **should** connect payment records with national ID verification (e.g., RENIEC).  
- We **should** deploy on a government-approved cloud hosting service.

---

## 📁 PROJECT ESTRUCTURE '
text
/vg-jass-english
├── ms-organizaciones/     # Manages organizations and branches
├── ms-usuarios/           # Manages user accounts
├── ms-cajas/              # Manages cash registers and assignments
├── ms-pagos/              # Handles payments, invoices, claims
├── ms-distribucion/       # Manages water zones, schedules, tariffs
├── ms-notificaciones/     # Sends notifications, manages templates
├── frontend/              # Angular UI
├── README.md              # ← You are here
├── CONTRIBUTING.md        # Contribution guidelines
├── .env.example           # Template for environment variables
└── docs/                  # UMLs, architecture diagrams, documents
```
```
## 📁 ENDPOINTS POSTMAN '
## 1. Obtener todas las cajas
- **Método:** `GET`
- **Ruta:** `/api/v1/boxes/all`
- **Descripción:** Obtiene todas las cajas.

## 2. Obtener cajas con filtro de estado
- **Método:** `GET`
- **Ruta:** `/api/v1/boxes`
- **Parámetro:** 
  - `status` (opcional): Filtra las cajas según su estado.
- **Descripción:** Obtiene todas las cajas, con opción de filtrar por estado.

## 3. Crear una nueva caja
- **Método:** `POST`
- **Ruta:** `/api/v1/boxes`
- **Cuerpo:** 
  - `Box`: Objeto que representa la caja a crear.
- **Descripción:** Crea una nueva caja y establece su estado como "active".

## 4. Actualizar una caja existente
- **Método:** `PUT`
- **Ruta:** `/api/v1/boxes/{id}`
- **Parámetro:** 
  - `id`: ID de la caja a actualizar.
- **Cuerpo:** 
  - `Box`: Objeto que representa la caja con la información actualizada.
- **Descripción:** Actualiza la información de una caja existente.

## 5. Eliminar una caja
- **Método:** `DELETE`
- **Ruta:** `/api/v1/boxes/{id}`
- **Parámetro:** 
  - `id`: ID de la caja a eliminar.
- **Descripción:** Cambia el estado de la caja a "inactive" en lugar de eliminarla físicamente.

## 6. Obtener cajas por ID de usuario
- **Método:** `GET`
- **Ruta:** `/api/v1/boxes/user/{userId}`
- **Parámetro:** 
  - `userId`: ID del usuario para filtrar las cajas.
- **Descripción:** Obtiene todas las cajas asignadas a un usuario específico.

## 7. Asignar una caja
- **Método:** `POST`
- **Ruta:** `/api/v1/boxes/assign`
- **Cuerpo:** 
  - `AssignBoxRequest`: Objeto que contiene la información para asignar una caja.
- **Descripción:** Asigna una caja a un usuario.

## 8. Actualizar el estado de una caja
- **Método:** `PATCH`
- **Ruta:** `/api/v1/boxes/{id}/status`
- **Parámetro:** 
  - `id`: ID de la caja a actualizar.
- **Cuerpo:** 
  - `BoxStatusUpdate`: Contiene el nuevo estado de la caja.
- **Descripción:** Actualiza el estado de una caja existente.

## 9. Restaurar una caja
- **Método:** `PATCH`
- **Ruta:** `/api/v1/boxes/{id}/restore`
- **Parámetro:** 
  - `id`: ID de la caja a restaurar.
- **Descripción:** Cambia el estado de una caja a "active".
```

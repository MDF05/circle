# Architecture Documentation

## 1. System Overview

The **Circle** platform is architected as a modern, decoupled monolithic application. It consists of a robust RESTful API backend and a responsive Single Page Application (SPA) frontend. The system is designed for scalability, maintainability, and ease of deployment.

### High-Level Diagram
```mermaid
graph TD
    Client[Client Browser]
    FE[Frontend SPA (React/Vite)]
    BE[Backend API (Node/Express)]
    DB[(PostgreSQL)]
    Redis[(Redis Cache)]
    Cloudinary[Cloudinary Media]

    Client -->|HTTPS| FE
    FE -->|REST API/JSON| BE
    BE -->|Prisma ORM| DB
    BE -->|Caching| Redis
    BE -->|Media Upload| Cloudinary
```

---

## 2. Repository Boundaries

The project is structured as a **Monorepo**, but enforces clear logical separation between concerns.

### Frontend (`fe-circle`)
*   **Responsibility**: Handles user interaction, presentation logic, and state management.
*   **Communication**: Consumes the Backend API via HTTP requests (using Axios).
*   **Key Libraries**: React, Redux Toolkit, Chakra UI, React Router.
*   **Build System**: Vite.

### Backend (`be-circle`)
*   **Responsibility**: Handles business logic, data persistence, authentication, and authorization.
*   **Communication**: Exposes RESTful endpoints documented via Swagger.
*   **Key Libraries**: Express, Prisma, Zod (Validation), JSON Web Token (JWT).
*   **Runtime**: Node.js.

---

## 3. Detailed Component Architecture

### 3.1 Backend Layer
The backend implementation follows a **Controller-Service-Repository** pattern (or similar modular structure) to separate concerns.

*   **API Layer (Controllers)**: Handles HTTP requests, parses input, validates using Zod, and sends responses.
*   **Service Layer**: Implementing business logic and transaction management.
*   **Data Access Layer (Prisma)**: Interacts directly with the PostgreSQL database.
*   **Middleware**: Handles cross-cutting concerns like Authentication (`auth middleware`), Error Handling, and Logging.

### 3.2 Frontend Layer
The frontend is built using a component-based architecture.

*   **Pages**: Top-level components representing routes.
*   **Components**: Reusable UI elements (Buttons, Cards, Inputs).
*   **Store (Redux)**: Global state management for user sessions and cached data.
*   **Hooks**: Custom React hooks for encapsulating logic (e.g., `useAuth`).

---

## 4. Inter-Service Communication

### API Design
*   **Protocol**: HTTP/1.1 (HTTPS in production).
*   **Format**: JSON.
*   **Authentication**: Bearer Token (JWT) passed in the `Authorization` header.

### External Integrations
*   **Database**: Connection via TCP/IP to PostgreSQL instance.
*   **Redis**: Used for caching frequently accessed data and session management.
*   **Cloudinary**: Direct upload or proxy upload for handling user-generated content (images/videos).

---

## 5. Security Architecture

*   **Data Transport**: All traffic encrypted via TLS/SSL.
*   **Data at Rest**: Sensitive data (passwords) hashed using bcrypt before storage.
*   **Input Validation**: Strict validation on both client and server sides (Zod).
*   **CORS**: Configured to allow requests only from trusted frontend domains.

---

## 6. Scalability Considerations

*   **Stateless Backend**: The Node.js application is stateless, allowing for horizontal scaling behind a load balancer.
*   **Caching Strategy**: Redis is employed to reduce database load for read-heavy operations.
*   **Database Optimization**: Prisma migrations manage schema evolution; indexing strategies applied to frequently queried fields.

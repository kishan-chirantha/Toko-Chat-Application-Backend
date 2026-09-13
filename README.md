# Toko Chat Application – Backend

Toko is a secure, real-time chat application designed to provide reliable messaging and communication between users. This repository contains the Java-based backend responsible for user management, authentication, REST API operations, WebSocket communication, and database integration.

The backend provides the services required by the Toko React Native mobile application through **REST APIs and WebSockets**.

---

## 🚀 Tech Stack

| Technology           | Purpose                                            |
| -------------------- | -------------------------------------------------- |
| **Java**             | Backend application development                    |
| **Java Servlets**    | REST API and server-side request handling          |
| **WebSockets**       | Real-time bidirectional communication              |
| **Hibernate ORM**    | Object-relational mapping and database persistence |
| **MySQL**            | Relational database management                     |
| **GlassFish Server** | Jakarta EE application server                      |

---

## ✨ Core Features

### 💬 Real-Time Messaging

* Real-time one-to-one messaging using WebSockets
* Persistent bidirectional communication
* Instant message delivery between connected users
* Real-time chat data synchronization
* WebSocket connection lifecycle management

### 👤 User Authentication & Management

The backend provides server-side functionality for:

* User registration
* User authentication
* User account management
* User session handling
* User information retrieval

Authentication and authorization are enforced on the server to prevent unauthorized access to protected resources.

### 👥 Contact & Friend Management

The backend manages user relationships and contact information, including:

* User-to-user relationships
* Friend and contact management
* Retrieving user information
* Managing chat participants

### 💾 Database Management

The application uses **Hibernate ORM** to map Java objects to relational database entities.

The MySQL database stores application data such as:

* `user`
* `friend_list`
* `chat`

Hibernate handles object-relational mapping, database queries, and persistence operations between the Java application and MySQL database.

---

## 🔐 Security & Access Control

### 🤝 WebSocket Handshake Validation

The backend validates the user information provided during the WebSocket connection process.

Only authenticated and authorized users should be allowed to establish a WebSocket session.

### 🛡️ Chat Authorization

The backend validates whether the requesting user is an authorized participant of a requested conversation before allowing access to chat data.

This prevents users from accessing conversations that do not belong to them.

> **Note:** Security and authorization are enforced on the backend and should not rely solely on frontend validation.

---

## 🏗️ Backend Architecture

The backend follows a layered architecture separating request handling, business logic, real-time communication, and data persistence.

```text
Toko Backend
│
├── REST API Layer
│   └── Java Servlets
│
├── Real-Time Communication
│   └── WebSocket Endpoints
│
├── Business Logic
│   ├── User Management
│   ├── Authentication
│   ├── Contact Management
│   └── Chat Management
│
├── Persistence Layer
│   └── Hibernate ORM
│
└── Database
    └── MySQL
```

### REST API

REST APIs are used for operations such as:

* User registration
* User authentication
* User management
* Contact management
* Retrieving application data

### WebSocket

WebSockets are used for real-time operations such as:

* Establishing chat connections
* Sending messages
* Receiving messages
* Synchronizing conversations
* Maintaining live communication

---

## 🧪 Development Requirements

Before running the backend, ensure that the following are installed and configured:

* Java Development Kit (JDK)
* GlassFish Server
* MySQL Server
* MySQL Workbench (optional)
* Maven
* NetBeans IDE or another Java IDE

The backend should be running before launching the React Native frontend.

---

## 🔗 Related Repository

### Frontend Repository

The React Native mobile application is maintained in a separate repository:

**[Toko Chat Application – Frontend](https://github.com/kishan-chirantha/Toko-Chat-Application)**

---

## 📄 License

This project was developed for educational and academic purposes.

© 2026 Kishan Chirantha. All rights reserved.

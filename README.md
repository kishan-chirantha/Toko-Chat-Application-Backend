# Toko Chat Application - Backend

This repository contains the backend source code for **Toko**, a secure, real-time chat application designed to offer free and secure calling and messaging to users worldwide. This backend handles user registration, account management, and real-time data synchronization.

## 🚀 Tech Stack

* **Language:** Java
* **API & Core Logic:** Java Servlets
* **Real-Time Communication:** WebSockets
* **Database:** MySQL
* **Application Server:** GlassFish

## ⚙️ Core Features & Architecture

* **Real-time Messaging:** Utilizes WebSockets for instant, low-latency sending and receiving of messages, maintaining a persistent, bi-directional connection.
* **User Authentication & Management:** Server-side logic built on Java Servlets handles initial non-real-time operations, such as user login and signup, processing data and managing the lifecycle of the user session.
* **Database Management:** Uses Hibernate Object-Relational Mapping (ORM) to seamlessly store and retrieve application data. The database includes tables for `user`, `friend_list`, and `chat`.
* **Security & Access Control:**
  * **Secure Connections:** Real-time chat functionality relies on a secure and authenticated WebSocket connection using the `wss://` protocol for TLS/SSL encryption.
  * **Handshake Validation:** The server validates the `userId` passed as a query parameter during the WebSocket handshake, ensuring only authenticated users can connect.
  * **Data Authorization:** Strict server-side access control logic ensures that the requesting `userId` is a legitimate participant in the requested chat before retrieving and sending chat data.

# 🎟️ VivaEventos - Sistema de Gestión de Boletas

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Microservices](https://img.shields.io/badge/Architecture-Microservices-blue?style=for-the-badge)

VivaEventos es una plataforma robusta para la venta de boletas de eventos, construida bajo una arquitectura de **microservicios** escalable y resiliente utilizando el ecosistema de Spring Cloud.

---

## 🏗️ Arquitectura de Microservicios

El sistema se compone de los siguientes módulos interconectados:

| Servicio | Descripción | Puerto | Repositorio |
| :--- | :--- | :--- | :--- |
| **Service Registry** | Discovery Server (Netflix Eureka). | `8761` | [Ver repo](https://github.com/Davidgarar/service-registry) |
| **Auth Service** | Autenticación, autorización y seguridad (JWT). | `8084` | [Ver repo](https://github.com/Davidgarar/auth-service) |
| **Event Service** | Gestión de eventos, locaciones y fechas. | `8081` | [Ver repo](https://github.com/Davidgarar/event-service) |
| **Ticket Service** | Generación, control y validación de boletas. | `8086` | [Ver repo](https://github.com/Davidgarar/ticket-service) |
| **Order Service** | Procesamiento de órdenes de compra. | `8082` | [Ver repo](https://github.com/Davidgarar/order-service) |
| **Payment Service** | Pasarela y procesamiento de pagos. | `8085` | [Ver repo](https://github.com/Davidgarar/payment-service) |
| **Notification Service** | Envío de correos y alertas al usuario. | `8083` | [Ver repo](https://github.com/Davidgarar/notification-service) |

---

## 🚀 Guía de Inicio Rápido

### 📋 Requisitos Previos
*   **Java 17** o superior.
*   **Maven 3.8+**.
*   **Git** instalado.

### Orden de ejecucion:
Terminal 1 - Service Registry (primero)

Terminal 2 - Event Service (segundo)

Terminal 3 - Order Service (tercero)

Terminal 4 - Notification Service (cuarto)


### Instalación (Clonar todo)
Ejecuta este comando en tu terminal para clonar todos los repositorios en una sola carpeta:

```bash
mkdir VivaEventos-Project && cd VivaEventos-Project && \
git clone [https://github.com/Davidgarar/service-registry.git](https://github.com/Davidgarar/service-registry.git) && \
git clone [https://github.com/Davidgarar/event-service.git](https://github.com/Davidgarar/event-service.git) && \
git clone [https://github.com/Davidgarar/order-service.git](https://github.com/Davidgarar/order-service.git) && \
git clone [https://github.com/Davidgarar/notification-service.git](https://github.com/Davidgarar/notification-service.git)

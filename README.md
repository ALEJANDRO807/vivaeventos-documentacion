# 🎟️ VivaEventos - Sistema de Gestión de Boletas

![Java](https://img.shields.io/badge/Java-ED8B00?style=for-the-badge&logo=java&logoColor=white)
![Spring Boot](https://img.shields.io/badge/Spring_Boot-6DB33F?style=for-the-badge&logo=spring-boot&logoColor=white)
![Microservices](https://img.shields.io/badge/Architecture-Microservices-blue?style=for-the-badge)

VivaEventos es una plataforma robusta para la venta de boletas de eventos, construida bajo una arquitectura de **microservicios** escalable y resiliente utilizando el ecosistema de Spring Cloud.

---

## 🏗️ Arquitectura del Sistema

El sistema se divide en los siguientes componentes estratégicos:

| Servicio | Descripción | Puerto | Repositorio |
| :--- | :--- | :--- | :--- |
| **Service Registry** | Localizador de servicios (Netflix Eureka). | `8761` | [Ver repo](https://github.com/Davidgarar/service-registry) |
| **Event Service** | Gestión del catálogo de eventos y disponibilidad. | `8081` | [Ver repo](https://github.com/Davidgarar/event-service) |
| **Order Service** | Procesamiento de órdenes y ventas. | `8082` | [Ver repo](https://github.com/Davidgarar/order-service) |
| **Notification Service** | Envío de confirmaciones y alertas. | `8083` | [Ver repo](https://github.com/Davidgarar/notification-service) |

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

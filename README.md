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
| **Validation Service** | Validacion Logistica. | `8087` | [Ver repo](https://github.com/JuanHincapie86/validation-service) |
| **Email service** | Confirmacion y recordatorio via email. | `8088` | [Ver repo](https://github.com/JuanHincapie86/email-service) |
---

## 🚀 Guía de Inicio Rápido

### 📋 Requisitos Previos
*   **Java 17** o superior.
*   **Maven 3.8+**.
*   **Git** instalado.

## ⚙️ Orden de Ejecución Local (Manual)

Si desea levantar los servicios de forma manual e independiente en lugar de usar Docker, debes abrir una pestaña de la terminal para cada microservicio y ejecutarlos estrictamente en el siguiente orden para asegurar el correcto registro en Eureka:

* **Terminal 1:** Service Registry (Primero - Servidor de Descubrimiento)
* **Terminal 2:** Event Service (Segundo)
* **Terminal 3:** Order Service (Tercero)
* **Terminal 4:** Notification Service (Cuarto)
* **Terminal 5:** Auth Service (Quinto)
* **Terminal 6:** Ticket Service (Sexto)
* **Terminal 7:** Payment Service (Séptimo)
* **Terminal 8:** Validation Service (Octavo)
* **Terminal 9:** Email Service (Noveno)

---

## 🐳 Despliegue con Docker (Ecosistema Completo)

### 🚀 Instrucciones para ejecutar el proyecto localmente

No es necesario compilar el código fuente ni generar los archivos `.jar` localmente, ya que las imágenes se descargarán automáticamente desde la nube.

Antes de iniciar cualquiera de los dos despliegues, asegúrate de contar con:
* **Docker Desktop** instalado y en ejecución.

### 📌 Registro de Imágenes Públicas
Las imágenes utilizadas se encuentran alojadas en el siguiente perfil público de Docker Hub:
👉 [Perfil de Docker Hub - alejandrolunalh](https://hub.docker.com/u/alejandrolunalh)

### 🚀 Comandos de Inicialización

1. Abre una terminal en la raíz de este repositorio (donde reside el archivo `docker-compose.yml`).
2. Ejecuta el siguiente comando para descargar las imágenes e iniciar el ecosistema en segundo plano:
   ```bash
   docker compose up -d

### 🔍 Verificar el estado de los servicios
Puedes comprobar el estado de los contenedores mediante el panel visual de **Docker Desktop** o directamente desde tu terminal ejecutando:
```bash
docker compose ps
```
# 📊 Matriz de Puertos y Enlaces de Acceso

Una vez que cualquiera de los dos entornos esté arriba y saludable (**Healthy**), podrás interactuar con los microservicios de manera transparente a través de tu `localhost`.

| Servicio | Puerto Local | Endpoint Base / Dashboard |
|---|---|---|
| Servidor de Descubrimiento (Eureka) | `8761` | http://localhost:8761 |
| Auth Service (Autenticación) | `8085` | http://localhost:8085/api/v1/auth |
| Event Service (Eventos) | `8081` | http://localhost:8081/api/v1/events/ |
| Order Service (Órdenes) | `8082` | http://localhost:8082/api/v1/orders/ |
| Ticket Service (Tickets) | `8086` | http://localhost:8086/api/v1/tickets/ |
| Payment Service (Pagos) | `8084` | http://localhost:8084/api/v1/payments/ |
| Notification Service | `8083` | Conexión interna |
| Validation Service | `8087` | Conexión interna |
| Email Service | `8088` | Conexión interna |

## 📥 Instalación (Clonación Completa del Ecosistema)

Para descargar el repositorio principal de orquestación junto con los 9 microservicios independientes en tu máquina local de un solo golpe, copia y pega el siguiente comando unificado en tu terminal:

```bash
git clone [https://github.com/ALEJANDRO807/vivaeventos-project.git](https://github.com/ALEJANDRO807/vivaeventos-project.git) && cd vivaeventos-project && \
git clone [https://github.com/Davidgarar/service-registry.git](https://github.com/Davidgarar/service-registry.git) && \
git clone [https://github.com/Davidgarar/event-service.git](https://github.com/Davidgarar/event-service.git) && \
git clone [https://github.com/Davidgarar/order-service.git](https://github.com/Davidgarar/order-service.git) && \
git clone [https://github.com/Davidgarar/notification-service.git](https://github.com/Davidgarar/notification-service.git) && \
git clone [https://github.com/Davidgarar/auth-service.git](https://github.com/Davidgarar/auth-service.git) && \
git clone [https://github.com/Davidgarar/ticket-service.git](https://github.com/Davidgarar/ticket-service.git) && \
git clone [https://github.com/Davidgarar/payment-service.git](https://github.com/Davidgarar/payment-service.git) && \
git clone [https://github.com/JuanHincapie86/validation-service.git](https://github.com/JuanHincapie86/validation-service.git) && \
git clone [https://github.com/JuanHincapie86/email-service.git](https://github.com/JuanHincapie86/email-service.git)
```

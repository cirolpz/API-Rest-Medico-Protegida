# API REST de Hospital | Spring Security, JWT

Este proyecto es una API REST desarrollada en **Spring Boot** para gestionar los recursos de un hospital, como médicos, usuarios y pacientes. Implementa buenas prácticas de desarrollo, manejo de errores, seguridad con **Spring Security** y autenticación mediante **JSON Web Token (JWT)**.
## Video
[![Video del Proyecto](https://img.youtube.com/vi/bj4ap7-RJEs/maxresdefault.jpg)](https://www.youtube.com/watch?v=bj4ap7-RJEs)
## Características Principales

-   **Gestión de Recursos:**
    -   Control de médicos, usuarios y pacientes.
-   **Buenas Prácticas de API:**
    -   Retornos estándar en la API.
    -   Uso de códigos HTTP adecuados como `201 Created`.
    -   Manejo de excepciones y errores personalizados (`400`, `404`).
-   **Seguridad:**
    -   Autenticación y autorización con **Spring Security**.
    -   Generación y validación de tokens JWT.
    -   Control de acceso a recursos según roles.
-   **Estandarización y Extensibilidad:**
    -   Uso de `ResponseEntity` para personalizar respuestas.
    -   Implementación de filtros de seguridad.

----------

## Contenido del Proyecto

### Buenas Prácticas en API

1.  **Estandarizando Retornos:**
    
    -   Respuestas estructuradas con `ResponseEntity`.
    -   Incluye el código `201 Created` y `Header Location` en recursos creados.
2.  **Manejo de Errores:**
    
    -   Tratamiento de errores comunes (`400`, `404`) con mensajes personalizados.
    -   Uso de `RestControllerAdvice` para centralizar el manejo de excepciones.
3.  **Mensajes Localizados:**
    
    -   Configuración para mostrar mensajes en español mediante propiedades de Spring Boot.

### Seguridad con Spring Security

1.  **Autenticación y Autorización:**
    
    -   Implementación de autenticación basada en usuarios registrados en una base de datos MySQL.
    -   Contraseñas hash para mayor seguridad.
2.  **Configuración:**
    
    -   Definición de clases de configuración para personalizar la seguridad de la API.
    -   Uso de controladores dedicados para la autenticación.
3.  **Tokens JWT:**
    
    -   Generación y validación de JWT utilizando la librería `auth0-jwt`.
    -   Configuración para extraer y validar tokens de solicitudes.
4.  **Control de Acceso:**
    
    -   Uso de filtros de seguridad para interceptar solicitudes.
    -   Liberación de accesos específicos (e.g., login).
    -   Control de acceso por roles y anotaciones.

----------

## Configuración

1.  **Base de Datos:**
    
    -   Configuración de una base de datos MySQL.
    -   Entidades principales: médicos, usuarios, pacientes.
2.  **Dependencias:**
    
    -   Spring Boot Starter Web.
    -   Spring Boot Starter Security.
    -   Spring Data JPA.
    -   Auth0 JWT.
3.  **Propiedades:**
    
    -   Configuración en `application.properties` para base de datos y seguridad.

----------

## Ejecución

1.  Clona el repositorio:
    
    bash
    
    Copiar código
    
    `git clone <url-del-repositorio>
    cd <nombre-del-proyecto>` 
    
2.  Configura las propiedades de conexión en `src/main/resources/application.properties`.
    
3.  Inicia la aplicación:
    
    bash
    
    Copiar código
    
    `mvn spring-boot:run` 
    

----------

## Aprendizajes y Recursos Clave

-   **Buenas prácticas en diseño de API.**
-   **Manejo centralizado de errores y mensajes localizados.**
-   **Configuración y uso avanzado de Spring Security.**
-   **Autenticación segura con JWT.**
-   **Control de acceso granular basado en roles.**

----------

## Próximos Pasos

1.  Mejorar la gestión de pacientes con funcionalidades adicionales.
2.  Optimizar el manejo de excepciones para otros códigos de error (`403`, `500`).
3.  Integrar documentación de la API con **Swagger**.

# 🗺️ Aplicación de Rutas y Movilidad Inteligente (WIP)

> **Estado del proyecto:** En fase inicial de desarrollo (Sprint 0 / Spike).

## 📖 Descripción del Proyecto
Este proyecto consiste en el desarrollo de una **aplicación de movilidad** que permite calcular rutas entre lugares de interés (dados de alta por el usuario o seleccionados en el mapa), teniendo en cuenta diferentes métodos de transporte (vehículo a motor, bicicleta o a pie). 

La aplicación no solo calcula el trayecto, la distancia y la duración, sino que también estima el **coste asociado a la ruta**: gasto económico en combustible o electricidad para vehículos, y gasto calórico para rutas a pie o en bicicleta.

El proyecto se desarrolla de forma conjunta para las asignaturas *Diseño de Software (EI1039)* y *Paradigmas de Software (EI1048)* del Grado en Ingeniería Informática (UJI).

## 🛠️ Tecnologías y Herramientas (Tech Stack)
Aunque el proyecto está en sus etapas iniciales, el stack tecnológico definido para el desarrollo es:

*   **Lenguaje / Plataforma:** **Kotlin** para desarrollo móvil nativo en Android (usando Android Studio).
*   **Lógica de Negocio y Conexión de Red:** Retrofit y Coroutines para llamadas asíncronas a APIs.
*   **APIs Externas (Integraciones planificadas):**
    *   **Openrouteservice:** Para el cálculo de rutas y geocodificación (obtención de coordenadas a partir de topónimos).
    *   **datos.gob.es:** Para obtener en tiempo real los precios de los carburantes en España.
    *   **Red Eléctrica de España:** Para los precios de la electricidad (recarga de vehículos eléctricos).
*   **Cartografía y Mapas:** Integración planificada con SDKs de mapas para la visualización de trayectos e interacción con marcadores.

## ⚙️ Metodología de Desarrollo
El desarrollo se rige estrictamente por procesos ágiles y buenas prácticas de ingeniería de software:

*   **ATDD (Acceptance Test Driven Development):** El desarrollo está guiado por Pruebas de Aceptación. Toda funcionalidad (historia de usuario) comienza definiendo los escenarios válidos e inválidos y sus pruebas (Given-When-Then) antes de escribir el código de producción.
*   **Pruebas de Integración con Mocks:** La lógica de negocio está completamente desacoplada de los servicios externos (APIs) usando abstracciones e inyección de dependencias, permitiendo probar la aplicación usando *mocks* cuando los servicios reales no están disponibles.
*   **Gitflow Adaptado:** Se utiliza una metodología estricta de ramas para el trabajo colaborativo (rama `main` para versiones estables, ramas `it-nn` para iteraciones y ramas `h-xx` para historias de usuario individuales), junto con *Pull Requests* para la revisión de código.

## 📋 Alcance Funcional (Historias de Usuario planificadas)
El sistema abordará los siguientes bloques funcionales:
1.  **Gestión de Usuarios:** Registro, inicio/cierre de sesión y modificación de perfiles.
2.  **Gestión de Lugares de Interés:** Alta por coordenadas, topónimos o clic en el mapa, y visualización de marcadores.
3.  **Gestión de Vehículos:** Inventario de vehículos personales con sus características (combustible, estado de avería).
4.  **Gestión de Rutas:** Cálculo avanzado considerando el medio de transporte para ofrecer la ruta más rápida, corta o económica, estimando costes (€ o kcal). Guardado e inversión de rutas.
5.  **Preferencias y Persistencia:** Guardado de favoritos (lugares, rutas), unidades de medida, y persistencia del estado de la aplicación incluso ante cierres inesperados (modo offline básico).

## 🎓 Autores y Grupo de Trabajo
*   Talia Hinojo Montañana
*   Rayan Mohamed Djelloul Ayad
*   Pedro Jareño Sevilla
*   Murat Can Isik

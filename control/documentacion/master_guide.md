# Guía Maestra del Proyecto: Organizador de Tareas Compartidas

## 1. Introducción

Este documento sirve como la guía principal para el desarrollo y mantenimiento del proyecto "Organizador de Tareas Compartidas". La aplicación está diseñada para facilitar la gestión de tareas del hogar, proyectos de grupo o planificación de eventos, permitiendo a los usuarios asignar tareas, establecer fechas límite y enviar recordatorios automáticos. Nuestro objetivo es crear una solución robusta, intuitiva y de alta calidad.

## 2. Filosofía de Desarrollo

Nuestro proceso de desarrollo se rige por los siguientes principios fundamentales:

*   **CERO INTERVENCIÓN HUMANA (AUTONOMÍA AI):** El ciclo de desarrollo, desde la creación de pruebas hasta la implementación y corrección, busca ser autónomo, gestionado por agentes de IA. La intervención humana es mínima y orientada a la supervisión.
*   **CALIDAD ANTE TODO:** Priorizamos la producción de código limpio, mantenible, eficiente, escalable y bien documentado, adhiriéndonos a las mejores prácticas de la industria.
*   **TDD NO NEGOCIABLE:** El Desarrollo Dirigido por Pruebas (TDD) es la piedra angular de nuestra metodología. Ningún código de implementación es escrito sin una prueba que falle primero.
*   **SISTEMA DE CONTROL COMO FUENTE DE VERDAD:** Todos los documentos en la carpeta `control/` son la fuente única y autorizada de información para el proyecto. Deben leerse y actualizarse rigurosamente.

## 3. Características Principales de la Aplicación

El "Organizador de Tareas Compartidas" incluirá las siguientes funcionalidades clave:

*   **Persistencia de Datos:** Almacenamiento seguro y robusto de tareas, usuarios, grupos y configuraciones.
*   **Autenticación y Gestión de Usuarios:** Registro, inicio/cierre de sesión y gestión de perfiles de usuario.
*   **Gestión de Grupos y Proyectos:** Creación, edición y eliminación de grupos, con invitación a miembros.
*   **Creación y Edición de Tareas:** Definición de título, descripción y asociación a grupos.
*   **Asignación de Tareas a Miembros:** Asignación flexible de tareas y visualización de asignaciones.
*   **Establecimiento de Fechas y Horas Límite:** Definición y gestión de plazos para cada tarea.
*   **Gestión del Estado de Tareas:** Marcado de tareas como 'pendientes', 'en progreso', 'completadas' y filtrado.
*   **Sistema de Recordatorios Automáticos:** Notificaciones proactivas sobre tareas próximas o vencidas.
*   **Interfaz de Usuario Intuitiva y Experiencia de Usuario:** Diseño centrado en el usuario para una navegación fácil y agradable.
*   **Pruebas Exhaustivas:** Cobertura completa con pruebas unitarias, de integración y E2E.
*   **Pipeline de Integración y Despliegue Continuo (CI/CD):** Automatización del proceso de integración y despliegue.

## 4. Tecnologías Principales

El proyecto se construye utilizando un stack moderno y eficiente:

*   **Frontend:** React.js con TypeScript, Vite (bundler), Tailwind CSS (estilos).
*   **Backend:** Node.js con TypeScript, Express.js (framework).
*   **Base de Datos:** PostgreSQL (relacional).
*   **ORM:** Prisma (para interacción con PostgreSQL).
*   **Testing:** Vitest y React Testing Library (para frontend y backend).
*   **Contenedores:** Docker.
*   **CI/CD:** GitHub Actions (o similar).

## 5. Estructura del Proyecto (Alto Nivel)

El proyecto seguirá una estructura modular, separando claramente las responsabilidades entre el frontend, el backend y la base de datos, con una configuración compartida para TypeScript y herramientas de linting/formateo. Se espera una estructura de monorepo si el proyecto escala, o al menos repositorios bien definidos para cada parte.

## 6. Proceso de Desarrollo y Contribución

Todo el desarrollo debe seguir el ciclo de trabajo TDD automatizado descrito en el prompt del agente de desarrollo. Los cambios deben estar documentados en `control/seguimiento/roadmap.md` y, una vez completados, se deben actualizar los archivos de seguimiento (`arbol.md`, `dependencias.md`, `memoria/`).

Para detalles específicos sobre la arquitectura, configuración del entorno o guías de estilo, consulte los documentos correspondientes en la carpeta `control/documentacion/`.
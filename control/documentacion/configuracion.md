# Configuración del Proyecto: Organizador de Tareas Compartidas

Este documento detalla los pasos y requisitos para configurar el entorno de desarrollo y ejecutar el proyecto "Organizador de Tareas Compartidas".

## 1. Requisitos Previos

Antes de empezar, asegúrate de tener instaladas las siguientes herramientas en tu sistema:

*   **Node.js:** Versión 18.x o superior. Puedes descargarlo desde [nodejs.org](https://nodejs.org/).
*   **npm o Yarn:** Se recomienda npm (viene con Node.js) o Yarn (versión 1.x o 2.x/3.x "Berry").
    ```bash
    node -v
    npm -v
    # o
    yarn -v
    ```
*   **Git:** Para clonar el repositorio y gestionar el control de versiones.
    ```bash
    git --version
    ```
*   **Docker y Docker Compose:** (Recomendado para la base de datos) Para gestionar fácilmente el contenedor de PostgreSQL.
    ```bash
    docker --version
    docker compose version
    ```

## 2. Configuración del Entorno de Desarrollo

### 2.1. Clonar el Repositorio

Primero, clona el repositorio del proyecto:

```bash
git clone [URL_DEL_REPOSITORIO]
cd organizador-tareas-compartidas
```

### 2.2. Estructura del Proyecto (Ejemplo de Monorepo)

Asumimos una estructura de monorepo o al menos directorios separados para frontend y backend:

```
organizador-tareas-compartidas/
├── backend/
│   ├── src/
│   ├── package.json
│   └── tsconfig.json
├── frontend/
│   ├── src/
│   ├── public/
│   ├── package.json
│   └── tsconfig.json
├── control/
│   └── documentacion/
│   └── seguimiento/
│   └── memoria/
├── .env.example
├── docker-compose.yml
├── package.json (root, si es monorepo)
└── tsconfig.json (root, si es monorepo)
```

### 2.3. Instalación de Dependencias

Navega a cada directorio y instala las dependencias:

```bash
# En el directorio raíz (si es monorepo con un único package.json)
npm install # o yarn install

# O si frontend y backend tienen sus propios package.json
cd backend
npm install # o yarn install

cd ../frontend
npm install # o yarn install
```

### 2.4. Configuración de Variables de Entorno

El proyecto utiliza variables de entorno para la configuración sensible. Copia el archivo `.env.example` (ubicado en la raíz del proyecto o en `backend/` y `frontend/`) a `.env` y edítalo con tus valores.

**Ejemplo de `.env` (backend):**

```env
PORT=3000
DATABASE_URL=
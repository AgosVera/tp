# NewCine 

Bienvenido al proyecto **NewCine**. Esta es una aplicación web completa para gestionar un cine, que incluye cartelera pública para los clientes, compra de entradas, y un panel de administración para gestionar películas, salas, funciones, géneros y ventas.

El proyecto está dividido en dos partes independientes:
1. **Backend:** El servidor que maneja la base de datos, la autenticación y la lógica de negocio.
2. **Frontend:** La interfaz visual que ven los usuarios en el navegador.

---

## Requisitos Previos

Antes de instalar, asegurate de tener las siguientes herramientas instaladas en tu computadora:

*   **Node.js** (versión 18 o superior). Descargalo desde [nodejs.org](https://nodejs.org/).
*   **pnpm** Si no lo tenés, instalalo abriendo una terminal y ejecutando:
    ```bash
    npm install -g pnpm
*   **MySQL** El proyecto utiliza MySQL 8.0 CE

## Instalación paso a paso

### Dependencias del Backend

El backend está construido con Node.js, Express y TypeScript. Las dependencias principales son:

*   **Framework y Servidor:**
    *   `express`: Framework web para crear la API REST.
    *   `cors`: Middleware para permitir peticiones desde el frontend (CORS).
*   **Base de Datos (ORM):**
    *   `@mikro-orm/core`: Núcleo del ORM MikroORM.
    *   `@mikro-orm/decorators`: Decoradores para definir entidades con TypeScript.
    *   `@mikro-orm/mysql`: Driver oficial de conexión a la base de datos MySQL.
    *   `@mikro-orm/sql-highlighter`: Herramienta para resaltar y depurar las consultas SQL.
    *   `reflect-metadata`: Requerido por MikroORM para el uso de decoradores.
*   **Autenticación y Seguridad:**
    *   `jsonwebtoken`: Para generar y validar tokens JWT.
    *   `bcryptjs`: Para encriptar (hashear) contraseñas.
*   **Generación de Códigos QR:**
    *   `qrcode`: Para generar los códigos QR de las entradas compradas.
*   **Herramientas de Desarrollo (DevDependencies):**
    *   `typescript`: Compilador de TypeScript a JavaScript.
    *   `tsc-watch`: Para reiniciar el servidor automáticamente al guardar cambios.
    *   `vitest` y `supertest`: Herramientas para ejecutar tests unitarios y de integración.
    *   `@types/express`, `@types/cors`, `@types/bcryptjs`, `@types/jsonwebtoken`, `@types/node`, `@types/qrcode`, `@types/supertest`: Definiciones de tipos para TypeScript.
*(Para instalar todas estas dependencias, ejecutá `pnpm install` dentro de la carpeta `dsw-backend`).*

### Dependencias del Frontend

El frontend está construido con React y TypeScript, utilizando Vite como empaquetador. Las dependencias principales son:

*   **Librerías Principales (Dependencies):**
    *   `react` y `react-dom`: Biblioteca principal para construir la interfaz de usuario.
    *   `react-router-dom`: Para manejar la navegación entre páginas sin recargar el navegador.
    *   `sweetalert2`: Para mostrar alertas y modales elegantes (reemplazando los `alert()` nativos).
*   **Herramientas de Desarrollo y testing (DevDependencies):**
    *   `vite`: Empaquetador y servidor de desarrollo ultrarrápido.
    *   `typescript`: Lenguaje que añade tipado estático a JavaScript.
    *   `@vitejs/plugin-react`: Plugin oficial de React para Vite.
    *   `eslint` y sus plugins (`@eslint/js`, `eslint-plugin-react-hooks`, etc.): Herramientas de análisis de código para mantener buenas prácticas.
    *   `@types/react`, `@types/react-dom`, `@types/node`: Definiciones de tipos para TypeScript.
    *   **Testing Unitario:** `vitest`, `@testing-library/react`, `@testing-library/jest-dom`, `@testing-library/user-event`, `jsdom`.
    *   **Testing E2E:** `@playwright/test`.
*(Nota: Para instalar todas estas dependencias, ejecutá `pnpm install` dentro de la carpeta `cine-frontend`).*

### Configuración de Variables de Entorno (`.env`)

Para que el servidor funcione, creá un archivo llamado `.env` en la raíz de `dsw-backend` con el siguiente contenido (ajustá los valores a tu base de datos local):

```env
DB_HOST=localhost
DB_USER=dsw
DB_PASSWORD=dsw
DB_NAME=cine
JWT_SECRET=contrasenia_secreta_muy_larga_y_complicada_que_deberia_ser_mas_segura
```

> ** Importante sobre la Base de Datos:**
> El proyecto está configurado para conectarse a una base de datos MySQL local con las siguientes credenciales por defecto:
> *   **Usuario:** `dsw`
> *   **Contraseña:** `dsw`
> *   **Base de datos:** `cine`
> *   **Puerto:** `3306`
> 
> Si tu MySQL local usa otras credenciales, deberás modificar el archivo `orm.ts` (en la propiedad `clientUrl`) para que coincidan con las tuyas.
>
> Además, el proyecto utiliza `syncSchema()`, que crea las tablas automáticamente al iniciar el servidor por primera vez.

---

## Pasos para Ejecutar el Proyecto

Para poner en marcha la aplicación, abrí **dos terminales distintas** (una para el backend y otra para el frontend).

### Paso 1: Levantar el Backend

1. Abrí una terminal y navegá hasta la carpeta del backend:
    ```bash
    cd dsw-backend
2. Instalá todas las dependencias (esto descarga Express, MikroORM, etc.):
   ```bash
   pnpm install
4. Iniciá el servidor en modo desarrollo (Deberás ver un mensaje en la terminal diciendo Server is running on port 3001s):
    ```bash
    pnpm start:dev
5. Crea un usuario Administrador (Solo la primera vez): Para probar el panel de control, necesitás un usuario con permisos de admin. Abrí una tercera terminal, navegá a dsw-backend y ejecutá:
    ```bash
    pnpm seed:admin

### Paso 2: Levantar el Frontend

1. Abrí una terminal y navegá hasta la carpeta del backend:
    ```bash
    cd cine-frontend
2. Instalá todas las dependencias
   ```bash
   pnpm install
4. Iniciá la aplicación
    ```bash
    pnpm dev
5. Abrí tu navegador web y entrá a la siguiente dirección: http://localhost:5173

##  Roles y Acceso

La aplicación cuenta con dos niveles de acceso:

*   **Cliente (Público):** Puede ver la cartelera, buscar películas, ver detalles, ver trailers y comprar entradas (requiere registrarse previamente).
*   **Administrador:** Tiene acceso al panel de administración para crear/editar/eliminar Salas, Películas, Géneros y Funciones, y ver las compras realizadas.

**Datos del Administrador (creados con el `seed:admin`):**

*   **Email:** `admin@test.com`
*   **Contraseña:** `admin123` 

*(Si no se ejecutó el seed, podés registrarte como cliente desde la web y luego modificar tu rol directamente en la base de datos a `ADMIN`).*

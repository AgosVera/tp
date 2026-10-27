# 🎬 NewCine 

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

Las dependencias principales son:

*   **Framework y Servidor:**
    *   `express`: Framework web para crear la API REST.
    *   `cors`: Middleware para permitir peticiones desde el frontend (CORS).
*   **Base de Datos (ORM):**
    *   `@mikro-orm/core`: Núcleo del ORM MikroORM.
    *   `@mikro-orm/postgresql` (o `mysql` / `sqlite` según uses): Driver de conexión a la base de datos.
    *   `@mikro-orm/reflection`: Motor de reflexión para TypeScript.
    *   `reflect-metadata`: Requerido por MikroORM para decoradores.
*   **Autenticación y Seguridad:**
    *   `jsonwebtoken`: Para generar y validar tokens JWT.
    *   `bcrypt`: Para encriptar (hashear) contraseñas.
*   **Entorno y Configuración:**
    *   `dotenv`: Para leer variables de entorno desde el archivo `.env`.

*(Para instalar todas estas dependencias de una sola vez, ejecutá `pnpm install` dentro de la carpeta del backend).*

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

3. Iniciá la aplicación
    ```bash
    pnpm dev
4. Abrí tu navegador web y entrá a la siguiente dirección: http://localhost:5173

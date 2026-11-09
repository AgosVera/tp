# Propuesta TP DSW

## Grupo
### Integrantes
51021 - Vera, Agostina<br>
51766 - Collaud Maria Victoria

### Repositorios
* [frontend app](https://github.com/Victoria-Collaud/dsw-frontend)
* [backend app](https://github.com/Victoria-Collaud/dsw-backend)

## Tema
### Descripción
* Página de un cine que permite realizar la compra de entradas y donde los usuarios también pueden registrarse, consultar películas y sus funciones. Los administradores pueden gestionar películas, géneros de película, salas y funciones para mantener actualizada la cartelera.

### Modelo
<!--imagen del modelo(https://drive.google.com/file/d/1OrZGkEuhjiOYSzRDrfIRpjYnOHMHgxqs/view); -->
<img width="1992" height="1060" alt="DER-cine" src="https://github.com/user-attachments/assets/06114639-b176-467f-8567-d8e56979506a" />
https://app.diagrams.net/#G1OrZGkEuhjiOYSzRDrfIRpjYnOHMHgxqs#%7B%22pageId%22%3A%22GNqIutAQHUyImfBTj5YL%22%7D



## Alcance Funcional 

### Alcance Mínimo

### Regularidad:
Regularidad
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Género<br>2. CRUD Sala <br>3.CRUD Película<br>4.CRUD Compra / Entrada |
|CRUD dependiente|1. CRUD Función {depende de} CRUD Película y CRUD Sala|
|Listado<br>+<br>detalle|1. Listado de películas filtrado por género o nombre, muestra título, género y clasificación => detalle CRUD Película con sinopsis, duración y funciones disponibles|
|CUU/Epic|1. Comprar  entradas para una función <br> 2. Administrar funciones disponibles de una película (idioma , horario, sala, disponibilidad, tipo de pantalla (2d, 3d)|




### Adicionales para Aprobación
|Req|Detalle|
|:-|:-
|CRUD |1. CRUD Película<br> 2. CRUD Sala <br>3. CRUD Función<br>4. CRUD Usuario<br>5. CRUD Compra / Entrada<br>6. CRUD Género|
|CUU/Epic|1. Comprar  entradas para una función<br>2. Administrar funciones disponibles de una película<br>3. Administrar películas|






### Alcance Adicional Voluntario
|Req|Detalle|
|:-|:-|
|Listados|1. Listado de compras filtrado por usuario o fecha, muestra película, función, cantidad de entradas y tota<br>2. Listado de funciones del día filtrado por película o sala, muestra horario, sala y cantidad de asientos disponibles|
|CUU/Epic|1. Seleccionar asientos específicos dentro de la sala|
|Otros|1. Envío de comprobante por email<br>2. Generación de QR para la entrada<br>3. Dashboard de administrador con estadísticas de ventas|



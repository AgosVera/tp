# Propuesta TP DSW

## Grupo
### Integrantes
*51021 - Vera, Agostina
*51766 - Collaud Maria Victoria

### Repositorios
* [frontend app](http://hyperlinkToGihubOrGitlab)
* [backend app](http://hyperlinkToGihubOrGitlab)
*Nota*: si utiliza un monorepo indicar un solo link con fullstack app.

## Tema
### Descripción
* Página de un cine que gestiona la compra de entradas y  donde los usuarios pueden registrarse, consultar películas y sus funciones. Los administradores pueden gestionar películas, salas y funciones para mantener actualizada la cartelera.* 

### Modelo
![imagen del modelo]()

*https://drive.google.com/file/d/1OrZGkEuhjiOYSzRDrfIRpjYnOHMHgxqs/view?usp=sharing)

## Alcance Funcional 

### Alcance Mínimo


Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Película<br>2. CRUD Sala|
|CRUD dependiente|1. CRUD Función {depende de} CRUD Película y CRUD Sala|
|Listado<br>+<br>detalle| 1. Listado de películas filtrado por género o nombre, muestra título, género y clasificación => detalle CRUD Película con sinopsis, duración y funciones disponibles<br> 2. Listado de funciones filtrado por fecha, muestra película, sala, horario y precio => detalle CRUD Función con datos completos y asientos disponibles|
|CUU/Epic|1. Comprar entradas para una función<br>2. Administrar funciones disponibles de una película (idioma, horario, sala, disponibilidad, tipo (2d,3d)|


Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Tipo Habitacion<br>2. CRUD Servicio<br>3. CRUD Localidad<br>4. CRUD Provincia<br>5. CRUD Habitación<br>6. CRUD Empleado<br>7. CRUD Cliente|
|CUU/Epic|1. Reservar una habitación para la estadía<br>2. Realizar el check-in de una reserva<br>3. Realizar el check-out y facturación de estadía y servicios|


### Alcance Adicional Voluntario

*Nota*: El Alcance Adicional Voluntario es opcional, pero ayuda a que la funcionalidad del sistema esté completa y será considerado en la nota en función de su complejidad y esfuerzo.

|Req|Detalle|
|:-|:-|
|Listados |1. Estadía del día filtrado por fecha muestra, cliente, habitaciones y estado <br>2. Reservas filtradas por cliente muestra datos del cliente y de cada reserve fechas, estado cantidad de habitaciones y huespedes|
|CUU/Epic|1. Consumir servicios<br>2. Cancelación de reserva|
|Otros|1. Envío de recordatorio de reserva por email|


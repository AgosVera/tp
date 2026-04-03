# Propuesta TP DSW

## Grupo
### Integrantes
51021 - Vera, Agostina<br>
51766 - Collaud Maria Victoria

### Repositorios
* [frontend app](http://hyperlinkToGihubOrGitlab)
* [backend app](http://hyperlinkToGihubOrGitlab)
*Nota*: si utiliza un monorepo indicar un solo link con fullstack app.

## Tema
Página de cine

### Descripción
Página de un cine que gestiona la compra de entradas y  donde los usuarios pueden registrarse, consultar películas y sus funciones. Los administradores pueden gestionar películas, salas y funciones para mantener actualizada la cartelera.

### Modelo
![imagen del modelo](<img width="1089" height="566" alt="dsw cine drawio" src="https://github.com/user-attachments/assets/2c27b864-81f3-493f-95ea-b20e7a82525f" />
)

https://drive.google.com/file/d/1OrZGkEuhjiOYSzRDrfIRpjYnOHMHgxqs/view?usp=sharing

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
|CRUD |1. CRUD Película<br>2. CRUD Sala<br>3. CRUD Función<br>4. CRUD Usuario<br>5. CRUD Compra/Entrada|
|CUU/Epic|1. Comprar una entrada para una función<br>2. Administrar funciones disponibles de una película<br>3. Administrar películas<br>4. Recomendar películas|


### Alcance Adicional Voluntario


|Req|Detalle|
|:-|:-|
|Listados ||
|CUU/Epic|1. Seleccionar asientos específicos dentro de la sala|
|Otros|1. Envío de comprobante por email<br>2. Generación de QR para la entrada|


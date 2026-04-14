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

<img width="1090" height="559" alt="dsw cine drawio" src="https://github.com/user-attachments/assets/53d5016b-a4db-40aa-89f7-1ae23998051b" />

https://drive.google.com/file/d/1OrZGkEuhjiOYSzRDrfIRpjYnOHMHgxqs/view?usp=sharing

## Alcance Funcional 

### Alcance Mínimo


Regularidad:
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Género<br>2. CRUD Sala|
|CRUD dependiente|1. CRUD Función {depende de} CRUD Película y CRUD Sala<br>2. CRUD Película {depende de} CRUD Género|
|Listado<br>+<br>detalle| 1. Listado de películas filtrado por género o nombre, muestra título, género y clasificación => detalle CRUD Película con sinopsis, duración y funciones disponibles|
|CUU/Epic|1. Comprar entradas para una función<br>2. Administrar funciones disponibles de una película (idioma, horario, sala, disponibilidad, tipo (2d,3d)<br>3. Administrar películas|


Adicionales para Aprobación
|Req|Detalle|
|:-|:-|
|CRUD |1. CRUD Película<br>2. CRUD Sala<br>3. CRUD Función<br>4. CRUD Usuario<br>5. CRUD Compra/Entrada<br>6. CRUD Género|
|CUU/Epic|1. Comprar entradas para una función<br>2. Administrar funciones disponibles de una película<br>3. Administrar películas|


### Alcance Adicional Voluntario


|Req|Detalle|
|:-|:-|
|Listados ||
|CUU/Epic|1. Seleccionar asientos específicos dentro de la sala|
|Otros|1. Envío de comprobante por email<br>2. Generación de QR para la entrada|


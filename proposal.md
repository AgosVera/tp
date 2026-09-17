# Propuesta TP DSW

## Grupo
### Integrantes
*51021 - Vera, Agostina<br>
*51766 - Collaud Maria Victoria

### Repositorios
* [frontend app](http://hyperlinkToGihubOrGitlab)
* [backend app](https://github.com/Victoria-Collaud/dsw-backend)

## Tema
### Descripción
* Página de un cine que gestiona la compra de entradas y  donde los usuarios pueden registrarse, consultar películas y sus funciones. Los administradores pueden gestionar películas, salas y funciones para mantener actualizada la cartelera.* 

### Modelo
<!--imagen del modelo(https://drive.google.com/file/d/1OrZGkEuhjiOYSzRDrfIRpjYnOHMHgxqs/view); -->

<img width="1089" height="559" alt="dsw cine drawio (1)" src="https://github.com/user-attachments/assets/cca08a9f-d362-41c4-b044-f7d50c0804c2" />


## Alcance Funcional 

### Alcance Mínimo

### Regularidad:
Regularidad
|Req|Detalle|
|:-|:-|
|CRUD simple|1. CRUD Género<br>2. CRUD Sala <br>3.CRUD Película |
|CRUD dependiente|1. CRUD Función {depende de} CRUD Película y CRUD Sala|
|Listado<br>+<br>detalle|1. Listado de películas filtrado por género o nombre, muestra título, género y clasificación => detalle CRUD Película con sinopsis, duración y funciones disponibles|
|CUU/Epic|1. Comprar  entradas para una función<br>2. Administrar funciones disponibles de una película (idioma , horario, sala,disponibilidad, tipo (2d,3d)<br>3. Administrar películas|




### Adicionales para Aprobación
|Req|Detalle|
|:-|:-
|CRUD |1. CRUD Película<br> 2. CRUD Sala <br>3. CRUD Función<br>4. CRUD Usuario<br>5. CRUD Compra / Entrada<br>6. CRUD Género|
|CUU/Epic|1. Comprar  entradas para una función<br>2. Administrar funciones disponibles de una película<br>3. Administrar películas|






### Alcance Adicional Voluntario
|Req|Detalle|
|:-|:-|
|Listados|1. Listado de compras filtrado por usuario o fecha, muestra película, función, cantidad de entradas y tota<br>2. Listado de funciones del día filtrado por película o sala, muestra horario, sala y cantidad de asientos disponibles|
|CUU/Epic|1. Cancelar una compra antes del horario de la función<br>2. Seleccionar asientos específicos dentro de la sala|
|Otros|1. Envío de comprobante por email<br>2. Generación de QR para la entrada<br>3. Dashboard de administrador con estadísticas de ventas|



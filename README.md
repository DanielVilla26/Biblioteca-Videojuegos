

## Hola, esta es la Arquitectura

    controller -> service -> repository -> model

## estas son las Jerarquía de clases

    ContenidoDigital (abstracta)
     |- JuegoFisico   precio = (precioBase * dias) + 2.00
     |- JuegoDigital  precio = precioBase * dias (-10% si tamanoGB > 50)

    Cliente: máximo 3 juegos alquilados a la vez

## como lo pueden Ejecutar
Requiere JDK 17 y Maven.

    mvn spring-boot:run

Queda en http://localhost:8080

## y estos son los Endpoints 
| Método | Ruta | Body |
|---|---|---|
| POST | /api/juegos/fisico | {"titulo":"Zelda","anioLanzamiento":2017,"precioBase":3.5,"pesoGramos":120} |
| POST | /api/juegos/digital | {"titulo":"Hades","anioLanzamiento":2020,"precioBase":2.0,"tamanoGB":60} |
| GET | /api/juegos | - (solo disponibles) |
| POST | /api/clientes | {"nombre":"Ana","email":"ana@mail.com"} |
| POST | /api/prestamos/alquilar | {"clienteId":1,"juegoId":1,"dias":4} |





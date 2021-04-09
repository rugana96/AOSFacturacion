Especificación de una API de facturas de un taller.

La operación get devuelve todas las facturas.
La operación fget devuelve una factura por su facturaId.
La operación uget devuelve todas las facturas de un usuario por su userId.
La operación vget devuelve todas las facturas de un vehículo por su vehiculoId.
La operación post genera la factura de un usuario.
La operación delete elimina una factura por su facturaId.
La operación put actualiza una factura.
La operación options muestra una lista de los métodos soportados.
La operación foptions muestra una lista de los métodos soportados para facturaId.
La operación voptions muestra una lista de los métodos soportados para vehiculoId.
La operación uoptions muestra una lista de los métodos soportados para userId.
Hemos decidido implementar cuatro tipos búsquedas:
1- Busca todas las facturas existentes.
2- Busca una factura por su facturaId.
3- Busca todas las facturas de un usuario por su userId. Ya que hemos pensado que puede ser interesante buscar todas las facturas de un usuario.
4- Busca todas las facturas de un vehículo por su vehiculoId. Ya que hemos pensado que puede ser interesante buscar todas las facturas de un vehículo.

# Especificación OpenAPI de un servicio de facturación de un taller 👨‍🔧
Proyecto de la asignatura Arquitectura Orientada a Servicios (AOS) de la Universidad Politécnica de Madrid (UPM) que consiste en la especificación de una API para la implementación de un servicio de facturación de trabajos de un taller.

## Participantes 👨‍🎓
  * Rubén Gago Navarro (r.gago@alumnos.upm.es)

## Decisiones de diseño 🔧
Para implementar el diseño, hemos utilizado diferentes fuentes, entre ellas las clases grabadas, el repositorio creado en clase con la especificación de comandas y el OpenAPI map.
Tal y como se ha enseñado en la asignatura, hemos separado la API en diferentes ficheros.
  * La operación get devuelve todas las facturas.
  * La operación fget devuelve una factura por su facturaId.
  * La operación uget devuelve todas las facturas de un usuario por su userId.
  * La operación vget devuelve todas las facturas de un vehículo por su vehiculoId.
  * La operación post genera la factura de un usuario.
  * La operación delete elimina una factura por su facturaId.
  * La operación put actualiza una factura.
  * La operación options muestra una lista de los métodos soportados.
  * La operación foptions muestra una lista de los métodos soportados para facturaId.
  * La operación voptions muestra una lista de los métodos soportados para vehiculoId.
  * La operación uoptions muestra una lista de los métodos soportados para userId.
  * Hemos decidido implementar cuatro tipos búsquedas
    1. Busca todas las facturas existentes.
    2. Busca una factura por su facturaId.
    3. Busca todas las facturas de un usuario por su userId. Ya que hemos pensado que puede ser interesante buscar todas las facturas de un usuario.
    4. Busca todas las facturas de un vehículo por su vehiculoId. Ya que hemos pensado que puede ser interesante buscar todas las facturas de un vehículo.

## Despliegue 🚀
Para desarrollar la API hemos probado varias herramientas, finalmente decidimos usar el editor de swagger y stoplight.
Para crear una imagen docker de Swagger editor:

1. Abrir la aplicación de docker para escritorio
2. Pull de la imagen:
	docker pull swaggerapi/swagger-editor
3. Run contenedor:
	docker run -d -p 80:8080 swaggerapi/swagger-editor
4. Abrir el navegador y escribir localhost o localhost:80

Se pueden omitir los pasos 2 y 3 lanzando el siguiente script en la consola donde se utilice Docker. Este script se encuentra
en el directorio root del proyecto.
	./docker_swagger.sh

Para parar la imagen:
1. docker ps
2. Copiar id de la imagen (Primer valor)
3. docker stop id_imagen (id_imagen es el valor copiado en el paso 2)

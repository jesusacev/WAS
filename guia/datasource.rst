Crear Datasource en WAS (Websphere Application Server) 8.0
++++++++++++

- Primero procedemos a crear un authentication alias. Ingresamos a la consola administrativa de WAS y seleccionamos la pestaña Security, y luego Global Security::


.. image:: ../imagenes/datasource/053.png


- Luego en la pestaña Java Authentication y Autoritazion Service, seleccionamos J2C authentication data:


.. image:: ../imagenes/datasource/054.png


- Seleccionamos New para crear los datos de autenticación:


.. image:: ../imagenes/datasource/055.png


- Ingresamos el alias, el usuario, el password y la descripción. Luego que le damos ok, guardamos los cambios:


.. image:: ../imagenes/datasource/056.png


- Seguidamente creamos el JDBC provider, que es es el driver que nos va a permitir la conexión hacia la base de datos:


.. image:: ../imagenes/datasource/057.png


- En la pestaña que tiene por defecto All scopes, seleccionamos el nodo y el server:


.. image:: ../imagenes/datasource/058.png


- Seleccionamos la opción New para crear el nuevo JDBC provider:


.. image:: ../imagenes/datasource/059.png


- Colocamos el tipo de base de datos, el nombre y la descripción:


.. image:: ../imagenes/datasource/060.png


- Le decimos la ruta del sistema operativo a donde se encuentra el JDBC que vamos a utilizar:


.. image:: ../imagenes/datasource/061.png


- Nos muestra un resumen de la creación:


.. image:: ../imagenes/datasource/062.png


- Ya el jdbc fue creado y le damos a guardar:


.. image:: ../imagenes/datasource/063.png


- Luego en la misma pestaña de JDBC en el menú principal, seleccionamos Data sources. Donde dice All scopes colocamos el nodo y el server:


.. image:: ../imagenes/datasource/064.png


- Seleccionamos New para crear el nuevo datasource:


.. image:: ../imagenes/datasource/065.png


- Ingresamos el nombre del datasource y del JNDI:


.. image:: ../imagenes/datasource/066.png


- Seleccionamos el JDBC provider ya creado previamente:


.. image:: ../imagenes/datasource/067.png


- Indicamos la URL de la base de datos:


.. image:: ../imagenes/datasource/068.png


- Seleccionamos el authentication alias creado con anterioridad:


.. image:: ../imagenes/datasource/069.png


- Nos muestra el resumen de la creación del datasource y le damos finalizar:


.. image:: ../imagenes/datasource/070.png


- Una vez creado el datasource le damos a la opción guardar:


.. image:: ../imagenes/datasource/071.png


- Nos muestra un mensaje que el datasource fue creado satisfactoriamente:


.. image:: ../imagenes/datasource/072.png 


- Procedemos a crear un segundo datasource que incluirá los mismos pasos para fines de practica:


.. image:: ../imagenes/datasource/073.png


.. image:: ../imagenes/datasource/074.png


.. image:: ../imagenes/datasource/075.png


.. image:: ../imagenes/datasource/076.png


.. image:: ../imagenes/datasource/077.png


.. image:: ../imagenes/datasource/078.png


.. image:: ../imagenes/datasource/079.png


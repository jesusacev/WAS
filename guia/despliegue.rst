Desplegar en WAS (Websphere Application Server) 8.0
++++++++++++


- En el menú principal de la consola administrativa, seleccionamos Applications --> Applications types --> WebSphere enterprise applications. Luego seleccionamos la opción Install para realizar un nuevo despliegue:


.. image:: ../imagenes/despliegue/Selección_068.png


- Elegimos la opción Remote file system en nuestro caso, ya que tenemos el ear en una ruta del servidor de aplicación:


.. image:: ../imagenes/despliegue/Selección_069.png


- Seleccionamos el servidor y el nodo:


.. image:: ../imagenes/despliegue/Selección_070.png


- Nos muestra el directorio raíz a donde buscaremos la ruta del ear:


.. image:: ../imagenes/despliegue/Selección_071.png


- Seleccionamos el ear:


.. image:: ../imagenes/despliegue/Selección_072.png


- Luego que seleccionamos el archivo, le damos a la opción next:


.. image:: ../imagenes/despliegue/Selección_073.png


- Nos pregunta como queremos instalar la aplicación y le decimos que detallada, ya que tenemos que asociar una shared librarie mas adelante:


.. image:: ../imagenes/despliegue/Selección_074.png


-Las opciones siguientes las dejamos por defecto:


.. image:: ../imagenes/despliegue/Selección_075.png


- La opción mapear módulos a servidores la dejamos por defecto:


.. image:: ../imagenes/despliegue/Selección_076.png


- Las opciones de recarga jsp también las dejamos por defecto:


.. image:: ../imagenes/despliegue/Selección_077.png


- Llegó el momento de mapear la shared librarie. Esto debe ser previamente conversado con el desarrollador o un arquitecto java, que son los que conocen mejor la aplicación:


.. image:: ../imagenes/despliegue/Selección_078.png


- En nuestro caso la vamos a agregar al módulo de WController.war, por lo que lo seleccionamos y le damos a "Reference shared libraries":


.. image:: ../imagenes/despliegue/Selección_079.png


- Debemos mover a seleccionados el shared librarie WCONTROLLER_LIB, que fue previamente creado en la sección **Creación de Shared Libraries en WAS (Websphere Application Server) 8.0**:


.. image:: ../imagenes/despliegue/Selección_080.png


.. image:: ../imagenes/despliegue/Selección_081.png


- Ya podemos observar el shared librarie asociado:


.. image:: ../imagenes/despliegue/Selección_082.png


- La siguiente opción de shared librarie la dejamos por defecto:


.. image:: ../imagenes/despliegue/Selección_083.png


- Inicializamos todos los parámetros por defecto:


.. image:: ../imagenes/despliegue/Selección_084.png


.. image:: ../imagenes/despliegue/Selección_085.png


.. image:: ../imagenes/despliegue/Selección_086.png


- El mapeo de los virtual hosts también queda por defecto:


.. image:: ../imagenes/despliegue/Selección_087.png


- En el "Map context roots for Web modules" y en el "Maps JASPI provider" tampoco modificamos nada:


.. image:: ../imagenes/despliegue/Selección_088.png


.. image:: ../imagenes/despliegue/Selección_089.png


- Nos muesta los módulos de compilación y le damos a siguiente:


.. image:: ../imagenes/despliegue/Selección_090.png


- Nos muestra el resumen de la instalación y luego finalizamos:


.. image:: ../imagenes/despliegue/Selección_091.png


- Nos dirá que está instalando, y si sale todo bien nos mostrará un mensaje que la aplicación fue instalada satisfactoriamente, y luego le damos a guardar:


.. image:: ../imagenes/despliegue/Selección_092.png


- Ya podemos observar la aplicación, pero la misma se encuentra detenida:


.. image:: ../imagenes/despliegue/Selección_093.png


- En este caso tenemos que hacer una configuración adicional, recomendada por un arquitecto java para el correcto funcionamiento de la aplicación. Damos click sobre el ear, y le damos a la opción "Class loadind and update detection":


.. image:: ../imagenes/despliegue/Selección_094.png


- Y en la opción "WAR class loader policy" seleccionamos "Single class loader for application":


.. image:: ../imagenes/despliegue/Selección_095.png


- Procedemos a guardar los cambios:


.. image:: ../imagenes/despliegue/Selección_096.png


- Luego iniciamos la aplicación a través del botón start:


.. image:: ../imagenes/despliegue/Selección_100.png


- Finalmente probamos el ingreso a la aplicación:


.. image:: ../imagenes/despliegue/Selección_097.png


.. image:: ../imagenes/despliegue/Selección_098.png


.. image:: ../imagenes/despliegue/Selección_099.png





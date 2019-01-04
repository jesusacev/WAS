Instalación de WAS (Websphere Application Server) 8.0
++++++++++++

- Ingresamos vía ssh al servidor con el parámetro de las X, para realizar la instalación. Ya debemos tener instalado el Instalation Manager de IBM y creado un usuario de servicio::


	$ ssh -X ibm@192.168.0.237
	ibm@192.168.0.237's password: 
	Last login: Thu Jan  3 15:36:12 2019 from 192.168.0.43


- Creamos la carpeta was para descomprimir el empaquetado de was 8::


	[ibm@was IBM]$ mkdir was
	[ibm@was IBM]$ ls
	IM  Instaladores  was
	[ibm@was IBM]$ pwd
	/opt/IBM
	$ cd was/
	[ibm@was was]$ ls
	was8.tar
	[ibm@was was]$ tar -xvf was8.tar


- Luego nos vamos a la carpeta de IM, seguidamente InstallationManager, y luego eclipse y ejecutamos el script IBMIM para iniciar la instalación::


	[ibm@was was]$ cd ..
	[ibm@was IBM]$ cd IM/
	[ibm@was IM]$ cd InstallationManager/
	[ibm@was InstallationManager]$ cd eclipse/
	[ibm@was eclipse]$ ./IBMIM


- Lo primero que nos mostrará la ventana de instalación::


.. image:: ../imagenes/was/036.png


- Luego le damos al boton de Archivo y preferencias:


.. image:: ../imagenes/was/037.png


- Le damos a añadir repositorios:


.. image:: ../imagenes/was/038.png


- Buscamos la ruta a donde descomprimimos el paquete de was8, y seleccionamos repository.config para agregarlo:


.. image:: ../imagenes/was/039.png


- Añadimos el repositorio:


.. image:: ../imagenes/was/040.png


- Y ya lo podemos observar en la lista de repositorios y le damos a aceptar:


.. image:: ../imagenes/was/041.png


- Luego volvemos a la pantalla de Instalación y seleccionamos instalar, valga la redundancia:


.. image:: ../imagenes/was/042.png


- Nos muestra el paquete de instalación y le damos a siguiente:


.. image:: ../imagenes/was/043.png


- Aceptamos la licencia:


.. image:: ../imagenes/was/044.png


- Indicamos la ubicación del directorio de recursos compartidos:


.. image:: ../imagenes/was/045.png


- Luego indicamos el directorio de instalación:


.. image:: ../imagenes/was/046.png


- Seleccionamos el la traducción de español por motivos de lengua nativa:


.. image:: ../imagenes/was/047.png


- Dejamos las caraterísticas por defecto y seleccionamos siguiente:


.. image:: ../imagenes/was/048.png


- Al final nos mostrará el resumen y de estar todo bien, procedemos a instalar:


.. image:: ../imagenes/was/049.png


.. image:: ../imagenes/was/050.png


- Luego nos mostrará un mensaje de que los paquetes se han instalado correctamente:


.. image:: ../imagenes/was/051.png


- Seguidamente nos abre el toolbox para crear el perfil:


.. image:: ../imagenes/was/052.png


- Seleccionamos el tipo de entorno que en este caso es servidor de aplicación:


.. image:: ../imagenes/was/053.png


- Le damos a la opción de creación de perfiles avanzada:


.. image:: ../imagenes/was/054.png


- Seleccionamos las 2 opciones de despliegue de aplicaciones:


.. image:: ../imagenes/was/055.png


- Colocamos el nombre del perfil y el directorio a donde se va a crear:


.. image:: ../imagenes/was/056.png


- Colocamos el nombre del nodo, el nombre del servidor y el nombre del host:


.. image:: ../imagenes/was/057.png


- Ingresamos el usuario administrativo y su contraseña:


.. image:: ../imagenes/was/058.png


- En las opciones de certificados le damos a crear un nuevo certificado personal por omisión para que lo cree por defecto:


.. image:: ../imagenes/was/059.png


- Nos mostrará los datos de los certificados y la CA emitidos y el tiempo de caducidad:


.. image:: ../imagenes/was/060.png


- Luego podemos ver los puertos por defecto que utilizará la aplicación los cuales podemos modificar a nuestra conveniencia:


.. image:: ../imagenes/was/061.png


- Al seguir de manera opcional podemos configurar un servidor web para direccionar peticiones al servidor de aplicación. Pero en este caso no lo haremos:


.. image:: ../imagenes/was/062.png


- Nos muestra el resumen de la creación del perfil:


.. image:: ../imagenes/was/063.png


- Carga el proceso de creación de perfiles:


.. image:: ../imagenes/was/064.png


- Nos debe indicar que el perfil se a creado exitosamente y le damos finalizar:


.. image:: ../imagenes/was/065.png


- Nos aparecerá la ventana de Primeros Pasos para verificación de funcionalidades, que puede comprobar si gusta:


.. image:: ../imagenes/was/066.png


- Si no iniciamos el servidor en la ventana de primeros pasos, lo iniciamos de forma manual con el script startServer.sh, que en nuestro caso está en la ruta /opt/IBM/was/WebSphere/AppServer/profiles/Venezuela/bin. Aquí estamos levantando el perfil, incluyendo los puertos del server y de la consola administrativa::

	[ibm@was bin]$ ./startServer.sh was1
	ADMU0116I: La información de la herramienta se está anotando en el archivo
		   /opt/IBM/was/WebSphere/AppServer/profiles/Venezuela/logs/was1/startServer.log
	ADMU0128I: Iniciando herramienta con el perfil Venezuela
	ADMU3100I: Leyendo la configuración para el servidor: was1
	ADMU3200I: El servidor se ha iniciado. Esperando el estado de inicialización.
	ADMU3000I: Servidor was1 abierto para e-business; el ID de proceso es 6902


- Consultamos la consola administrativa vía web, a través del puerto que le definimos en la creación del perfil (se deben tomar en cuenta las iptables), e ingresamos con el usuario creado durante la instalación:


.. image:: ../imagenes/was/067.png


- Ingresamos satisfactoriamente a la consola de administración:


.. image:: ../imagenes/was/068.png


- Si ingresamos a servidores de aplicación de Websphere, podremos ver dicho servidor con su nodo y el nombre del host en que fue instalado:


.. image:: ../imagenes/was/069.png

	


















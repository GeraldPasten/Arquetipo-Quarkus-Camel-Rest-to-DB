# baseservice-rest-databese-crud

Aplicación desarrollada utilizando Quarkus, Camel 3, JPA, Hibernate y rutas REST. La aplicación realiza operaciones CRUD en una base de datos utilizando JPA, y utiliza Camel para exponer puntos de acceso REST. También se proporcionan ejemplos de cómo manejar logs en Camel y configuraciones de Quarkus, cómo manejar excepciones, procesar datos de consultas y aplicar lógica de negocios. Además, se incluyen pruebas JUnit 5 con Camel y una carpeta "openshift" con configuraciones de rutas para OpenShift.

# Contenido
- [x] Endpoints Rest Camel
- [x] Recibir y producir JSON
- [x] Despliegue en ocp / Comandos OC
- [x] Carpeta Openshift
- [x] Parametrizacion y Configuracion
- [x] CRUD en JPA mediante CAMEL
- [x] Logica de negocios en rutas Camel
- [x] Configuracion de Logs 
- [x] Manejo de excepciones
- [x] Junit Test con Camel

# Tecnologías utilizadas
Quarkus: Un framework de Java diseñado para aplicaciones nativas de la nube.
Camel 3: Un framework de integración de código abierto que permite la implementación de patrones de integración empresarial.
JPA (Java Persistence API): Una API estándar de Java para mapear objetos a bases de datos relacionales.
Hibernate: Una implementación de JPA que proporciona una capa de persistencia para el acceso a bases de datos.
REST: Un estilo arquitectónico para construir servicios web escalables y fáciles de consumir.

# Configuración
La configuración de la aplicación se encuentra en el archivo application.properties en la carpeta resources. Aquí se pueden ajustar diversos aspectos, como la configuración de la base de datos, los logs y otras propiedades específicas de Quarkus.

# Uso de Camel para rutas REST
La clase UsuarioResource utiliza Camel para definir rutas REST que se encargan de manejar las operaciones CRUD de la entidad Usuario. Se pueden agregar más rutas o modificar las existentes según sea necesario para adaptarse a los requisitos específicos del proyecto.

# Manejo de logs
La configuración de logs se encuentra en el archivo application.properties. Aquí se pueden ajustar los niveles de log para diferentes paquetes y clases, así como configurar la salida de los logs.

Además, Camel proporciona su propio mecanismo de logging que se puede configurar mediante opciones específicas en las rutas.

# Manejo de excepciones
La aplicación muestra ejemplos de cómo manejar excepciones utilizando Camel. Se pueden agregar manejadores de excepciones personalizados en las rutas para capturar y manejar excepciones específicas según sea necesario.

# Consultas y lógica de negocios
La clase UsuarioService implementa la lógica de negocio relacionada con el manejo de usuarios. Aquí se pueden realizar consultas a la base de datos utilizando JPA y aplicar lógica de negocio adicional según sea necesario.

# Pruebas JUnit 5 con Camel
La clase UsuarioServiceTest en el directorio test contiene pruebas unitarias utilizando JUnit 5 y Camel. Estas pruebas permiten verificar el comportamiento esperado de los diferentes métodos de la clase UsuarioService.

# Configuraciones de rutas para OpenShift
La carpeta openshift contiene el archivo route-config.yaml, que proporciona configuraciones de rutas para OpenShift. Estas configuraciones se pueden utilizar para exponer los puntos de acceso REST de la aplicación en un clúster de OpenShift.

# Comandos
A continuación se presentan algunos comandos útiles para utilizar la aplicación:

# Crear nuestro arquertipo
Creando una nueva carpeta a la altura raiz y abriendo una terminal, podemos utilizar este comando para generar un proyecto base.

mvn archetype:generate   
-DarchetypeGroupId=com.mx.banorte.services   
-DarchetypeArtifactId=baseservice-rest-databese-crud-archetype   
-DarchetypeVersion=1.0.0-SNAPSHOT   
-DgroupId=com.example   
-DartifactId=my-project   
-Dversion=1.0.0   
-Dpackage=com.example.myproject

    -DarchetypeGroupId: Especifica el ID del grupo (Group ID) del arquetipo que deseas utilizar para generar el proyecto. En este caso, el valor es com.mx.banorte.services.

    -DarchetypeArtifactId: Especifica el ID del artefacto (Artifact ID) del arquetipo que deseas utilizar. En este caso, el valor es baseservice-rest-databese-crud-archetype.

    -DarchetypeVersion: Especifica la versión del arquetipo que deseas utilizar. En este caso, el valor es 1.0.0-SNAPSHOT.

    -DgroupId: Especifica el ID del grupo (Group ID) que se utilizará para el nuevo proyecto que se generará. En este caso, el valor es com.example. Puedes ajustar este valor según tu propia estructura de paquetes y convenciones de nomenclatura.

    -DartifactId: Especifica el ID del artefacto (Artifact ID) para el nuevo proyecto. En este caso, el valor es my-project. Puedes ajustar este valor según el nombre que desees darle a tu proyecto.

    -Dversion: Especifica la versión del nuevo proyecto. En este caso, el valor es 1.0.0. Puedes ajustar este valor según tus propias convenciones de versión.

    -Dpackage: Especifica el paquete base que se utilizará para las clases generadas en el nuevo proyecto. En este caso, el valor es com.example.myproject. Puedes ajustar este valor según tu propia estructura de paquetes.

    El comando mvn archetype:generate combina estos parámetros para generar un nuevo proyecto utilizando el arquetipo especificado. El resultado será una estructura de proyecto básica con la configuración y los archivos iniciales necesarios para comenzar a desarrollar






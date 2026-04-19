# COMPLETAR  
Comparando sus conocimientos antes de hacer la práctica con sus conocimientos después de hacer la tarea, explicar los principales aprendizajes logrados para beneficio de su formación profesional.  

1. Conectar varios contenedores sobre una o varias redes, para poder desplegar servicios y que estos contenedores se comuniquen entre si.
2. Comprender los comandos para crear, correr e inspeccionar redes.
3. Establecer variables de entorno necesarias para arrancar contenedores o desplegar servicios.

Si solucionó un problema presentado al realizar la práctica también se debe documentar.

Consultar: Cómo se gestionan datos confidenciales con los secretos de Docker (Docker Secrets).

Los Docker Secrets son un mecanismo que permite gestionar información sensible —como contraseñas, claves API o certificados— de forma segura dentro de Docker, evitando exponer estos datos directamente en variables de entorno o en el código de la aplicación.

La idea principal es que, en lugar de pasar credenciales directamente al contenedor (por ejemplo, usando variables de entorno con -e, lo cual es inseguro porque pueden verse con comandos como docker inspect), se crean objetos llamados “secrets” que Docker almacena de manera protegida. Estos secretos son entregados únicamente a los contenedores que los necesitan y se montan como archivos temporales dentro de ellos.

Para utilizar Docker Secrets, primero se debe crear el secreto. Esto se puede hacer leyendo el contenido desde la entrada estándar, por ejemplo, una contraseña. Luego, es necesario trabajar con Docker en modo Swarm, ya que esta funcionalidad no está disponible con el uso tradicional de docker run. Para ello, se inicializa Docker Swarm y posteriormente se crea un servicio que utilice el secreto.

Cuando un contenedor recibe un secreto, Docker lo monta automáticamente en una ruta interna, generalmente dentro del directorio /run/secrets/. La aplicación dentro del contenedor puede leer este archivo para obtener el valor sensible. Por ejemplo, en el caso de bases de datos como MySQL, en lugar de pasar directamente la contraseña, se puede indicar una variable especial que apunte al archivo del secreto.

Este enfoque ofrece varias ventajas. En primer lugar, mejora la seguridad, ya que los secretos no se exponen en texto plano ni en logs. Además, el acceso está controlado y limitado solo a los servicios autorizados. Sin embargo, también presenta algunas limitaciones, como el hecho de que solo funciona en modo Swarm y no en ejecuciones simples con docker run. En entornos de desarrollo, muchas veces se utilizan alternativas como archivos .env o configuraciones en docker-compose, aunque estas no ofrecen el mismo nivel de seguridad.

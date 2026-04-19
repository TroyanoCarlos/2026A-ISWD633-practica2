## Esquema para el ejercicio
![Imagen](esquema-4-ejercicio.PNG)

### Crear la red
# COMPLETAR

### Crear el contenedor mysql a partir de la imagen mysql:8, configurar las variables de entorno necesarias
# COMPLETAR

### Crear el contenedor wordpress a partir de la imagen: wordpress, configurar las variables de entorno necesarias
# COMPLETAR

De acuerdo con el trabajo realizado, en el esquema del ejercicio el puerto a es 8080

Ingresar desde el navegador al wordpress y finalizar la configuración de instalación.
# COLOCAR UNA CAPTURA DE LA CONFIGURACIÓN

<img width="1913" height="920" alt="image" src="https://github.com/user-attachments/assets/414d8fe4-d20c-4ee6-a19c-dadad8e1d442" />

Desde el panel de admin: cambiar el tema y crear una nueva publicación.
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress
# COLOCAR UNA CAPTURA DEL SITO EN DONDE SEA VISIBLE LA PUBLICACIÓN.
<img width="1919" height="961" alt="image" src="https://github.com/user-attachments/assets/ab40db8f-c485-486e-aade-93e881553390" />

### Eliminar el contenedor wordpress
# COMPLETAR

### Crear nuevamente el contenedor wordpress
Ingresar a: http://localhost:9300/ 
recordar que a es el puerto que usó para el mapeo con wordpress

### ¿Qué ha sucedido, qué puede observar?
# COMPLETAR
<img width="1757" height="642" alt="image" src="https://github.com/user-attachments/assets/961c75ce-392f-4d7d-94d3-b6dd01cdaad6" />

A pesar de haber eliminado el contenedor de wordpress, la configuración del usuario que ingresa a wordpress se mantuvo, con un mensaje dando a entender que si se quisiera reiniciar estos datos se deberia eliminar la base de datos en MySQL.

Al ingresar con el usuario que ya se había registrado para wordpress, la publicación creada persistío, dando a entender que tanto credenciales de wordpress como publicaciones quedan alojadas en la base de datos dentro del contenedor mysql

<img width="1919" height="899" alt="image" src="https://github.com/user-attachments/assets/7e91ee90-9eda-447d-a49c-af4990b3ae75" />

# Variables de Entorno
### ¿Qué son las variables de entorno?

Las variables de entorno son valores almacenados en el sistema operativo que influyen en el comportamiento de procesos u operaciones. Pueden ser valores asignados, rutas especificas o credenciales. Estas variables son dinámicas e insiden en las aplicaciones según el valor que se pueda asignar o cambiar.

# COMPLETAR

### Para crear un contenedor con variables de entorno

```
docker run -d --name <nombre contenedor> -e <nombre variable1>=<valor1> -e <nombre variable2>=<valor2>
```

### Crear un contenedor a partir de la imagen de nginx:alpine con las siguientes variables de entorno: username y role. Para la variable de entorno rol asignar el valor admin.

<img width="1161" height="85" alt="image" src="https://github.com/user-attachments/assets/5af85748-fad5-4046-9dc7-fe5f93201e3d" />


# COMPLETAR

# CAPTURA CON LA COMPROBACIÓN DE LA CREACIÓN DE LAS VARIABLES DE ENTORNO DEL CONTENEDOR ANTERIOR
<img width="1248" height="250" alt="image" src="https://github.com/user-attachments/assets/984308df-1441-4da3-8076-f105737b8a34" />


### Crear un contenedor con la imagen de mysql, mapear todos los puertos
# COMPLETAR
<img width="1086" height="350" alt="image" src="https://github.com/user-attachments/assets/3efa23b6-6dbb-41bd-be6e-919d5bd767d0" />


### ¿El contenedor se está ejecutando?
# COMPLETAR
<img width="1914" height="117" alt="image" src="https://github.com/user-attachments/assets/63c3e757-100d-4ed9-a7e1-16e6662dedc0" />

### Identificar el problema
# COMPLETAR

No se asigno una contraseña al contenedor
<img width="1377" height="244" alt="image" src="https://github.com/user-attachments/assets/7ca39800-3764-44c1-923c-2196edb9fcff" />


### Para crear un contenedor con variables de entorno especificadas
- Portabilidad: Las aplicaciones se vuelven más portátiles y pueden ser desplegadas en diferentes entornos (desarrollo, pruebas, producción) simplemente cambiando el archivo de variables de entorno.
- Centralización: Todas las configuraciones importantes se centralizan en un solo lugar, lo que facilita la gestión y auditoría de las configuraciones.
- Consistencia: Asegura que todos los miembros del equipo de desarrollo o los entornos de despliegue utilicen las mismas configuraciones.
- Evitar Exposición en el Código: Mantener variables sensibles como contraseñas, claves API, y tokens fuera del código fuente reduce el riesgo de exposición accidental a través del control de versiones.
- Control de Acceso: Los archivos de variables de entorno pueden ser gestionados con permisos específicos, limitando quién puede ver o modificar la configuración sensible.

### ¿Qué bases de datos existen en el contenedor creado?
# COMPLETAR
<img width="1909" height="713" alt="image" src="https://github.com/user-attachments/assets/926eef03-956b-4236-b4a1-c817b9b16449" />


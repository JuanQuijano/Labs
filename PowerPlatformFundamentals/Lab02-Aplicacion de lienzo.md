# Laboratorio 2: Aplicación de Lienzo
## Escenario

Seguiremos el siguiente plan para diseñar la aplicación de lienzo:
- Crearemos una aplicación de lienzo a partir de datos en la tabla Visit.
- Configuraremos la visualización de visitas en la pantalla de navegación.
- Permitiremos realizar cambios básicos en la aplicación.
- Probaremos la funcionalidad de la aplicación.

#### Requisitos previos
- Laboratorio 0: Validar el Entorno.
- Laboratorio 1: Modelado de datos.

## Ejercicio 1: crear una aplicación de lienzo de visitas

### Tarea 1: Crear la aplicación Tours
- Vaya a https://make.powerapps.com
    * Si sale el dialogo de identificación, ingrese la dirección de correo electrónico de sus credenciales de Microsoft 365 en el cuadro de texto que dice: "Ingrese su dirección de correo electrónico".
    * Ingrese la contraseña.
    * Seleccione Sí para permanecer conectado.
- Seleccione "Entorno" y, en el listado de entornos que aparece, seleccione el de "PracticaAlumno" con su número de Alumno.
- En el menú de la derecha seleccione "+ Crear".
- En la pantalla de crear aplicación escoja la opción de "Dataverse".
#### Tarea 1.1: Si no existiera la conexión al Dataverso
- En el caso de que la conexión al dataverso no exista, debe pulsar en el botón "+ Nueva conexión" del menú superior de la sección de Conexiones.
- Buscar y seleccionar la conexión de "Microsoft Dataverse" de entre el listado de conexiones.
- Pulsar el botón de "Crear".
- Seleccionar la cuenta de alumno que se le ha asignado.
- Pulsar en el botón de "Allow access".
- Localizar y seleccionar la tabla de "Visit". Puede utilizar el buscador de la esquina superior derecha para facilitar la búsqueda de la tabla.
- Pulsar en el botón de la esquina inferior derecha "Conectar".

Si aparece la pantalla de Bienvenida a Power Apps Studio, pulse en el botón de "Omitir".
- En el menú superior izquierdo (el que está justo debajo del menú con fondo fucsia), pulse en el icono de "Vista previa de la aplicación", Y compruebe que la aplicación funciona correctamente.
- Cierre la pantalla de Vista previa en la "X" en la esquina superior derecha.

### Tarea 2: Edite la aplicación creada y defina un Tema de colores
Ahora vamos a modificar ligeramente el diseño de la aplicación.
- Seleccione la etiqueta de "Visit" en la pantalla de la aplicación. A la derecha se abre la sección de configuración del objeto seleccionado.
- Cambie el texto a "Bellows College Tours".
Como se observa, no se visualiza toda la línea de ´texto, por lo cual vamos a corregirlo.
- Cambie el Tamaño de la fuente de 27 a 24, y pulse la tecla "Enter".

Ahora vamos a realizarlo en las otras pantallas de la aplicación.

- En la sección de "Vista de árbol" a la izquierda de la pantalla de la aplicación, seleccione icono de pantalla llamado "DetailScreen1".
- Sustituya el título "Visit" por "Visit Details". Aquí no es necesario cambiar el tamaño de la fuente.
- Haga lo mismo en la pantalla EdtiScreen1, pero cambiando el título por "Edit Details".

Por último, vamos a escoger un Tema de colores para nuestra aplicación.
- En el menú superior despliegue el menú de "Tema".
- Escoja el Tema que más le guste, y espere un poco a que se actualice la aplicación.
- Pulse en cualquier lugar vacío de la pantalla para salir de la selección del Tema.

### Guarde y pruebe la aplicación
- En el menú superior, busque y pulse el símbolo de un disquete, que es el de "Guardado".
- En el nombre introduzca "Visits", y pulse en el botón "Guardar".
- Lance la vista previa de la publicación, y compruebe que todas las pantallas y controles son funcionales.

¡Ha construido su primera aplicación de lienzo con PowerApps!








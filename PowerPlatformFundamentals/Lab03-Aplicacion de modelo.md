# Laboratorio 3: Aplicación de modelo
## Escenario

Como parte de la creación de la aplicación, hará lo siguiente:

- Crear una nueva aplicación basada en modelos denominada Bellows Campus Management
- Editar la navegación de la aplicación para hacer referencia a las tablas requeridas
- Personalizar los formularios y vistas de tablas necesarios para la aplicación.

Trabajaremos con los siguientes componentes:
- Vistas: las vistas permiten al usuario ver los datos existentes en la tabla de formularios.
- Formularios: aquí es donde el usuario crea o actualiza nuevas filas en las tablas.

Ambos se integrarán en la aplicación basándose en una plantilla, para una mejor experiencia de usuario.

#### Requisitos previos
Laboratorio 0: Validar el Entorno.

Laboratorio 1: Modelado de datos.

## Ejercicio 1: personalizar las pantallas y los formularios

### Tarea 1: editar el formulario de visita
- Vaya a https://make.powerapps.com
    * Si sale el dialogo de identificación, ingrese la dirección de correo electrónico de sus credenciales de Microsoft 365 en el cuadro de texto que dice: "Ingrese su dirección de correo electrónico".
    * Ingrese la contraseña.
    * Seleccione Sí para permanecer conectado.
- Seleccione "Entorno" y, en el listado de entornos que aparece, seleccione el de "PracticaAlumno" con su número de Alumno.
- En el menú lateral de la izquierda seleccione "Tablas".
- Localice y abra la tabla "Visit".
- Dentro de la sección "Experiencias de datos", seleccione el icono de "Formularios".
- Seleccione el **Tipo de formulario** "Principal" del formulario "Information".
- En la sección de la derecha de propiedades del formulario Information, cambie el Nombre para mostrar a "Main Info".

En el panel izquierdo, llamado Columnas de tabla", agregue los siguientes campos debajo del campo Owner arrastrando las columnas al formulario o simplemente haciendo clic en los nombres de las columnas:
- Visitor
- Expected start
- Expected end
- Actual start
- Actual end

Arrastre la columna Code y suéltela en el encabezado del formulario.

El encabezado es la zona superior derecha del formulario. Es posible que deba minimizar el panel Propiedades en el lado derecho de la pantalla para ver el campo en el formulario.

-  Mantenga seleccionado el campo de "Code", y en el panel de propiedades seleccione la opción de "Solo lectura".
- Seleccione el campo "Owner", y cambie la propiedad de la Etiqueta (pone Owner) a la palabra "Host".
- En el menú superior, en la esquina de la derecha, pulse el botón de "Guardar y publicar".

Vuelva atrás pulsando en el botón de "Atrás" que está en el menú superior, en la esquina izquierda. Se abrirá la pantalla de Formularios, y podrá navegar por la miga de pan superior a la pantalla de la tabla "Visit".

### Tarea 2: Editar la Vista de visitas activas
- Dentro de la sección "Experiencias de datos", seleccione el icono de "Vistas".
- Seleccione la vista "Active Visit".
- Añada los siguientes campos arrastrándolos a la pantalla principal o haciendo click en ellos:
    * Code
    * Visitor
    * Expected start 
    * Expected end
- Expanda el menú desplegable del campo "Created On" y pulse en el icono de "Quitar"
- Amplie cada columna para que se visualice completamente el dato contenido.
- Pulse el botón de "Guardar y publicar" situado en la esquina superior derecha.

### Tarea 3: Crear una vista para las visitas de hoy
Vamos a clonar la vista actual para crear la nueva vista de las visitas de hoy.

- Pulsar el botón "Guardar como", a la izquierda del botón "Guardar y publicar".
- Cambiarle el nombre a "Today's Visits" y pulsar el botón de "Guardar".
- En el panel de propiedades, en la parte derecha de la pantalla, pulse en el enlace inferior de "Editar filtros...".
- En el filtro que está dado de alta, despliegue el menú contextual de la primera casilla y seleccione el campo "Expected start".
- En la segunda casilla despliegue el menú contextual y seleccione "hoy".
- Pulse el botón "Aceptar" en la parte inferior de la pantalla.
- Añada los campos "Actual start" y "Actual end" a la vista.
- Pulse el botón de "Guardar y publicar" situado en la esquina superior derecha.

## Ejercicio 2: Crear una aplicación basada en modelo
### Tarea 1: Crear una app
En este ejercicio, creará una aplicación basada en modelos, personalizará el mapa del sitio y probará la aplicación.

Para simplificar las cosas y debido a limitaciones de tiempo, no cubriremos algunas de las columnas de la tabla Visit en esta práctica de laboratorio.

- Vuelva a la pantalla principal de make.powerapps.com
- Pulse en el botón del menú izquierdo de "+ Crear".
- En la pantalla de "Crear aplicación" pulse en el botón de "Aplicación vacía".
- De las opciones que aparecen, pulse en el botón "Crear" de "Aplicación en blanco basada en Dataverse".
- Introduzca "Bellows Campus Management" como Nombre de la nueva aplicación basada en modelo, y pulse el botón de "Crear".
- Pulse en el botón "+ Agregar página" que está en el medio de la pantalla.
- Seleccione "Tabla de Dataverse" y pulse el botón de "Siguiente".
- Seleccione las tablas "Contact" y "Visit", y pulse el botón de "Agregar".
- En el árbol de navegación de la derecha, seleccione el nodo "Nuevo grupo".
- En la sección que se ha abierto a la derecha de la pantalla, "Opciones de visualización", cambie el Título a "Security".
- Pulse en el botón de "Guardar" que está a la izquierda en el menú superior.

### Tarea 2: Pruebe la aplicación
- Pulse el botón "publicar" que está situado en el menú superior a la derecha.
- Pulse el botón de "Reproducir" que está situado justo a la derecha del anterior.
- Compruebe que puede añadir una nueva visita que va a empezar la visita hoy, y que la terminará mañana.
- Compruebe que aparece en la vista de "Today's Visits", a la que se accede en el menú desplegable del título de la página que estamos viendo.
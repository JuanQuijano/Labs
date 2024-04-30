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

## Ejercicio 1: personalizar los pantallas y los formularios

### Tarea 1: editar el formulario de visita
- Vaya a https://make.powerapps.com
    * Si sale el dialogo de identificación, ingrese la dirección de correo electrónico de sus credenciales de Microsoft 365 en el cuadro de texto que dice: "Ingrese su dirección de correo electrónico".
    * Ingrese la contraseña.
    * Seleccione Sí para permanecer conectado.
- Seleccione "Entorno" y, en el listado de entornos que aparece, seleccione el de "PracticaAlumno" con su número de Alumno.
- En elmenú lateral de la izquierda seleccione "Tablas".
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

Vuelva atrás pulsando en el botón de "Atrás" que está en el menú superior, en la esquina izquierda. Se abrira la pantalla de Formularios, y podrá navegar por la miga de pan superior a la pnatalla de la tabla "Visit".

### Tarea 2: Editar la Vista de visitas activas
- Dentro de la sección "Experiencias de datos", seleccione el icono de "Vistas".
- 

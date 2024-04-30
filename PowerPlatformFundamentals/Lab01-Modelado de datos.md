# Laboratorio 1: Modelado de datos
## Escenario

En esta práctica de laboratorio, accederá a su entorno y creará una base de datos de Microsoft Dataverse y una solución para realizar un seguimiento de sus cambios. También creará un modelo de datos para admitir los siguientes requisitos:

R1: seguimiento de información para visitas planificadas al campus
R2: registrar información básica para identificar y rastrear visitantes
R3 - Planificar, registrar y gestionar visitas

Finalmente, importará datos de muestra a Microsoft Dataverse.

## Ejercicio 1: crear una tabla

### Tarea 1: Crear la tabla de Visit y añadir columnas
Vamos a crear la tabla de Visitas que utilizaremos en el resto de las prácticas. Para ello crearemos una nueva y le añadiremos las columnas necesarias.

- Vaya a https://make.powerapps.com
- Si sale el dialogo de identificación, ingrese la dirección de correo electrónico de sus credenciales de Microsoft 365 en el cuadro de texto que dice: "Ingrese su dirección de correo electrónico".
- Ingrese la contraseña.
- Seleccione Sí para permanecer conectado.
- Seleccione "Entorno" y, en el listado de entornos que aparece, seleccione el de "PracticaAlumno" con su número de Alumno.
- En el menú de la izquierda escoja la opción de "Tablas"·
- En el menú superior pulse en "+ Nueva Tabla" y escoja ene l menú desplegable la primera opción de "Agregar columnas y datos".
- Pinche en el lapicero al lado del nombre de la tabla "Nueva Tabla"
- Cambie el nombre de la tabla a "Visit", y asegúrese que el nombre en plural sea Visit.
- Pulse en la única columna existente para editar la columna, y cambie el nombre para mostrar a "Name".
- Pulse en el botón de "Actualizar"
- Pulse el botón de "Crear" en la esquina inferior derecha de la pantalla.
- En la sección de "Esquema", pulse en el icono de "Columnas".
- En el menú superior pulse en el botón de "+ Nueva columna".
- Utilice la sección de "Nueva columna" que se despliega a la derecha de la pantalla de "Columnas", para añadir las siguientes columnas:
    * Escriba "Expected Start" como Nombre para mostrar.
    * Selecciona "Fecha y hora" como Tipo de datos.
    * En Requerido seleccione "Requerido por la empresa".
    * Expanda el submenú de Opciones Avanzadas.
    * En el Ajuste de la zona horaria, seleccione "Independiente de la zona horaria".
    * Click Guardar
- Ahora otra columna:
    * Escriba "Expected end" como Nombre para mostrar.
    * Selecciona "Fecha y hora" como Tipo de datos.
    * En Requerido seleccione "Requerido por la empresa".
    * Expanda el submenú de Opciones Avanzadas.
    * En el Ajuste de la zona horaria, seleccione "Independiente de la zona horaria".
    * Click Guardar
- Otra columna más:
    * Escriba "Actual Start" como Nombre para mostrar.
    * Selecciona "Fecha y hora" como Tipo de datos.
    * En Requerido seleccione "Opcional".
    * Expanda el submenú de Opciones Avanzadas.
    * En el Ajuste de la zona horaria, seleccione "Independiente de la zona horaria".
    * Click Guardar
- Y otra columna:
    * Escriba "Actual End" como Nombre para mostrar.
    * Selecciona "Fecha y hora" como Tipo de datos.
    * En Requerido seleccione "Opcional".
    * Expanda el submenú de Opciones Avanzadas.
    * En el Ajuste de la zona horaria, seleccione "Independiente de la zona horaria".
    * Click Guardar
- Ahora la columna de código:
    * Escriba "Code" como Nombre para mostrar.
    * Selecciona "# Autonumeración" como Tipo de datos.
    * En Tipo de autonumeración seleccione "Número prefijado de la fecha"
    * Click Guardar
- Ultima columna:
    * Escriba "Visitor" como Nombre para mostrar.
    * Selecciona "Búsqueda" como Tipo de datos.
    * En la tabla relacionada busque y seleccione la tabla "Contact"
    * Expanda el submenú de Opciones Avanzadas.
    * Cambie el nombre de la relación a "visitor_id".
    * Click Guardar

### Tarea 1.1: Subir un fichero Excel al OneDrive
Vamos a subir los datos de los visitantes a un almacenamiento desde donde podamos importarlo dentro de la tabla creada anteriormente.

- Descargue el fichero [Visits.xlsx](Visits.xlsx) a su equipo local (la carpeta de descargas puede ser un buen sitio).
- En el menú de los 9 puntos de la esquina superior izquierda, seleccione la aplicación "OneDrive".
- Seleccione el botón de "+ Add new" y escoga la opción de "Files Upload". En la ventana de selección vaya hasta la carpeta en donde descargó el fichero excel, selecciónelo, y pulse en el botón de "Abrir". Debería ver el fichero excel dentro de la opción de "My files" del menú de la izquierda.

Puede cerrar esta pestaña del navegador.

### Tarea 1.2: Crear el flujo de datos
Ahora vamos a construir un flujo de importación de datos desde la Excel a la tabla de Visit dentro del Dataverso.

- En la pestaña de make.powerapps.com, asegurándonos de estar en el Entorno correcto (PracticaAlumno + número de alumno), escogemos la opción de tablas del menú de la izquierda.
- Localizamos y abrimos la tabla "Visit" que hemos construido.
- En el menú superior seleccionamos "Importar", y en el menú desplegable escogemos "Importar datos".
- En la pantalla de "Elegir origen de datos" escogemos el "Libro de excel".
- Y pulsamos en el botón de "Examinar OneDrive"

Si pide que seleccionemos la cuenta, escogemos la del alumno que tenemos asignado.

- Dentro de la pantalla de "Examinar OndeDrive" escogemos la excel "Visits.xlsx", y pulsamos en el botón de "Select".
- Pulsamos el botón de "Siguiente" situado en la esquina inferior derecha.
- En la pantalla de "Elegir datos", pulsamos en el check de la tabla "Visits", y se nos tienen que cargar datos en la sección principal.
- Pulse en el botón de "Siguiente". Se debe abrir la pantalla de transformación de los datos con los iconos de los pasos aplicados a la derecha de la pantalla.
- Pulse el botón de "Siguiente".

Ahora vamos a mapear las columnas del fichero excel con las columnas de la tabla en el Dataverso.

- En la sección de "Configuración de carga", escoja la segunda opción de "Cargar en una tabla existente".
- En el menú desplegable de "Tabla de destino" seleccione la tabla cuyo nombre es similar a: "crXXX_visit". Donde XXX es una combinación de letras y números.
- Configure la asignación de columnas siguiendo las indicaciones de la siguiente tabla:

| Columna de origen  | Columna de destino |
| -------------      | -------------      |
| actual end         | crxxx_ActualEnd    |
| actual start       | crxxx_ActualStart  |
| code               | crxxx_Code         |
| scheduled end      | crxxx_ExpectedEnd  |
| scheduled start    | crxxx_ExpectedStar |
| name               | crxxx_Name         |

- Pulse en el botón "Siguiente".
- Asegúrese que está seleccionado "Actualizar manualmente" dentro de la sección de Actualizar configuración.
- Pulse el botón de "Publicar".

Con esto a importado los datos que están almacenados dentro del fichero excel, a una nueva tabla en el Dataverse de su entorno, que utilizará para las prácticas del curso.

Tardará unos minutos en realizar la importación y que se muestre en la sección de Columnas y datos de la tabla Visit.
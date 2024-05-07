# Laboratorio 3: Automatización de flujos de trabajo
## Escenario

En esta práctica de laboratorio, creará un flujo de Power Automate para notificar a un visitante por correo electrónico que hay una visita programada .

Pasos de laboratorio de alto nivel
Los siguientes elementos han sido identificados como requisitos que debe implementar para completar el proyecto:

Los contactos deben ser notificados por correo electrónico cuando se programe una visita.

#### Requisitos previos
- Laboratorio 0: Validar el Entorno.
- Laboratorio 1: Modelado de datos.
- Laboratorio 3: Aplicación de modelo.
- La creación de un contácto "John Doe" con un email al que pueda enviarsele correo y poder leerlo.

## Ejercicio 1: crear el flujo de notificación de una visita

### Tarea 1: Crear el flujo
- - Vaya a https://make.powerapps.com
    * Si sale el dialogo de identificación, ingrese la dirección de correo electrónico de sus credenciales de Microsoft 365 en el cuadro de texto que dice: "Ingrese su dirección de correo electrónico".
    * Ingrese la contraseña.
    * Seleccione Sí para permanecer conectado.
- Seleccione "Entorno" y, en el listado de entornos que aparece, seleccione el de "PracticaAlumno" con su número de Alumno.
- En el menú de la izquierda pulse en la opción de "Flujos".
- En el menú superior despliegue el menú contxtual de "+ Nuevo Flujo" y escoja el de "Flujo de nube automatizado".
- El Nombre del flujo debera ser: "Visit Notification".
- En la caja de búsqueda de todos los desencadenadores busque por "Dataverse".
- Seleccione la que dice "Cuando se agrega, modifica o elimina una fila"
- Pulse el botón de "Crear".
- Configure el desencadenador con los siguientes datos:
    * Tipo de cambio: Added
    * Nombre de tabla: Visit
    * Ámbito:  Organization
- Pulse en el menú de "..." a la derecha del título del conector y elija "Cambiar nombre". Introduzca "“When a visit is added" y pulse Enter.

### Tarea 2: Crear un paso para recuperar la fila del visitante
- Pulse el botón "+ Nuevo paso" debajo del conector "“When a visit is added".
- Busque en el conector Dataverse la acción "Obtener una fila por id".
- En el nombre de tabla elija "Contacts".
- Para seleccionar el Id. de fila, pulse en la caja de texto contigua para que se abra la ventana de contenido dinámico. En ella busque el campo "Visitor (Valor)".
- Cambie el nombre de la acción a "Get Visitor".

### Tarea 3: Crear un paso para enviar email al visitante
- Añada un nuevo paso del tipo "Office 365 Outlook", con la acción "Enviar correo electrónico (V2)".
- Pulse en el campo "A", y pulse en el enlace inferior de "Agregar contenido dinámico". Seleccione "Email" de la seccion "Get Visitor".
- Como asunto introduzca "Your planned visit to Bellows College".
- Y en el cuerpo introduzca el siguiente mensaje:
> Dear {First Name},
>
>  You are currently scheduled to visit Bellows Campus from {Expected Start} until {Expected End}.
>
>  Best regards,
>
>  Campus Administration
>  Bellows College
- Reemplace las marcas {Firs Name},  {Expected Start} y {Expected End}, con los valores dinámicos.
Lo más sencillo es buscarlos en la caja de búsuqeda de la ventana de "Contenido dinámico".
- Pulse en el botón de "Guardar" del menú superior.

### Tarea 4: Probar y validar el flujo
- Pulse en el botón de "Probar" en el menú superior, seleccione "Manualmente" y pulse en el botón inferior de "Probar".
- Abra en una nueva pestaña la página principal de Power Apps.
- Desde la sección de "Aplicaciones" del menú lateral izquierdo, lance la aplicación de Tipo Basado en modelo de "Bellows Campus Managment" situando encima el ratón y pulsando el botón de "Reproducir" que aparece.
- En el menú superior pulse el botón de "+ New" que añade un nuevo contácto.
- Introduzca los datos, utilizando un email al que pueda acceder. Y pulse el botón de "Save & Close".

Vuelva a la pestaña en dónde está probando el flujo y espere al resultado. Todo debería salir con el check en verde, y debería llegarle un correo electrónico a la dirección introducida en el nuevo contácto.

**Nota:** en algunos casos le cuesta horrores en enviar el email y el flujo dá timeout. Pero el objetivo es ver cómo se construye y configura, y ahora te tocaría buscar como solucionarlo ;)

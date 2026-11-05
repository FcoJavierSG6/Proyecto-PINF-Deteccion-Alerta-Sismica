## CU-07. Compartir información de un terremoto

* **Actor principal:** Usuario.
* **Actores secundarios:** -
* **Descripción:** Permite al usuario compartir la información de un terremoto mediante aplicaciones externas de comunicación, como WhatsApp, correo electrónico o redes sociales.
* **Precondiciones:** El usuario pulsa 'Compartir' desde la opción de 'Consultar Terremoto'. El dispositivo también debe tener conexión.

### Flujo principal
1. El usuario accede al apartado de Consultar ficha del Terremoto.
2. El usuario accede a la opción de Compartir.
3. El sistema prepara la ficha del terremoto a compartir.
4. El sistema muestra un menú con las distintas opciones (Whatsapp, correo, redes sociales...)
5. El usuario selecciona la aplicación y confirma el envío.
6. El sistema vuelve a enseñarle la ficha del terremoto, después del envío.


### Postcondiciones
* La información del sismo es transmitida correctamente mediante la app externa seleccionada.

### Flujos alternativos

* **4-5a. Cancelación de compartir.**
  * 4-5a.1. El usuario cancela la acción.
  * 4-5a.2. El sistema vuelve a la pantalla Consultar ficha de Terremoto.

* **5b. Fallo de la app externa**
  * 5b.1. El sistema notifica el error y vuelve a la pantalla Consultar ficha de Terremoto  

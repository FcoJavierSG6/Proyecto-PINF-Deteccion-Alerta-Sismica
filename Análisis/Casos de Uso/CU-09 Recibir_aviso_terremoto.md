## CU-09. Recibir aviso de terremoto

* **Actor principal:** Sistema.
* **Actores secundarios:** Servidor de Notificaciones, Usuario.
* **Descripción:** Permite al usuario recibir notificaciones en su dispositivo cuando el ROA publique un terremoto que cumpla los criterios establecidos,
evitando avisos duplicados salvo cambios significativos en la magnitud.
* **Precondiciones:** El usuario debe tener conexión. El usuario debe tener activada la opción de recepción de mensajes
en la configuración.

### Flujo principal
1. El sistema detecta que el ROA ha publicado datos de un sismo.
2. El sistema comprueba que la configuración del usuario permite el envío (magnitud_mínima, recepción de mensajes...).
3. El sistema comprueba que el sismo no haya sido enviado ya.
4. El sistema compone el mensaje de aviso.
5. El sistema envía el aviso al Servidor de Notificaciones.
6. El usuario recibe la notificación emergente.


### Postcondiciones
* El usuario ha recibido la notificación correctamente y queda informado.

### Puntos de extensión
* **Consultar ficha de terremoto**. Al recibir el aviso, el usuario tiene la opción de pinchar en el aviso y consultar dicho terremoto.

### Flujos alternativos

* **2a. Configuración deniega la notificación.**
  * 2a.1. El sistema detecta que la configuración del usuario rechaza el sismo de la notificación.
  * 2a.2. El sistema cancela el envío al usuario correspondiente.

* **3a. Notificación enviada.**
  * 3a.1. El sistema detecta que la información del sismo ya fue enviada.
  * 3a.2. El sistema cancela el envío.  

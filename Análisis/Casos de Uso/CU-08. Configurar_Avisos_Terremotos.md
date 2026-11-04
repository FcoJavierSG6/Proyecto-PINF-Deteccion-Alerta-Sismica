## CU-08. Configurar avisos de terremotos

* **Actor principal:** Usuario.
* **Actores secundarios:** -
* **Descripción:** Permite al usuario configurar las preferencias de recepción de avisos de terremotos, estableciendo una magnitud mínima, una zona geográfica y las opciones de activación y sonido de las notificaciones.
* **Precondiciones:** El usuario pulsa 'Configuración de avisos'.

### Flujo principal
1. El usuario accede al apartado de configuración de avisos.
2. El sistema muestra la configuración actual.
3. El usuario activa los avisos de terremotos.
4. El usuario establece la magnitud mínima a partir de la cual desea recibir avisos.
5. El usuario selecciona el ámbito geográfico (un radio alrededor de su ubicación, toda la zona de cobertura del ROA o una región concreta).
6. El usuario selecciona si desea recibir los avisos con sonido o en silencio.
7. El usuario confirma los cambios.
8. El sistema valida y guarda las preferencias.
9. El sistema informa al usuario de que la configuración se ha guardado correctamente.

### Postcondiciones
* Las preferencias de avisos quedan almacenadas y se utilizarán para determinar qué terremotos cumplen los criterios establecidos.

### Flujos alternativos
* **3a. Desactivar los avisos**
  * 3a.1 - El usuario desactiva los avisos de terremotos.
  * 3a.2 - El sistema guarda la preferencia de desactivación.

* **5a. Permiso de ubicación aceptado**
  * 5a.1 - El usuario selecciona un radio alrededor de su ubicación.
  * 5a.2 - El sistema solicita permiso para acceder a la ubicación.
  * 5a.3 - El usuario concede el permiso (continúa en el paso 6).

* **5b. Permiso de ubicación denegado**
  * 5b.1 - El usuario selecciona un radio alrededor de su ubicación.
  * 5b.2 - El sistema solicita permiso para acceder a la ubicación.
  * 5b.3 - El usuario deniega el permiso.
  * 5b.4 - El sistema informa de que necesita acceder a la ubicación para configurar avisos basados en un radio.
  * 5b.5 - El usuario selecciona otra zona geográfica (continúa en el paso 5).

* **8a. Error al guardar la configuración**
  * 8a.1 - El sistema no puede guardar las preferencias.
  * 8a.2 - El sistema informa al usuario del error (continúa en el paso 7).

* ***a. Configuración cancelada**
  * *a.1 - El usuario cancela la operación antes de confirmar los cambios.
  * *a.2 - El sistema descarta las modificaciones realizadas.

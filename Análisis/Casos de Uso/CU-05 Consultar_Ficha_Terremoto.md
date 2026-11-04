## CU-05. Consultar ficha de terremoto

* **Actor principal:** Usuario.
* **Actores secundarios:** Servicio web del ROA.
* **Descripción:** Permite al usuario consultar la información detallada de un terremoto publicado por el ROA, incluyendo sus características, localización mapeada, estado de revisión y, si se dispone de permiso de ubicación, la distancia respecto al usuario.
* **Precondiciones:**
  * Existe un terremoto seleccionado desde la lista o el mapa.
  * La información del terremoto está disponible en la aplicación o puede obtenerse a través del servicio web del ROA.

### Flujo principal
1. El usuario selecciona un terremoto desde la lista o el mapa.
2. El sistema identifica el terremoto seleccionado.
3. El sistema obtiene la información detallada del evento si no está disponible localmente.
4. El sistema muestra la fecha y hora del terremoto en hora local y UTC.
5. El sistema muestra la latitud, longitud, profundidad, magnitud, tipo de terremoto, zona e identificador del evento.
6. El sistema muestra un mapa reducido centrado en el epicentro.
7. El sistema muestra a qué distancia del usuario está el epicentro.
8. El sistema indica si la localización del terremoto es automática o ha sido revisada por un sismólogo del ROA.
9. El usuario consulta la información de la ficha.

### Postcondiciones
* El usuario ha visualizado la información disponible del terremoto seleccionado.

### Puntos de extensión
* **Compartir información:** Disponible cuando el usuario decide compartir la ficha.
* **Enviar informe "Lo has sentido":** Disponible cuando el usuario decide hacer la encuesta.

### Flujos alternativos
* **3a. Error al obtener la información**
  * 3a.1 - El sistema no puede obtener la información detallada del terremoto.
  * 3a.2 - El sistema informa al usuario de que no ha sido posible cargar la ficha.

* **7a. Ubicación del usuario no autorizada**
  * 7a.1 - El sistema comprueba que no dispone de permiso para acceder a la ubicación del usuario.
  * 7a.2 - El sistema muestra la ficha sin indicar la distancia entre el usuario y el epicentro (continúa en el paso 8).

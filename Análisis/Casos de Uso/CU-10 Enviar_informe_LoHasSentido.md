## CU-10. Enviar informe "¿Lo has sentido?"

* **Actor principal:** Usuario.
* **Actores secundarios:** Servidor Web ROA.
* **Descripción:** Permite al usuario comunicar si ha sentido un terremoto mediante un cuestionario que recoge su ubicación aproximada, las sensaciones experimentadas y posibles daños observados, enviando las respuestas al servicio web del ROA.
* **Precondiciones:** El usuario debe estar en la pantalla del caso de uso Consultar ficha del Terremoto. El terremoto debe pasar el filtro de la configuración del usuario.

### Flujo principal
1. El usuario se encuentra en la pantalla Consultar ficha del Terremoto.
2. El usuario selecciona 'Enviar informe "¿Lo has sentido?"'.
3. El sistema despliega el cuestionario.
4. El sistema solicita al usuario su ubicación aproximada para calcular distancia.
5. El usuario acepta y envía el formulario.
6. El sistema valida la información introducida y se la envía con un POST al servidor del ROA.
7. El servidor ROA devuelve una confirmación de recepción y procesa la información.
8. El sistema muestra al usuario un mensaje de agradecimiento y regresa a la pantalla Consultar ficha del Terremoto.


### Postcondiciones
* El informe es enviado al servidor ROA para su análisis.
* La ficha del terremoto debe reflejar que el usuario ha enviado el informe y debe aparecer la distancia, si fue aceptada su solicitud.

### Flujos alternativos

*  **3-5a. Cancelación del cuestionario.**
    *  3-5a.1. El usuario selecciona la opción Cancelar Cuestionario.
    *  3-5a.2. El sistema descarta la información introducida y vuelve a la pantalla Consultar ficha del Terremoto.
 
*  **5b. Denegación de ubicación.**
    *  5b.1. El usuario rechaza los permisos de ubicación.
    *  5b.2. El sistema continúa sin calcular distancia con respecto al terremoto.
 
*  **6a. Cuestionario incompleto.**
    *  6a.1. El usuario no completa el cuestionario y selecciona Enviar.
    *  6a.2. El sistema mostrará un mensaje de Incompleto y se mantendrá en el cuestionario, sin enviarlo.
  
*  **7a. Fallo de conexión con el Servidor ROA.**
    *  7a.1. La solicitud falla por conexión o indisponibilidad del servidor.
    *  7a.2. El sistema mostrará un mensaje de error y dará la opción de Reintentar o Salir (volviendo a la pantalla de Consultar ficha del Terremoto).

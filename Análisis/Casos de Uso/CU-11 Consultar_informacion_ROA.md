## CU-11. Consultar información del Servidor del ROA.

* **Actor principal:** Usuario.
* **Actores secundarios:** Servidor Web ROA.
* **Descripción:** Permite al usuario consultar información sobre el Observatorio, la Sección de Geofísica y su red sísmica, incluyendo un enlace a la página web oficial.
* **Precondiciones:** El usuario debe estar en el menú principal.

### Flujo principal
1. El usuario selecciona desde el menú el desplegable de opciones principales (Información ROA, Recomendaciones de seguridad sísmica ...).
2. El usuario selecciona Información ROA.
3. El sistema muestra una pantalla informativa sobre el ROA (resumen institucional, información sobre la sección de Geofísica, logotipo...).
4. El usuario pulsa Salir y el sistema vuelve al menú principal.


### Postcondiciones
* El usuario ha visualizado información sobre el ROA y su sección de Geofísica.

### Flujo opcional

*  **4a. Enlace a la web del ROA.**
    *  4a.1. El usuario selecciona el enlace.
    *  4a.2. El sistema le redirecciona a la web del ROA.
    *  4a.3. El usuario vuelve de la web.
    *  4a.4. Volvemos al paso 4 del flujo principal.

## CU-14. Configurar Preferencias de la Aplicación.

* **Actor principal:** Usuario.
* **Actores secundarios:** -.
* **Descripción:** Permite al usuario configurar sus preferencias generales, incluyendo los avisos, las unidades de medida y el formato de hora.
* **Precondiciones:** El usuario debe estar en el menú principal.

### Flujo principal
1. El usuario selecciona el desplegable del menú principal.
2. El usuario selecciona Ajustes/Configurar Preferencias.
3. El sistema muestra un listado de ajustes modificables (notificaciones, unidades, tema oscuro/claro, formato de hora...).
4. El usuario modifica los ajustes.
5. El sistema guarda la configuración y la aplica.
6. El sistema regresa a usuario al menú principal.


### Postcondiciones
* El usuario ha configurado su aplicación exitosamente.

### Flujos alternativos

*  **4a. Configuración por defecto.**
    *  4a.1. El usuario no modifica nada de la configuración.
    *  4a.2. El sistema mantendrá la configuración por defecto y regresará al menú principal.

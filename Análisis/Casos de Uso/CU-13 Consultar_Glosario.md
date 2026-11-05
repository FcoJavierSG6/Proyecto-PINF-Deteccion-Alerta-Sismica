## CU-13. Consultar Glosario Sísmico

* **Actor principal:** Usuario.
* **Actores secundarios:** -.
* **Descripción:** Permite al usuario consultar definiciones de términos relacionados con la actividad sísmica, como magnitud, intensidad, epicentro y profundidad.
* **Precondiciones:** El usuario se encuentra en el menú principal.

### Flujo principal
1. El usuario selecciona el desplegable de opciones del menú principal y el sistema lo muestra.
2. El usuario selecciona la opción de Glosario Sísmico.
3. El sistema muestra un listado de los eventos sísmicos registrados, ordenados según el filtro que por defecto es orden reciente.
4. El sistema carga los datos de los sismos listados.
5. El usuario selecciona un sismo.
6. El sistema muestra sus datos correspondientes.
7. El usuario selecciona Salir.
8. El sistema volverá al menú principal.

### Postcondiciones
* El usuario ha consultado y conoce a los sismos consultados.

### Flujos alternativos
*  **ITERACIÓN**
    * Pasos 5-6 se iteran hasta llegar al 7 en un istante.

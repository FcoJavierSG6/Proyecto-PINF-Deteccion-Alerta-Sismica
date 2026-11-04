## CU-06. Consultar estaciones sísmicas

* **Actor principal:** Usuario.
* **Actores secundarios:** Servicio web del ROA.
* **Descripción:** Permite al usuario visualizar las estaciones sísmicas pertenecientes a la red del ROA sobre el mapa de terremotos, así como ocultarlas cuando lo desee.
* **Precondiciones:** El usuario se encuentra visualizando el mapa de terremotos y pulsa la opción 'Estaciones'.

### Flujo principal
1. El usuario accede a la opción para mostrar las estaciones sísmicas en el mapa.
2. El sistema solicita la información de las estaciones al servicio web del ROA.
3. El servicio web devuelve la información de las estaciones, incluyendo sus coordenadas geográficas.
4. El sistema representa las estaciones sísmicas mediante símbolos diferenciados sobre el mapa.
5. El usuario visualiza la distribución geográfica de las estaciones.

### Postcondiciones
* Las estaciones sísmicas se muestran sobre el mapa. Si el usuario desactiva la opción, las estaciones dejan de mostrarse sin afectar a los terremotos representados.

### Flujos alternativos
* **3a. Error de conexión**
  * 3a.1 - No se puede obtener la información de las estaciones.
  * 3a.2 - El sistema informa del error y mantiene el mapa de terremotos visible.

* **5a. Ocultar estaciones**
  * 5a.1 - El usuario desactiva la opción de mostrar estaciones sísmicas.
  * 5a.2 - El sistema elimina sus símbolos del mapa, manteniendo visibles los terremotos.

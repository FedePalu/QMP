# QMP 5ta iteración

## La solución consiste en:

1- Se deberíá implementar Patron Command en PresupuestoAgregar dado que habría que guardarse la info para poner modificar el guardarropas y también deberían poder deshacerse.

2- Haciendo herencia en Propuesta defino un comportamiento distinto en el método modificarGuardarropa de cada Propuesta que, con el boolean aceptado, defino si realizaré esa acción o no.

3- Con limpiarPropuestasAceptadas() se podría hacer un forEach() fijándome en las propuestas que tienen aceptado = true y eliminarlas de las listas



# QMP 4ta iteración

## La solición consiste en:

1- Crear la clase Clima, como singleton de AccuWeatherApi. Así se cumplirían los requerimientos de:
* Como administrador de QuéMePongo, quiero poder configurar fácilmente diferentes servicios de obtención del clima para ajustarme a las cambiantes condiciones económicas.
* Como stakeholder de QuéMePongo, quiero poder asegurar la calidad de mi aplicación sin incurrir en costos innecesarios. 

Ya que no voy a trabajar sobre la clase AccuWeather en sí sino que en los test voy a implementar ese método setApi(AccuWeatherApi) para setear el api y no gastar dinero cada vez que hago un text.

2- El método devolverTemperatura(String ciudad) está implementado para que encapsular toda implementación de getWeather, ya que devuelve un List<Map<String,Object>>, y hacer que devuelva una temperatura (int).

3- La SugerenciaCategorica dentro del método obtenerSugerencia() conoce los tipos de categorias gracias a la clase enum. Una solución sería algo tipo categoria.DarTodos() y que devuelva todo los tipos de categorias, y que según el criterio devolver la sugerencia de prendas.

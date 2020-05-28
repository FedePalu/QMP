## QMP

# La solición consiste en:

1- Crear la clase Clima, como singleton de AccuWeatherApi. Así se cumplirían los requerimientos de:
* Como administrador de QuéMePongo, quiero poder configurar fácilmente diferentes servicios de obtención del clima para ajustarme a las cambiantes condiciones económicas.
* Como stakeholder de QuéMePongo, quiero poder asegurar la calidad de mi aplicación sin incurrir en costos innecesarios. 

Ya que no voy a trabajar sobre la clase AccuWeather en sí sino que en los test voy a implementar ese método setApi(AccuWeatherApi) para setear el api y no gastar dinero cada vez que hago un text.

2- El método devolverTemperatura(String ciudad) está implementado para que encapsular toda implementación de getWeather, ya que devuelve un List<Map<String,Object>>, y hacer que devuelva una temperatura (int).

3- La SugerenciaCategorica dentro del método obtenerSugerencia() conoce los tipos de categorias gracias a la clase enum. Una solución sería algo tipo categoria.DarTodos() y que devuelva todo los tipos de categorias, y que según el criterio devolver la sugerencia de prendas.

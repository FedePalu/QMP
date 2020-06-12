# QMP 6ta iteración
*(NO LLEGUÉ A TERMINAR TODOS LOS REQUERIMIENTOS A LOS 30' Y ALGUNOS NO SABÍA COMO RESOLVERLOS)*
## La solución consiste en:

1- Los dos primeros requerimientos relacionados con las sugerencias diarias no pude resolverlos completos dado que no se me ocurrió cómo hacer para que se actualice todas las mañanas diariamente

2- Con almacenarAlerta(alerta, usuario) se almacenan en la lista de alertas, perteneciente al usuario, las distintas alertas resolviendo el requerimiento:

*Como usuarie de QueMePongo, quiero poder conocer cuáles son las últimas alertas meteorológicas publicadas en el sistema para estar informado (pudiendo verlas, por ejemplo, al entrar en quemepongo.com)

3- Con actualizarSugerencia(sugerencia) se resuelve el requerimiento:

*Como usuarie de QuéMePongo quiero que se actualice mi sugerencia diaria con las condiciones climáticas actualizadas cuando se genere algún alerta durante el día 

4- Con handleAlerta(alerta) se va a poder manejar los distintos resultados según la alerta generada, resolviendo así los requerimientos: 

*Como usuarie de QueMePongo quiero tener la posibilidad de que ante una alerta de tormenta la app me notifique que debo llevarme también un paraguas 

*Como usuarie de QueMePongo quiero que ante una alerta meteorológica de granizo la app  me notifique que evite salir en auto

Pd: Debería tener alguna función tipo notificar(usuario)

5- Con sendMail(usuario, alerta) se debería mandar un mail gracias al servicio externo de mails, resolviendo: 

*Como usuarie de QueMePongo quiero poder recibir un mail avisándome si se generó algún alerta meteorológico y cuál

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

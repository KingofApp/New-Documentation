# Fichero con configuración

Como ya hemos visto previamente, el **Visualizer** es un sistema capaz de cargar dinámicamente de piezas de software a partir de un fichero de configuración. Este fichero se llama `structure.json` y se ha de ubicar en la carpeta `core` del **Visualizer**.

A continuación vamos a inspeccionar uno de estos ficheros para explicar en detalle que campos soporta y la función de los mismos.

| Campo | Descripción                                                                | Requerido | Formato       |
| ----- | -------------------------------------------------------------------------- | --------- | ------------- |
| _id   | Identificador único de la app. Se genera automáticamente en el Visualizer. | Si        | Hex (16 char) |
| name  | Nombre de la aplicación.                                                   | Si        | String        |
| type  | Describe el tipo de aplicación, solo admite el valor `app`                 | Si        | String        |
| packageName | Nombre de dominio de la app.                                         | Si        | [Java package naming](http://www.oracle.com/technetwork/java/codeconventions-135099.html) |
| config | Define parámetros de configuración esenciales para el buen funcionamiento de la app. | Si | [Config object](#config-object) |
| metadata | Contiene datos para la subida de la aplicación a los diferentes *market places*.   | No | Objecto de metadata |
| themes | Permite definir un [Tema(ToDo)]() por cada entorno para el cual se ha de generar la app. Actualmente sólo se permiten los entornos `ios` y `android` | Si | Objecto de [Themes object](#themes-object) |
| modules | Contiene la información sobre cada uno de los módulos configurados dentro de la aplicación, así como su disposición | Si | [Modules object](#modules-object) |
| services | Contiene cada uno de los [Servicios(ToDo)]() utilizados en la app. Al no ser posible tener configurado el mismo servicio más de una vez, está formado por un objeto donde la key es el identificador del servicio | Si | Objecto de [Services object](#services-object) |
| users | Usuarios y permisos que tienen acceso a la aplicación.                      | No        | Array   |
| createrAt | Fecha de creación de la app                                            | No        | ISO Date      |
| updatedAt | Fecha de la última actualización de la app                             | No        | ISO Date      |




## <a name=modules-object></a> Modules object

## <a name=services-object></a> Services object

### <a name=service-object></a> Service object

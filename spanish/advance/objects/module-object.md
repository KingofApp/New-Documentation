# Module object


| Clave | Descripción | Requerido | Formato |
| ----- | ----------- | --------- | ------- |
| name  | Nombre que se muestra en el menú | Si | String |
| identifier | El nombre único con el que se registró el módulo y sus ficheros. Sólo están permitidos los caracteres alfabéticos | Si | String  |
| type  | Determina la tecnología con la que está construido el módulo. En estos momentos solamente está soportada una tecnología: <ul><li>**A:** AngularJS</li></ul> | Si| String |
| icon  | Icono del módulo. Se puede especificar de dos formas: <ul><li>Insertando el nombre de uno de los [iron-icons](https://elements.polymer-project.org/bower_components/iron-icons/demo/index.html).</li> <li>Utilizar un icono personalizado a partir de una URL, tanto local como remota.</li></ul> | No | String o URL |
| version | Indica la versión del módulo | Si | [Semantic versioning](http://semver.org/) |
| author  | Datos del desarrollador o desarrolladores que participaron en el módulo. | No | String |
| category | Especifica las categorías a las que pertenece el módulo. Para rellenar este campo, se recomienda revisar la [lista de categorías ToDo]() disponibles. | No | Array de Strings |
| canContain | Indica si el módulo es [contenedor ToDo](). Si no se define, se asumirá que no es contenedor (false). | No | Booleano |  
| showOn | Define en que partes del Builder se puede trabajar con este módulo. | Si | [ShowOn object](showon-object.md) |
| view   | Define la ruta a la vista principal del módulo.  | Si | URL |
| files  | Listado de ficheros necesarios para el funcionamiento del módulo. Estos archivos puede ser `JS`, `HTML` o `CSS`. | Si | Array de URLs |
| libs   | Listado de dependencias JavaScript necesarias para lanzar el módulo. Se ulizan las importaciones de [Bower](https://bower.io/) como sistema de dependencias. El valor por defecto es un array vacío `[]`. | Si | Array de [Lib object]() |
| deps   | Listado de dependencias de Apache Cordova necesarias para lanzar el módulo. | No | Array de String |
| scope  | Objeto que inyecta valores por defecto al scope del módulo. Se puede acceder a los datos a través de `$scope.{identificador_del_módulo}.modulescope`. Estas variables pueden ser configuradas más tarde en el formulario de configuración | Si | JSON |
| createdAt | Fecha de creación del módulo. | No | ISO Date |
| images   | Imágenes promocionales del módulo. | No | [Images object](images-object.md) |
| uniqueId | Id único que identifica el módulo dentro de las rutas de navegación. | No | webview-vPXgu |
| widget   | Agrupa los datos necesarios para renderizar en el Builder la sección de [administración ToDo]() de cualquier módulo. En caso de no estar definido, se asumirá que el módulo no permite ser administrado. | No | [Widget object](widget-object.md) |
| iframeRequest | Permite configurar la comunicación del iframe utilizado en el widget de adminitración. | No | [IframeRequest object](iframeRequest-object.md) |
| config   | Permite crear el apartado de [configuración del módulo](../modules/interaction.md) que se le mostrará al usuario desde el Builder. No es necesario para el desarrollo del módulo, pero es imprescindible para la reutilización de los módulos una vez subidos al Builder | Si | xxxxx |

## ShowOn object

| Clave | Descripción | Requerido | Formato |
| ----- | ----------- | --------- | ------- |
| market | Define si el modulo puede encontrarse en el market place de módulos. <br><br>En ciertas ocasiones no deseamos que determinados módulos hijos puedan ser utilizados de manera independiente. Este sería uno de los casos en los que se configuraría para que no fuese visible. | Si | Booleano |  
| dragDrop | Define si el modulo puede manipularse libremente en la sección de drag&drop del Builder. <br><br> Es común utilizar esta opcion para los módulos hijo, ya que es el padre el que espeficica su ubicación. | Si | Booleano |  
| menu | Permite al módulo indicarle a los menús que no debería aparecer en ellos. <br><br>Es muy util cuando queremos evitar que determinadas subsecciones no sean utilizadas en lo menúss cuando se trabaja desde el Builder. | Si | Booleano |  

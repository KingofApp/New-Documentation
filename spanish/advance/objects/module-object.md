# Module object


| Clave | Descripción | Requerido | Formato |
| ----- | ----------- | --------- | ------- |
| name  | Nombre que se muestra en el menu | Si | String |
| identifier | El nombre único con el que se registró el módulo y sus ficheros. Sólo están permitidos los caracteres alfabéticos | Si | String  |
| type  | Determina la tecnologóa con la que está construida el módulo. En estos momentos solamente está soportada una tecnología: <ul><li>**A:** AngularJS</li></ul> | Si| String |
| icon  | Icono del módulo. Puede ser especificar de dos formas: <ul><li>Insertando el nombre de uno de los [iron-icons](https://elements.polymer-project.org/bower_components/iron-icons/demo/index.html), o</li> <li>Utilizar uno personalizado a partir de una URL, tanto local como remota.</li></ul> | No | String o URL |
| version | Indica la versión del módulo | Si | [Semantic versioning](http://semver.org/) |
| author  | Dotos del o los desarrolladores que participaron en el módulo | No | String |
| category | Especifica las categorías a las que pertenece el módulo. Para rellenar este campo revisar la [lista de categorias ToDo]() disponibles. | No | Array de Strings |
| canContain | Indica si el módulo es [contenedor ToDo](). Si no se define se asumirá que es falso | No | Booleano |  
| showOn | Define en que partes del builder se puede trabajar con este módulo. | Si | [ShowOn object](showon-object.md) |
| view   | Define la ruta a la vista principal del módulo.  | Si | URL |
| files  | Listado de ficheros necesarios para el funcionamiento del módulo. Estos archivos puede ser `JS`, `HTML` o `CSS`. | Si | Array de URLs |
| libs   | Listado de dependencias JavaScript necesarias para lanzar el módulo. Se ulizan las importaciones de [Bower](https://bower.io/) como sistema de despencias. El valor por defecto es un array vación `[]`. | Si | Array de [Lib object]() |
| deps   | Listado de dependencias de Apache Cordova necesarias para lanzar el módulo. | No | Array de String |
| scope  | Objeto que inyecta valores por defecto al scope del módulo. Se puede acceder a los datos a través de `$scope.{identificador_del_módulo}.modulescope`. Estas variables pueden ser configurados más tarde en el formulario de configuración | Si | JSON |
| createdAt | Fecha de creación del módulo | No | ISO Date |
| images   | Imagenes promocionales del módulo | No | [Images object](images-object.md) |
| uniqueId | Id único que identifica el módulo dentro de las rutas de navegación | No | webview-vPXgu |
| widget   | Agrupa los datos necesarios para renderizar en el builder la sección de [administración ToDo]() de cualquier la módulo. En caso de no estar definido se asumirá que el módulo no permite ser administrado. | No | [Widget object](widget-object.md) |
| iframeRequest | Permite configurar la comunicación del iframe utilizado en el widget de adminitración. | No | [IframeRequest object](iframeRequest-object.md) |
| config   | Permite crear el apartado de [configuración del módulo](../modules/interaction.md) que se mostrará desde el builder. No es necesario de desarrollo del módulo pero es imprescindible para la reuitilación de los módulos una vez subidos al builder | Si | xxxxx |

## ShowOn object

| Clave | Descripción | Requerido | Formato |
| ----- | ----------- | --------- | ------- |
| market | Define si el modulo puede encontrarse en el market place de módulos. <br><br>En ciertas ocasiones no deseamos que determinados módulos hijos puedan ser utilizados por si mismos, este es uno de los casos en los que se configuraría para que no fuese visible. | Si | Booleano |  
| dragDrop | Define si el modulo puede manipularse libremente en la sección de drag&drop del builder. <br><br> Es común utilizar esta opcion para los módulos hijo, ya que es el padre el que espeficica su ubicación. | Si | Booleano |  
| menu | Permite al módulo indicarle a los menús que no debería aparecer en ellos. <br><br>Es muy util cuando queremos evitar que determinadas subsecciones no sean utilizadas en lo menus cuando se trabaja desde el builder. | Si | Booleano |  

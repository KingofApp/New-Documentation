# Module object

| Clave | Descripción | Requerido | Formato |
| ----- | ----------- | --------- | ------- |
| name  | Nombre que se muestra en el menú | Si | String |
| identifier | El nombre único con el que se registró el módulo y sus ficheros. Sólo están permitidos los caracteres alfabéticos | Si | String  |
| descriptionShort | Descripciones cortas del módulo separadas por idiomas | No | Objeto de String  |
| type  | Determina la tecnología con la que está construido el módulo. En estos momentos solamente está soportada una tecnología: <ul><li>**A:** AngularJS</li></ul> | Si| String |
| icon  | Icono del módulo. Se puede especificar de dos formas: <ul><li>Insertando el nombre de uno de los [iron-icons](https://elements.polymer-project.org/bower_components/iron-icons/demo/index.html).</li> <li>Utilizar un icono personalizado a partir de una URL, tanto local como remota.</li></ul> | No | String o URL |
| version | Indica la versión del módulo | Si | [Semantic versioning](http://semver.org/) |
| author  | Datos del desarrollador o desarrolladores que participaron en el módulo. | No | String |
| category | Especifica las categorías a las que pertenece el módulo. Para rellenar este campo, se recomienda revisar la [lista de categorías ToDo]() disponibles. | No | Array de Strings |
| price | Precio que se mostrará en Koapp Builder | Si | [Price object](price-object.md) |
| canContain | Indica si el módulo es [contenedor ToDo](). Si no se define, se asumirá que no es contenedor (false). | No | Booleano |  
| requires | Array de módulos de los que depende nuestro propio módulo. Cada módulo del que es dependiente se identifica con el `identifier`.  | No | [Module requires object](module-requires-object.md) |
| searchable | Define si nuestro módulo soporta al módulo de búsqueda. | No | Booleano |
| showOn | Define en que partes del Builder se puede trabajar con este módulo. | Si | [ShowOn object](showon-object.md) |
| view   | Define la ruta a la vista principal del módulo.  | Si | URL |
| files  | Listado de ficheros necesarios para el funcionamiento del módulo. Estos archivos puede ser `JS`, `HTML` o `CSS`. | Si | Array de URLs |
| libs   | Listado de dependencias JavaScript necesarias para lanzar el módulo. Se ulizan las importaciones de [Bower](https://bower.io/) como sistema de dependencias. El valor por defecto es un array vacío `[]`. | Si | Array de [Lib object](lib-object.md) |
| deps   | Listado de dependencias de Apache Cordova necesarias para lanzar el módulo. | No | Array de String |
| scope  | Objeto que inyecta valores por defecto al scope del módulo. Se puede acceder a los datos a través de `$scope.{identificador_del_módulo}.modulescope`. Estas variables pueden ser configuradas más tarde en el formulario de configuración | Si | JSON |
| createdAt | Fecha de creación del módulo. | No | ISO Date |
| images   | Imágenes promocionales del módulo. | No | [Plugin images object](plugin-images-object.md) |
| uniqueId | Id único que identifica el módulo dentro de las rutas de navegación. | No | webview-vPXgu |
| widget   | Agrupa los datos necesarios para renderizar en el Builder la sección de [administración ToDo]() de cualquier módulo. En caso de no estar definido, se asumirá que el módulo no permite ser administrado. | No | [Widget object (TODO)](widget-object.md) |
| iframeRequest | Permite configurar la comunicación del iframe utilizado en el widget de adminitración. | No | [IframeRequest object](iframeRequest-object.md) |

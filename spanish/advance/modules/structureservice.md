# API (structureService)

**Getters**

Métodos | Descripción | Parámetros | Retorno
----------------|-------------|--------|--------
`get()` | Objeto con la estructura de datos de aplicación | - | Objeto JSON
`getVisitedLocations()` | Lista con las rutas que ya han sido visitadas | - | Array
`getColors()` | Objeto con la lista de colores utilizados por la aplicación | - | Objeto JSON
`getConfig()` | Objeto con los parametros config de la aplicación | - | Objeto JSON
`getCurrentModules($location, callback)` | Genera a partir de una ruta la lista de modulos que se usan en ella | $location | Array
`getFonts()` | Objeto con las fuentes utilizadas por la aplicación | - | Objeto JSON
`getImages()` | Objeto con la lista de imagenes utilizadas por la aplicación | - | Objeto JSON
`getIndex()` | Valor de la primera vista utilizada por la aplicación  | - | String
`getLang()` | Idioma principal de la aplicación | - | String
`getMenuItems()` | Lista con todas las rutas utilizadas por los diferentes menus | - | Array
`getModule(path)` | Obtiene un Objeto modulo a partir de una ruta | String | Objeto JSON


**Setters**

Métodos | Descripción | Parámetros
----------------|-------------|--------
`set(newData)` | Establece una nueva estructura de datos de aplicación | Objeto JSON
`setColors(colors)` | Establece los colores | Objeto JSON
`setFonts(fonts)` | Asigna la fuente primaria y la utilizada para el titulo. | Objeto JSON
`setImages(images)` | Establece imágenes tipo fondo, icono, splash... | Objeto JSON
`setLang(locale)` | Establece el idioma de la aplicación | String
`setModules(newData)` | Establece una estructura de módulos | Objeto JSON
`setVisitedLocations(locations)` | Establece las rutas previamente visitadas en la aplicación | Array


**Otros**

Métodos | Descripción | Parámetros | Retorno
----------------|-------------|--------|--------
`launchSpinner(selector)` | Crea un spinner a partir de un selector | selector css |
`registerModule($location, $scope, item)` | Utilizada para registrar un módulo en el sistema de vistas | $location, $scope, 'nombre-modulo' |
`validateScope(module)` | Valida un objeto modulo y devuelve una vista 'not found' o su vista por defecto | Objeto JSON | String

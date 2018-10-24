# Librerías en módulos

### Funcionamiento

Las librerías se registran en el apartado libs del structure.json, por ejemplo:

```json
"libs": [
  {
    "bower": {
      "weather-icons": "^2.0.10"
    },
    "src": "bower_components/weather-icons/css/weather-icons-wind.min.css"
  },
  {
    "bower": {
      "angular-openweathermap-api-factory": "^0.5.0"
    },
    "src": "bower_components/angular-openweathermap-api-factory/dist/angular-openweathermap-api-factory.min.js"
  }
],
```
`Los tipos de archivo soportados son html, css y js.`

Estas librerias son dinamicamente y en orden agregadas por el visualizer, previamente a la ejecución del modulo para que esten disponibles.

`En caso de que la dependencia tenga mas de un fichero, habrá que agregar estos en un array.`

```json
"libs": [
  {
    "bower": {
      "vanilla-js-calendar": "1.0.9"
    },
    "src": ["bower_components/vanilla-js-calendar/dist/js-calendar.js", "bower_components/vanilla-js-calendar/dist/js-calendar.min.css"]
  }
]
```

Por otro lado estas mismas dependencias deberán agregarse en el archivo bower.json del modulo. Esta acción es necesaria porque en el momento de lanzar el visualizer, este, descarga las librerias bower para cada módulo.

Ejemplo bower.json:
```json
{
  "name": "openweathermap",
  "authors": "King Of app",
  "description": "Module that displays weather information in a particular area.",
  "keywords": [
    "kingofapp",
    "module"
  ],
  "license": "MIT",
  "homepage": "https://github.com/KingofApp",
  "private": true,
  "dependencies": {
    "angular-openweathermap-api-factory": "^0.5.0",
    "weather-icons": "^2.0.10"
  }
}
```

Ádemas es necesario el archivo `.bowerrc` dentro de la carpeta del modulo. Es muy importante posicionar la ruta correcta, esta es la configuración recomendada.

```json
{
  "directory" : "../../bower_components"
}
```

**Instalar y eliminar dependencias**

La instalación y eliminación se realiza utilizando [bower desde la terminal](https://bower.io/#install-packages). Además es necesario reflejar los cambios en *../app/modules/XXXX/config.json*, *../app/core/structure.json* y *../app/modules/XXXX/bower.json*


### Referencias

Documentación relacionada | Módulos de ejemplo donde se usa
--------------------------|--------------------------
<ul></ul> | <ul><li>[OpenWeatherMap module](https://github.com/KingofApp/koapp-module-openweathermap)</li><li>[Googlemap module](https://github.com/KingofApp/koapp-module-googlemap)</li></ul>

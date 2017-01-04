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

## Referencias

Documentación relacionada | Módulos de ejemplo donde se usa
--------------------------|--------------------------

<ul></ul> | <ul><li>[OpenWeatherMap module](https://github.com/KingofApp/koapp-module-openweathermap)</li><li>[Googlemap module](https://github.com/KingofApp/koapp-module-googlemap)</li></ul>

# Módulos

Los módulos permiten crear nuevas funcionalidades, para facilitar el desarrollo de nuevos módulos por parte de la comunidad. Utilizamos como base de trabajo Angular 1.5.x. 

Si ya estas familiarizado con el desarrollo de módulos en Angular, no necesitaras aprender nada nuevo, solo tendrás que familiarizarte con la estructura de archivos y la carga dinámica. 


::::: ESPERANDO CATCH_UP :::::

Para aquellos desarrolladores que no se hayan aventurado todavía con el desarrollo web con Angular... hemos preparado una [pequeña guía]() de ayuda para hacerte el camino del aprendizaje más fácil, centrándonos solamente en aquellas partes de Angular.js que resultan relevantes para desarrollar Apps con nosotros.


### Generador de Módulos.

Una manera fácil y sencilla para crear módulos rápidamente es utilizar [nuestro generador](https://www.npmjs.com/package/generator-koapp-modules). Este generador se basa en [Yeoman](http://yeoman.io/) al igual que otros generadores que utilizamos en King of App.

Este generador nos permite crear toda la estructura de archivos y contenido que necesitamos para empezar a desarrollar las nuevas funcionalidades.

Una vez tenemos el generador instalado globalmente podremos crear módulos desde cualquier lugar de nuestro sistema, aunque lo recomendado es hacerlo desde la carpeta donde esta alojado el Visualizer.


- **Instalación global y arranque**

```bash
npm install -g generator-koapp-module && yo koapp-module
```

- **Rellenamos los datos necesarios...**


![technical_modules_1](../../screenshots/technical_modules_1.png)


Las preguntas son sencillas y autocompletarán toda la estructura de archivos necesaria para crear un módulo. Solo necesitas editar los archivos *config.json*, *controller.js*, *index.html*, etc... Puedes encontrar comentarios que te ayudaran a ubicarte mejor dentro de cada archivo, además de documentación específica.


### Estructura

Esta es la estructura básica de un módulo. El módulo tiene una estructura similar a otros elementos (spinners, temas, etc...) y requiere de su carpeta con los diversos archivos de configuración.

El módulo ya incluye diversos elementos para facilitarnos el desarrollo como un ejemplo de soporte multi-idiomas y diversas tareas preconfiguradas en Gulp para poder ejecutar test E2E.

```
testmodule
├── tests
│   ├── protractor.conf.js
│   │   └── e2e
│   │       └── spec.js
├── locale
│   ├── en_US.json
│   └── es_ES.json
├── .bowerrc
├── controller.js
├── index.html
├── style.html
├── package.json
├── config.json
├── bower.json
├── Gulpfile.js
└── README.md
```

### Incluyendo el módulo en Koapp Visualizer

Los módulos también deben registrarse dentro de nuestro archivo `structure.json`.

Debemos indicar diversos parámetros, estos  parámetros determinarán y definirán la relación entre nuestros módulo y el Visualizer.

Nota: Es importante utilizar nombres que tengan sentido y respeten la misma filosofía que la declaración de variables (minúsculas, sin acentos, etc...)

- **config.json básico**
```json
{
  //...
  "modules": {
    //...
    "/ruta-mapa": {
      "name": "Mapas",
      "identifier": "googlemap",
      "type": "A",
      "icon": "room",
      "showOn": {
        "market": true,
        "dragDrop": true
      },
      "view": "modules/googlemap/index.html",
      "files": ["modules/googlemap/controller.js", "modules/googlemap/directive.js", "modules/googlemap/style.css"],
      "libs": [{
        "bower": {
          "GoogleWebComponents/google-map": "^1.1.7"
        },
        "src": "bower_components/google-map/google-map.html"
      }],
      "scope": {
        "lat": "39.8847281",
        "lon": "4.2540999",
        "zoom": "15"
      }
    },
    //...
  }
  //...
}
```

- **Explicación**

Definimos la ruta (*/ruta-mapa*) y su configuración.

Clave | Descripción | Valor por defecto
----------------|-------------|--------
`name` | Nombre que se muestra en el menu | ""
`identifier` | El nombre único con el que se registró el módulo y sus ficheros.(Solo están permitidos los caracteres alfabéticos) | ""
`type` | Tipo de módulo. "A" -> Angular. | ""
`icon` | Icono del módulo. Puede ser uno de los iconos de [iron-icons](https://elements.polymer-project.org/bower_components/iron-icons/demo/index.html) o customizado (url) | ""
`showOn.market` | Define si el spinner puede ser utilizado por los usuarios. | true
`view` | Define la ruta a la vista  | ""
`files` | Array que define los archivos(js, css...) necesarios para lanzar el módulo. | []
`libs` | Array que define las dependencias (bower) necesarias para lanzar el módulo | []
`scope` | Objeto que inyecta los valores por defecto al scope del módulo `$scope.{identificador_del_módulo}.modulescope` | {}


### Configuración del Módulo

El propio módulo tiene un archivo de configuración que determinará ciertos aspectos técnicos y también nos aportará todos los metadatos necesarios (autor, precio, versión, descripciones, etc...) para poder ubicar correctamente tu módulo en nuestro market una vez haya sido validado y publicado.


- **config.json**

```json
{
  "name"       : "Test module",
  "identifier" : "testmodule",
  "icon"       : "home",
  "description": {
    "es-ES": "Descripción del modulo",
    "en-US": "Module description"
  },
  "documentation": {
    "es-ES": "# Test module\r\nConfiguración...",
    "en-US": "# Test module\r\nConfiguration..."
  },
  "descriptionShort": {
    "es-ES": "Descripción corta",
    "en-US": "Short description"
  },
  "price"       : 0,
  "type"       : "A",
  "version"    : "1.0",
  "author"     : "King of App",
  "category"   : [
      "others"
  ],
  "requires"   : [
      "othermodule"
  ],
  "canContain" : false,
  "showOn"     : {
    "market"   : "true",
    "dragDrop" : "true"
  },
  "view"       : "modules/testmodule/index.html",
  "files"      : [
    "modules/testmodule/controller.js"
  ],
  "libs"       : [],
  "deps"       : [],
  "scope"      : {
    "data"  : "Sample data"
  },
  "config"     : [],
  "images": {
    "list": "modules/testmodule/images/list.png",
    "screenshots": [
      "modules/testmodule/images/screenshot01.png",
      "modules/testmodule/images/screenshot02.png"
    ],
    "popover": "modules/testmodule/images/popover.png",
    "banner": "modules/testmodule/images/banner.png",
    "logo": "modules/testmodule/images/logo.png"
  }
}
```

- **Opciones básicas**

Clave | Descripción | Valor por defecto
----------------|-------------|--------
`name` | Nombre del módulo | ""
`identifier` | El nombre único con el que se registró el módulo y sus ficheros.(Solo están permitidos los caracteres alfabéticos) | ""
`icon` | Icono del módule. Puede ser uno de los iconos de [iron-icons](https://elements.polymer-project.org/bower_components/iron-icons/demo/index.html) o customizado (url) | ""
`description` | Soporta Multi-lenguaje y son los datos que se mostraran como descripción en Koapp Builder | {}
`documentation` | Formato Markdown. Soporta Multi-lenguaje y son los datos que se mostraran como documentación en Koapp Builder | {}
`descriptionShort` | Soporta Multi-lenguaje y son los datos que se mostraran como documentación breve en Koapp Builder | {}
`price` | Precio que se mostrará en Koapp Builder | 0
`type` | Tipo de módulo. Por el momento solo soportado Angular ("A")  | A
`version` | Versión | 0.0.1
`author` | Nombre del autor | ""
`category` | Categorías a las que pertenece el módulo | "others"
`view` | Ruta a la vista principal | "modules/{identifier}/index.html"
`files` | Array de ficheros que cargaran antes que el módulo | []
`libs` | Array de dependencias de Bower requeridas por nuestro módulo | []
`deps` | Array de dependencias con Phonegap. | []
`scope` | Objeto que inyecta los valores por defecto al scope del módulo `$scope.{identificador_del_módulo}.modulescope` | {}
`config` | Configuración de los ajustes en Koapp Builder | {}
`images.list` | :::: DEFINIR :::: | ""
`images.screenshots` | Capturas de pantalla de nuestro módulo en funcionamiento | {}
`images.popover` | Nuestro Popover | ""
`images.banner` | Nuestro Banner | ""
`images.logo` | Nuestro Logo | ""


- **Opciones avanzadas**

Clave | Descripción | Valor por defecto
----------------|-------------|--------
`showOn.market` | Define si el módulo puede ser utilizado por los usuarios del market | true
`showOn.dragDrop` | Desabilita la funcionalidad *drag&drop* en el market. | True
`requires` | Array de módulos de los que depende nuestro propio módulo  | []
`canContain` | Define si nuestro módulo puede soportar otros módulos dentro de si mismo, como los menús | False
`searchable` | Define si nuestro módulo soporta al módulo de búsqueda. | False


### Dependencias del módulo

- `.bowerrc`. Es muy importante posicionar la ruta correcta, esta es la configuración recomendada.

```json
{
  "directory" : "../../bower_components"
}
```

- `bower.json`

```json

{
  "name": "koapp-module-googlemap",
  "authors": "King of App",
  "description": "googlemap module for King of App",
  "keywords": [
    "kingofapp",
    "module"
  ],
  "license": "MIT",
  "homepage": "http://kingofapp.com",
  "private": true,
  "dependencies": {
    "google-map": "GoogleWebComponents/google-map#^1.1.0"
  }
}
```


**Instalar y eliminar dependencias**

La instalación y eliminación se realiza utilizando [bower desde la terminal](https://bower.io/#install-packages). Además es necesario reflejar los cambios en *config.json* y *../app/core/structure.json*


### Estructura interna

Una vez tenemos toda la estructura de archivos y configuración correctamente implementados... podemos centrarnos en la funcionalidad de nuestro módulo.


Toda la lógica de nuestro módulo se define desde *controller.js*. Ya disponemos de una estructura básica con las dependencias mínimas.

- *controller.js*
```javascript
(function() {
  'use strict';

  angular
    .module('miModulo', [])
    .controller('miModuloController', loadFunction);

  loadFunction.$inject = ['$scope', 'structureService', '$location'];

  function loadFunction($scope, structureService, $location) {
    // Register upper level modules
    structureService.registerModule($location, $scope, 'miModulo');
    // --- Start miModuloController content ---
    console.info("Hi! from miModuloController");
    // --- End miModuloController content ---
  }
}());
```


La representación visual de nuestro módulo se define en *index.html*. 

- *index.html*
```html
<div class="module miModulo" ng-controller="miModuloController">
    <!-- write your module html here -->
    <p id="hi" translate>miModulo.hi</p>
    <!-- end module html -->
</div>
```

Importante: Presenting data in modules
For templating features to work with modules we strongly recommend to use our custom [Koa elements](https://github.com/KingofApp/docs/tree/master/themes#list-of-elements) inside the view.html of the module.


Nuestros estilos se definen directamente dentro de *style.html* 

- *style.html*
```html
<style is="custom-style">
/* write your module style here */
    #hi {
        /* use theme colors @example*/
        color: var(--primary-text-color);
    }
/* end module style */
</style>
```

Importante: Debes hacer uso de las variables de color para que tu módulo sea compatible con todos los temas, así el usuario final define globalmente los estilos en un solo lugar.


### API (structureService)

::::: @Fer DESCRIPCIÓN Y DETALLES (#156749) ::::::

**Getters**

Métodos | Descripción | Parámetros | Retorno
----------------|-------------|--------|--------
`get()` | - | - | Objeto JSON
`getLibs()` | - | - | - 
`getLocations()` | - | - | - 
`getChildren(menuPath)` | - | path - "/route" | Array
`getColors()` | - | - | - 
`getConfig()` | - | - | - 
`getCurrentModules($location, callback)` | - | $location | Array 
`getFonts()` | - | - | - 
`getImages()` | - | - | - 
`getIndex()` | - | - | - 
`getLang()` | - | - | - 
`getMenuItems()` | - | - | - 
`getModule(path)` | - | Objeto JSON
`getVisitedLocations()` | - | - | - 


**Setters**

Métodos | Descripción | Parámetros | Retorno
----------------|-------------|--------|--------
`set(newData)` | - | - | - 
`setLibs(libs)` | - | - | - 
`setColors(colors)` | - | - | - 
`setCssVariables(config)` | - | - | - 
`setFonts(fonts)` | - | - | - 
`setImages(images)` | - | - | - 
`setLang(locale)` | - | - | - 
`setModules(newData)` | - | - | - 
`setSpinner(newData)` | - | - | - 
`setVisitedLocations(locations)` | - | - | - 
`update(newData)` | - | - | - 
`validateScope(module)` | - | - | - 


**Otros**

Métodos | Descripción | Parámetros | Retorno
----------------|-------------|--------|--------
`launchSpinner(selector)` | - | - | - 
`loadLang()` | - | - | - 
`onChange(callback)` | - | - | - 
`registerModule($location, $scope, item)` | - | - | - 


### [Funcionalidades de los módulos](features.md)

Los módulos cuentan con algunas funcionalidades pre-cargadas de las que podemos sacar partido como son los eventos o el sistema de almacenamiento.

**[Leer más](features.md)**


### [Interacción con el Usuario](interaction.md)

Cuando desarrollamos nuevas funcionalidades a trevés de módulos siempre tendremos algunos que solicitarle al usuario algunos datos (Tokens, preferencias, etc...) para poder adecuar nuestro módulo al contexto de ejecucción.

Esta Interacción con el usuario se define en forma de formulario desde el Visualizer.

Para agilizar este proceso King of App integró y desarrollo mejoras sobre Angular-Formly

**[Leer más](interaction.md)**


### [Menús](menus.md)

Un tipo especial de módulos son los menús.

Los menús pueden desarrollarse con Angular o Polymer, en función de tus necesidades.

Además los menús tienen la particularidad de actuar como padres de otros módulos.

**[Leer más](menus.md)**


### [Testing con módulos](testing.md)

El testeo de nuestro código juega un papel crucial para preveenir errores.

En King of App recomendamos realizar al menos test de integración (e2e).

El [generador de Módulos](https://www.npmjs.com/package/generator-koapp-module) ya incluye ejemplos.

**[Leer más](testing.md)**


### Subir Módulos a Koapp Builder

::::::::: @Jovi Proceso de subida por parte de clientes (#156741) ::::::::


### Soporte a JSDoc3

:::::::: DESCRIPCIÓN (@Ulises) :::::::::

:::::::: CAPTURA (@Ulises):::::::::::

```javascript
(function() {
  'use strict';

  angular
    .module('nuevaVersion', [])
    .controller('nuevaVersionController', loadFunction);

  loadFunction.$inject = ['$scope', 'structureService', '$location'];
  /**
    * Function that loads the module
    * @function
    * @name loadFunction
    * @since  0.0.1
    * @Author Ulises Gascón
    * @example
    *   function loadFunction($scope, structureService, $location) {
    *   structureService.registerModule($location, $scope, 'nuevaVersion');
    *   console.info("Hi! from nuevaVersionController");
    * }
    * @param  {service} $scope - {@link https://docs.angularjs.org/guide/scope}
    * @param  {object} structureService - {@link http://docs.kingofapp.com/modules/}
    * @param  {service} $location - {@link https://docs.angularjs.org/api/ng/service/$location}
    */
  function loadFunction($scope, structureService, $location) {
    // Register upper level modules
    structureService.registerModule($location, $scope, 'nuevaVersion');
    // --- Start nuevaVersionController content ---
    console.info("Hi! from nuevaVersionController");
    // --- End nuevaVersionController content ---
  }
}());
```

### Ejemplo

- **[Módulo OpenweatherMap](https://github.com/KingofApp/koapp-module-openweathermap)**

![banner](https://raw.githubusercontent.com/KingofApp/koapp-module-openweathermap/master/images/banner.png)

Este módulo utiliza las diversas librerías para lograr integrar la información meteorológica de una zona concreta.

- Licencia: MIT. 
- [Código fuente](https://github.com/KingofApp/koapp-module-openweathermap)



### Ejemplos

:::::::: EJEMPLOS MÁS ESPECIFICOS (@Ulises) :::::::

**[Sencillo](example.md)**

**[Avanzado](advance_example.md)**




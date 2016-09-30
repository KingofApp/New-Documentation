# Funcionalidades

### Eventos

**koaAppRendered** 

Es un evento que lanza un callback cuando todos los [Elementos Koa]() se han cargado.

*Ejemplo:*
```javascript
$rootScope.$on("koaAppRendered",function() {
  //Your code here

});
```


:::::::: @devTeam Existen más eventos propios?? Ejemplos/Doc  (#156704)  :::::::: 


### Servicio de almacenamiento (Storage Service)


King of App integra [angular-indexedDB](https://github.com/webcss/angular-indexedDB) y permite hacer uso de la api de [IndexedDB](https://www.w3.org/TR/IndexedDB) para almacenar información persistente.

Es necesario inyectar la dependencia *storageService* para poder tener acceso a los métodos.

*Ejemplo:*
```javascript
(function() {
  'use strict';

  angular
    .module('miModulo', [])
    .controller('miModuloController', loadFunction);

  loadFunction.$inject = ['$scope', 'structureService', 'storageService', '$location'];

  function loadFunction($scope, structureService, storageService, $location) {
    // Register upper level modules
    structureService.registerModule($location, $scope, 'miModulo');
    // --- Start miModuloController content ---
    storageService.getAll().then(function(data) {
      $scope.list = data;
      console.log("We have in the list...", $scope.list);
    });
    // --- End miModuloController content ---
  }
}());
```


**Funcionalidades disponibles:**

Todos los métodos funcionan siguiendo una estructura de [promesas](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/Promesa) y mantienen un [sistema de clave-valor](https://developer.mozilla.org/es/docs/IndexedDB-840092-dup/Usando_IndexedDB#Estructuración_de_la_base_de_datos).

Métodos | Descripción | Parámetros | Retorno
----------------|-------------|--------|--------
`getAll()` | Retorna todos los objetos almacenados  |  | Array
`del(clave)` | Borra un elemento concreto | clave | -
`get(key)` | Retorna los datos de una clave específica | clave | Objeto JSON o String
`set(key, data)` | Almacena datos en una clave específica | clave, datos(string o Json) | -

**Funcionalidades avanzadas:**

::::::: Verificar (@Ulises) ::::::::

- `init(objectName)` 

Cambia manualmente el ámbito del almacenamiento, por defecto *modules*, pero puede ajustarse a *servicios*. No hay más ámbitos disponibles.

[Demo](https://github.com/KingofApp/koapp-demo-storagesample)



### Searchable Modules

:::::::: DESCRIPCIÓN y EJEMPLO (@Ulises) ::::::::



### Soporte Multi-lenguje

King of App actualmente soporta gran variedad de lenguajes. Estos lenguajes se definen por el soporte del sistema operativo de los smartphones.

Para identificar los idiomas se utilizan los [códigos de idiomas](https://es.wikipedia.org/wiki/C%C3%B3digo_de_idioma_IETF).


**Más información**
- [Android](https://developer.android.com/reference/java/util/Locale.html)
- [IOS](https://developer.apple.com/library/content/documentation/MacOSX/Conceptual/BPInternational/LanguageandLocaleIDs/LanguageandLocaleIDs.html)

**Códificaciones**
- [Lista ISO 639-1](https://en.wikipedia.org/wiki/List_of_ISO_639-1_codes)

**Lenguajes disponibles**

Código | Idioma 
-------|-------
ar | Árabe
ar_EG | Árabe (Egipto)
ar_IL | Árabe (Israel)
bg | Bulgaro
ca | Catalán
cs | Checo
da | Danés
de_AT | Alemán (Austria)
de_CH | Alemán (Suiza)
de_DE | Alemán (Alemania)
de_LI | Alemán (Liechtenstein)
el | Griego
en_AU | Inglés (Australia)
en_CA | Inglés (Canada)
en_GB | Inglés (Reino Unido)
en_IE | Inglés (Irlanda)
en_IN | Inglés (India)
en_NZ | Inglés (Nueva Zelanda)
en_SG | Inglés (Singapur)
en_US | Inglés (Estados Unidos)
en_ZA | Inglés (Zimbabue)
es_ES | Español (España)
es_MX | Español (México)
es_US | Español (Estados Unidos)
fi | Finlandes
fr_BE | Frances (Bélgica)
fr_CA | Frances (Canada)
fr_CH | Frances (Suiza)
fr_FR | Frances (Francia)
he | Hebreo
hi | Hindú
hr | Croata
hu | Húngaro
id | Indonesio
it | Italiano
ja | Japonés
ko | oreano
lt | Lituano
lv | Letonio
ms | Malayo
nb | Noruego
nl | Holandés
pl | Polaco
pt_BR | Portugés (Brasil)
pt_PT | Portugés (Portugal)
ro | Rumano
ru | Ruso
sk | eslovaco
sl_SI | Esloveno (Eslovenia)
sr | Serbio
sv | Sueco
th | Tailandés
tl_PH | Talago (Filipinas)
tr | Turco
uk | Ucraniano
vi | Vietnamita
zh_CN | Chino (China)
zh_Hans | Chino (simplificado)
zh_Hant | Chino (tradicional)
zh_HK | Chino (Hong Kong)
zh_TW | Chino (Taiwan)


**Crear Apps multi-idioma**

King of App integra [angular Translate](https://angular-translate.github.io/)

Dentro de nuestro módulo tenemos la carpeta */locale* que nos permite gestionar todos los archivos que albergan las traducciones.

Por defecto contamos con los ficheros para inglés (*/locale/en_US.json*) y español (*/locale/es_ES.json*). Ambos comparten la misma estructura de llaves y únicamente varian los textos asociados.

Nuestro módulo gestiona de manera automática la traducción desde el propio html.

- *locale/es_ES.json*
```json
{
  "moduletest.text1": "Primer texto",
  "moduletest.text2": "Segundo texto",
  "moduletest.text3": "Tercer texto",
  "moduletest.text4": "My nombre es {{variable}}"
}
```


- *locale/en_US.json*
```json
{
  "moduletest.text1": "First text",
  "moduletest.text2": "Second text",
  "moduletest.text3": "Third text",
  "moduletest.text4": "My name is {{variable}}"
}
```

- *index.html*
```html
<!-- ... -->
<p>{{ "moduletest.text1" | translate }}</p>
<p translate>moduletest.text2</p>
<p translate>{{ "moduletest.text3" }}</p>
<p translate="moduletest.text4" translate-values="{ variable:'World' }"> </p>
<!-- ... -->
```



**Detectando el idioma actual**

Podemos utilizar la API (structureService) para detectar el idioma.

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
    console.info("Lenguaje Actual:", structureService.getLang());
    // --- End miModuloController content ---
  }
}());
```



#### Custom Filter - loadUrl

::::::: DESCRIPCIÓN Y EJEMPLOS (@Ulises) :::::::

loadUrl is the filter used to define the correct path for the module's resources in each environment.
Example:
```javascript
PDFJS.workerSrc = $filter('loadUrl')('modules/pdfviewer/pdfjs/pdf.worker.js');
```
```html
<div id='playicon'>
  <koa-icon icon="{{'modules/soundcloud/images/play.svg' | loadUrl}}"></koa-icon>
</div>
<div id="pauseicon">
  <koa-icon icon="{{'modules/soundcloud/images/pause.svg' | loadUrl}}"></koa-icon>
</div>
```
Checkout our [pdfviewer module](https://github.com/KingofApp/koapp-module-pdfviewer).
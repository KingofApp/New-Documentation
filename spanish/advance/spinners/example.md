### Ejemplo sencillo

Para este ejemplo utilizaremos como base [el spinner de W3Schools](http://www.w3schools.com/howto/howto_css_loader.asp). Este spinner es muy sencillo y solamente tendremos que preocuparnos de incluir el HTML y el CSS en nuestra App.


### Solución

Puedes descargarte el ejemplo completo 
- [Zip](https://gist.github.com/UlisesGascon/8da33d599689ea5911daee5a5edc409e/archive/6e87e81ffbbce3b55f45f31b0ad73e1a4e919fbd.zip)
- [Gist](https://gist.github.com/UlisesGascon/8da33d599689ea5911daee5a5edc409e)**


### Detalles de la integración

- *app/core/structure.json*

```json
//...
"spinner": {
  "identifier": "koapp-spinner-doc-simple",
  "path": "spinners/koapp-spinner-doc-simple/koapp-spinner-doc-simple.html"
},
//...
```

- *bower.json*

```json
{
  "name": "koapp-spinner-doc-simple",
  "authors": "Ulises Gascón",
    "description": "Documentation simple sample spinner for King of App",
  "main": "koapp-spinner-doc-simple.html",
  "moduleType": [
    "globals"
  ],
  "keywords": [
    "kingofapp",
    "spinner"
  ],
  "license": "MIT",
  "homepage": "http://kingofapp.com",
  "private": true,
  "ignore": [
    "**/.*",
    "node_modules",
    "bower_components",
    "test",
    "tests"
  ],
  "dependencies": {
    "polymer": "Polymer/polymer#^1.2.0",
    "koa-behaviors": "KingofApp/koa-behaviors#^0.11.0"
  },
  "devDependencies": {
    "webcomponentsjs": "webcomponents/webcomponentsjs#^0.7.0"
  }
}
```

- *config.json*

```json
{
  "name": "Spinner - simple example",
  "identifier": "koapp-spinner-doc-simple",
  "description": {
    "en-US" : "Documentation sample spinner for King of App",
    "es-ES" : "Ejemplo de la documentación para King of App"
  },
  "version": "0.0.1",
  "author": "Ulises Gascón",
  "category": ["documentation", "demo"],
  "price": 0,
  "platforms": [
    "android",
    "ios",
    "windows"
  ],
  "showOn": {
    "market": true
  },
  "subscription": false,
  "main": "spinners/koapp-spinner-doc-simple/koapp-spinner-doc-simple.html"
}
```

- *koapp-spinner-doc-simple.html*

```html
<link rel="import" href="../../bower_components/polymer/polymer.html">
<link rel="import" href="../../bower_components/koa-behaviors/koa-spinner-behavior.html">

<dom-module id="koapp-spinner-doc-simple">
  <template strip-whitespace>
    <style>
      /* write your template style here */
        .loader {
            border: 16px solid #f3f3f3;
            border-top: 16px solid #3498db;
            border-radius: 50%;
            width: 120px;
            height: 120px;
            animation: spin 2s linear infinite;
        }

        @keyframes spin {
            0% { transform: rotate(0deg); }
            100% { transform: rotate(360deg); }
        }
      /* end template style */
    </style>

    <!-- write your template here -->
      <div class="loader"></div>
    <!-- end template -->
  </template>

  <script>
    Polymer({
      is: 'koapp-spinner-doc-simple',
      behaviors: [
        Polymer.KoaSpinnerBehavior
      ]
    });
  </script>
</dom-module>
```

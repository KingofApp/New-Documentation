# Ejemplo avanzado con canvas

### Descripción

Utilizaremos como base [este spinner](https://codepen.io/ulisesgascon/pen/rrxXXW) que funciona utilizando *canvas*. Este spinner utiliza JavaScript como base junto con HTML y css. Deberemos incluirlo todo para asegurarnos que funcione correctamente.

La integración de JavaScript se hace sencilla cuando tenemos en cuenta los [Lifecycle callbacks de polymer](https://www.polymer-project.org/1.0/docs/devguide/registering-elements#lifecycle-callbacks), ya que podemos encapsular toda la lógica, que teníamos originalmente, dentro de una función y no necesitaremos retocar el código original.


### Solución

Puedes descargarte el ejemplo completo 
- [Zip](https://gist.github.com/UlisesGascon/4ec4724dcaa7b68ec50c4799e6893b69/archive/3941a902dcf42aec67d910fb7710b8f0394129f1.zip)
- [Gist](https://gist.github.com/UlisesGascon/4ec4724dcaa7b68ec50c4799e6893b69)**


### Detalles de la integración

- *app/core/structure.json*

```json
//...
"spinner": {
  "identifier": "koapp-spinner-doc-complex",
  "path": "spinners/koapp-spinner-doc-complex/koapp-spinner-doc-complex.html"
},
//...
```

- *bower.json*

```json
{
  "name": "koapp-spinner-doc-complex",
  "authors": "Ulises Gascón",
    "description": "Documentation complex sample spinner for King of App",
  "main": "koapp-spinner-doc-complex.html",
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
  "name": "Spinner - Complex example",
  "identifier": "koapp-spinner-doc-complex",
  "description": {
    "en-US" : "Documentation complex sample spinner for King of App",
    "es-ES" : "Ejemplo complejo de la documentación para King of App"
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
  "main": "spinners/koapp-spinner-doc-complex/koapp-spinner-doc-complex.html"
}
```

- *koapp-spinner-doc-complex.html*

```html
<link rel="import" href="../../bower_components/polymer/polymer.html">
<link rel="import" href="../../bower_components/koa-behaviors/koa-spinner-behavior.html">

<dom-module id="koapp-spinner-doc-complex">
  <template strip-whitespace>
    <style>
      /* CSS del spinner */
      #spinner {
        width: 50;
        height: 50;
        padding: 30px;
      }
      /* end CSS */
    </style>

    <!-- HTML del spinner -->
      <canvas id="spinner"></canvas>
    <!-- fin HTML -->
  </template>

  <script>
    Polymer({
      is: 'koapp-spinner-doc-complex',
      // Utilizando lifecycle-callbacks (attached en este caso)
      attached: function() {
          var canvas = document.getElementById('spinner');
          var context = canvas.getContext('2d');
          var start = new Date();
          var lines = 16,  
              cW = context.canvas.width,
              cH = context.canvas.height;
          var draw = function() {
              var rotation = parseInt(((new Date() - start) / 1000) * lines) / lines;
              context.save();
              context.clearRect(0, 0, cW, cH);
              context.translate(cW / 2, cH / 2);
              context.rotate(Math.PI * 2 * rotation);
              for (var i = 0; i < lines; i++) {
                  context.beginPath();
                  context.rotate(Math.PI * 2 / lines);
                  context.moveTo(cW / 10, 0);
                  context.lineTo(cW / 4, 0);
                  context.lineWidth = cW / 30;
                  context.strokeStyle = "rgba(0, 0, 0," + i / lines + ")";
                  context.stroke();
              }
              context.restore();
          };
          window.setInterval(draw, 1000 / 30);
      },
      behaviors: [
        Polymer.KoaSpinnerBehavior
      ]
    });
  </script>
</dom-module>
```

# Spinners (Loaders)

Los spinners se construyen con Polymer, como un elemento más.


### Generador de Spinners.

Una manera fácil y sencilla para crear spinners es utilizar [nuestro generador](https://www.npmjs.com/package/generator-koapp-spinner). Este generador se basa en [Yeoman](http://yeoman.io/) al igual que otros generadores que utilizamos en King of App. Una vez tenemos el generador instalado globalmente podremos crear spinners desde cualquier lugar de nuestro sistema, aunque lo recomendado es hacerlo desde la carpeta donde esta alojado el Visualizer.


- **Instalación global y arranque**

```bash
npm install -g generator-koapp-spinner && yo koapp-spinner
```

- **Rellenamos los datos necesarios...**


![spinner_1](../screenshots/spinner_1.png)


Las preguntas son sencillas y completarán toda la estructura de elementos de Polymer necesaria para crear un spinner. Solo necesitas editar el archivo *html* e incluir tus estilos (Css), estructura (Html) y lógica (JavaScript). Puedes encontrar comentarios que te ayudaran a ubicarte mejor dentro del archivo.


### Estructura

Se trabaja como un elemento de Polymer y requiere de su propia carpeta con sus diversos archivos de configuración.

```
koapp-spinner-template
├── .bowerrc
├── bower.json
├── config.json
└── koapp-spinner-template.html
```


### Incluyendo el Spinner en nuestra App

Los spinners también están registrados dentro de nuestro archivo `structure.json`. Debemos indicar ruta e identificador... estos dos parámetros determinarán y definirán la relación entre muchos elementos. Es importante utilizar nombres que tengan sentido y respeten la misma filosofía que la declaración de variables (minúsculas, sin acentos, etc...)

```json
{
  //...
  "config": {
    //...
    "spinner": {
      "identifier": "koapp-spinner-template",
      "path": "spinners/koapp-spinner-rotationplane/koapp-spinner-template.html"
    },
    //...
  }
  //...
}
```


### Configurando el Spinner

El propio spinner tiene un archivo de configuración que determinará ciertos aspectos técnicos y también nos aportará todos los metadatos necesarios (autor, precio, versión, descripciones, etc...) para poder ubicar correctamente tu spinner en nuestro market una vez haya sido validado y publicado.


- **config.json básico**

```json
{
  "name": "Spinner Template",
  "identifier": "koapp-spinner-template",
  "description": {
    "en-US" : "",
    "es-ES" : ""
  },
  "version": "1.0.0",
  "author": "King of App",
  "category": [],
  "price": 0,
  "showOn": {
    "market": true
  },
  "main": "spinners/koapp-spinner-template/koapp-spinner-template.html"
}
```

- **Explicación**

Clave | Descripción | Valor por defecto
----------------|-------------|--------
`name` | Nombre del spinner | ""
`identifier` | El nombre único con el que se registrará el spinner y sus ficheros.(Solo están permitidos los caracteres alfabéticos) | ""
`description` | Descripción multilenguaje que mostraremos en nuestro market | {}
`version` | Control de versiones. [Ver SemVer](http://semver.org/lang/es/) | 1.0.0
`author` | Nombre del autor | ""
`category` | Categorías a las que pertenece tu spinner  | []
`price` | Precio para adquirir tu spinner en nuestro market | 0
`showOn.market` | Define si el spinner puede ser utilizado por los usuarios. | True
`main` | ruta/url al spinner | "spinners/koapp-spinner-{identifier}/koapp-spinner-{identifier}.html"


### Dependencias del spinner

- `.bowerrc`. Es muy importante posicionar la ruta correcta, esta es la configuración recomendada.

```json
{
  "directory" : "../../bower_components"
}
```

- `bower.json`. Esta es la configuración recomendada (polymer, koa-behaviors y devDependencies incluidos), pero puedes ampliarla si lo necesitas.

```json

{
  ...
  "dependencies": {
    "polymer": "Polymer/polymer#^1.2.0",
    "koa-behaviors": "KingofApp/koa-behaviors#^0.11.0"
  },
  "devDependencies": {
    "webcomponentsjs": "webcomponents/webcomponentsjs#^0.7.0"
  }
}
```


### Estructura interna del spinner

- koapp-spinner-template.html
```html
<link rel="import" href="../../bower_components/polymer/polymer.html">
<link rel="import" href="../../bower_components/koa-behaviors/koa-spinner-behavior.html">

<dom-module id="koapp-spinner-template">
  <template strip-whitespace>
    <style>
      /* CSS del spinner */

      /* fin CSS */
    </style>

    <!-- HTML del spinner -->

    <!-- fin HTML -->
  </template>

  <script>
    Polymer({
      is: 'koapp-spinner-template',
      behaviors: [
        Polymer.KoaSpinnerBehavior
      ]
    });
  </script>
</dom-module>
```


### Combinaciones de colores

Al igual que en los temas, podremos utilizar algunas variables clave para hacer que nuestro spinner se adapte automáticamente a los colores que los usuarios quieran.

- **Colores disponibles**

Propiedad del color | Descripción
----------------|-------------
`--primary-text-color` | El color del texto principal se utiliza como un color de texto general.
`--primary-background-color` | El color de fondo se utiliza en items, cards, dialogs, drop-downs o menus.
`--secondary-text-color` | Se utiliza en cualquier texto que no muestre una información primaria.
`--disabled-text-color` | Este color de texto se utiliza para mostrar las opciones de movilidad reducida.
`--divider-color` | Se utiliza en divisores como en las tarjetas
`--primary-color` | El color más utilizado en tu App.
`--light-primary-color` | Versión modificada del color primario para resaltar.
`--dark-primary-color` | Versión modificada del color primario para crear sombras.
`--accent-color` | Color de alto contraste, debe ser diferente del color primario, color del texto o color de fondo .
`--light-accent-color` | Versión modificada del color de acentuado para resaltar.
`--dark-accent-color` | Versión modificada del color de acentuado para crear sombras.
`--background-color` | Color utilizado para el fondo.

- **Ejemplo**:
```css
.spinner-layer {
  position: absolute;
  width: 100%;
  height: 100%;
  opacity: 0;
  border-color: var(--accent-color);
}
```

- **Más información**
  - [Polymer - Styling local DOM](https://www.polymer-project.org/1.0/docs/devguide/styling)
  - [Using CSS variables](https://developer.mozilla.org/en-US/docs/Web/CSS/Using_CSS_variables)


### Visualización del Spinner

En ocasiones necesitamos poder ver el spinner en funcionamiento de manera ininterrumpida, existen diversos métodos para lograrlo.

La opción más recomendada es crearte un módulo que incluya en el `index.html` y `controller.js` la siguiente configuración.

- index.html
```
<div class='transitionloader'></div>
```

- controller.js
```
structureService.launchSpinner('.transitionloader');
```

También puedes descargarlo [desde aquí (Spinner Visualizer v0.1)](../../../uploads/spinner-visualizer.zip).  

Pero si solo vas a diseñar un spinner o no quieres emplear tiempo en crearte un entorno de trabajo puedes optar por modificar el módulo html que se instala por defecto junto al Visualizer


### Ejemplos

**[Sencillo](example.md)**

Para este ejemplo utilizaremos como base [el spinner de W3Schools](http://www.w3schools.com/howto/howto_css_loader.asp). Este spinner es muy sencillo y solamente tendremos que preocuparnos de incluir el HTML y el CSS en nuestra App.

**[Avanzado](advance_example.md)**

Utilizaremos como base [este spinner](https://codepen.io/ulisesgascon/pen/rrxXXW) que funciona utilizando *canvas*. Este spinner utiliza JavaScript como base junto con HTML y css.  Deberemos incluirlo todo para asegurarnos que funcione correctamente.

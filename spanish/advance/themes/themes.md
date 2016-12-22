# King of App themes

### ¿Qué es un tema de king of App?
Un tema es un conjunto de componentes con un estilo propio, creando un tema podremos personalizar al 100% una app.

Un tema desarrollado para King of App se compone de un conjunto de componentes de [Polymer](https://www.polymer-project.org).


### Empezamos - Generador de temas.

Una manera fácil y sencilla para crear temas rápidamente es utilizar [nuestro generador](https://www.npmjs.com/package/generator-koa-theme). Este generador se basa en [Yeoman](http://yeoman.io/) al igual que otros generadores que utilizamos en King of App.

Este generador nos permite crear toda la estructura de archivos y contenido que necesitamos para empezar a desarrollar el nuevo tema.

Una vez tenemos el generador instalado globalmente podremos crear el tema desde cualquier lugar de nuestro sistema, aunque lo recomendado es hacerlo desde la carpeta donde esta alojado el Visualizer.


- **Instalación global y arranque**

```bash
npm install -g generator-koa-theme && cd com.kingofapp.visualizer/app/themes && yo koa-theme mythemename
```

Nota: `mythemename` representa el nombre del tema.


**Estructura Generada**

```
  koapp-theme-mythemename
  ├── elements
  │   ├── mythemename-badge
  │   │    ├── demo
  │   │    │   └── index.html
  │   │    └── mythemename-badge.html
  │   ├── ...
  │
  ├── styles
  │   ├── default-theme.html
  │   └── main.css
  ├── .bowerrc
  ├── .gitignore
  ├── bower.json
  ├── config.json
  └── koapp-theme-mythemename.html
```


**Incluir nuestro tema en el Visualizer**

El visualizer sirve para previsualizar los temas o módulos que vayamos a desarrollar, puedes ver aqui la documentación completa [Visualizer](../visualizer/readme.md), en resumen el visualizer carga de forma dinamica los temas y módulos leyendo de un JSON como el que aparece a continuación. Por tanto solo instanciandolo ya podemos empezar a trabajar en nuestro tema.

- *app/core/structure.json:*
```json
  {
    "config": {
      ...
      "theme": {
        "identifier": "koapp-theme-mythemename",
        "path": "themes/koapp-theme-mythemename/koapp-theme-mythemename.html"
      },
      ...
    },
    ...
  }
  ```


**¡Empieza con los cambios!**

* En el visualizer: `http://localhost:9001`
* La demo de cada componente.
  * Ejemplo: `http://localhost:9001/themes/koapp-theme-mythemename/elements/mythemename-button/demo/`



### Personalizando el tema con componentes, ¿Qué son los componentes?

Un componente es un conjunto de estándares para crear elementos HTML reutilizables.

Por ejemplo, si desea crear un carrusel de imágenes, puede crear un nuevo elemento html <image-carousel>, con todo lo que es JavaScript (comportamiento) y CSS (estilo) dentro del propio elemento. Después de eso, puede utilizar este elemento en cualquier parte de su documento.


### Sobre los componentes

Cada componente esta contenido en su propio directorio y debe seguir una estructura determinada (nombreDelTema-componente). Para facilitarnos mantener esta correlación, podemos utilizar el [generador de temas](#empezamos---generador-de-temas) que ya nos construye toda la estructura necesaria de manera automática.

Dentro de la carpeta de de nuestro componente siempre debemos incluir una subcarpeta con un demo.html, que nos facilitará posteriormente el desarrollo. También el generador se encargará de incluir esto de manera automática.

- *Estructura:*

```
awesometheme-button
├── demo
│   └── index.html
└── awesometheme-button.html
```

Cada componente se compone de un `KoaBehavior` desde el que se gestionan el resto de componentes necesarios (host attributes, propiedades, etc...).

**KoaBehavior**: Es un comportamiento ([Polymer behavior](https://www.polymer-project.org/1.0/docs/devguide/behaviors.html)) que contiene la mayoría de los componentes de comportamiento como atributos, métodos, etc...


- Elementos incluidos en KoaBehavior:

Elemento | Utilidad | Documentación
------------ | ------------- | -------------
Behaviors | Gestiona la herencia entre propiedades y métodos | [Polymer behaviors](https://www.polymer-project.org/1.0/docs/devguide/behaviors.html)
Host attributes | Permite definir los estilos durante la creación del componente | [Polymer host attributes](https://www.polymer-project.org/1.0/docs/devguide/registering-elements.html#host-attributes)
Properties | Gestiona las propiedades | [Polymer properties](https://www.polymer-project.org/1.0/docs/devguide/properties.html)
Styling | Permite utilizar CSS Customizado y Mixins | [Polymer styling](https://www.polymer-project.org/1.0/docs/devguide/styling.html)
Methods | Métodos de Polymer expuestos | [Polymer Instance methods](https://www.polymer-project.org/1.0/docs/devguide/instance-methods)



### Lista de componentes

Esta es la lista de los componentes disponibles para un tema.

* [koa-badge](elements/koa-badge.md#koa-badge) (Utiliza `koa-icon`)
* [koa-button](elements/koa-button.md#koa-button)
* [koa-card](elements/koa-card.md#koa-card)
* [koa-checkbox](elements/koa-checkbox.md#koa-checkbox)
* [koa-dialog](elements/koa-dialog.md#koa-dialog)
* [koa-dropdown-menu](elements/koa-dropdown-menu.md#koa-dropdown-menu) (Utiliza `koa-icon`, `koa-input` y `koa-menu-button`)
* [koa-grid](elements/koa-grid.md#koa-grid)
* [koa-icon-button](elements/koa-icon-button.md#koa-icon-button) (Utiliza `koa-icon`)
* [koa-input](elements/koa-input.md#koa-input) (con [koa-textarea](elements/koa-input.md#koa-textarea))
* [koa-item](elements/koa-item.md#koa-item) (con [koa-item-body](elements/koa-item.md#koa-item-body))
* [koa-menu](elements/koa-menu.md#koa-menu) (con [koa-submenu](elements/koa-menu.md#koa-submenu))
* [koa-menu-button](elements/koa-menu-button.md#koa-menu-button)
* [koa-progress](elements/koa-progress.md#koa-progress)
* [koa-radio-button](elements/koa-radio-button.md#koa-radio-button)
* [koa-slider](elements/koa-slider.md#koa-slider) (Utiliza `koa-input` y `koa-progress`)
* [koa-tabs](elements/koa-tabs.md#koa-tabs) (con [koa-tab](elements/koa-tabs.md#koa-tab))
* [koa-toggle-button](elements/koa-toggle-button.md#koa-toggle-button)
* [koa-toolbar](elements/koa-toolbar.md#koa-toolbar)


### Modificando un componente

Partiendo de la típica estructura de un componente...

```
mythemename-button
├── demo
│   └── index.html
└── mythemename-button.html
```

En `mythemename-button.html` puedes hacer cambios en el componente.

La estructura interna:

```html
<!-- write your imports here -->

<dom-module id="mythemename-button">
  <template>
    <!-- write your styles here -->
    <style>

    </style>
    <!-- end styles -->

    <!-- write your template here -->

    <!-- end template -->
  </template>

  <script>
    Polymer({
      is: 'mythemename-button',

      behaviors: [
        Polymer.KoaButtonBehavior
      ],

      // Logic here. hostAttributes, behaviors: [], properties, methods, etc
    });
  </script>
</dom-module>
```

El generador ya incluye imports, hostAttributes, behaviors, properties, methods, etc.

Por ejemplo en `koa-button`:

```html
<link rel="import" href="../../../../bower_components/polymer/polymer.html">
<link rel="import" href="../../../../bower_components/koa-behaviors/koa-button-behavior.html">

<dom-module id="mythemename-button">
  <template>
    <!-- write your styles here -->
    <style>

    </style>
    <!-- end styles -->

    <!-- write your template here -->

    <!-- end template -->
  </template>

  <script>
    Polymer({
      is: 'mythemename-button',

      behaviors: [
        Polymer.KoaButtonBehavior
      ]
    });
  </script>
</dom-module>
```


**Pasos para customizar un componente**.

1. Añadir la plantilla

  ```html
  <content></content>
  ```

  Nota: [`<content>`](https://www.polymer-project.org/1.0/docs/devguide/local-dom.html#dom-distribution) provee un punto de inserción.

2. Añadir los estilos

  ```css
  :host {
    cursor: pointer;
    display: inline-block;
    font-size: 14px;
    font-weight: 400;
    line-height: 1.42857143;
    margin-bottom: 0;
    padding: 6px 12px;
    text-align: center;
    vertical-align: middle;
    white-space: nowrap;
  }
  :host(:not[link]) {
    background-color: #fff;
    border-radius: 4px;
    border: 1px solid #ccc;
    color: #333;
  }
  :host([link]) {
    color: #23527c;
    text-decoration: underline;
  }
  :host([active]),
  :host([pressed]) {
    color: #333;
    background-color: #e6e6e6;
    border-color: #adadad;
  }
  :host([big]) {
    border-radius: 6px;
    font-size: 18px;
    line-height: 1.3333333;
    padding: 10px 16px;
  }
  :host([disabled]) {
    background-color: #e0e0e0;
    border-color: #ccc;
  }
  :host([focused]) {
    background-color: #e6e6e6;
    border-color: #8c8c8c;
    color: #333;
    text-decoration: none;
  }
  ```

  Nota: El selector `:host` se selecciona a si mismo.


Ahora ya tenemos el componente custom:

```html
<link rel="import" href="../../../../bower_components/polymer/polymer.html">
<link rel="import" href="../../../../bower_components/koa-behaviors/koa-button-behavior.html">

<dom-module id="mythemename-button">
  <template>
    <!-- write your styles here -->
    <style>
      :host {
        cursor: pointer;
        display: inline-block;
        font-size: 14px;
        font-weight: 400;
        line-height: 1.42857143;
        margin-bottom: 0;
        padding: 6px 12px;
        text-align: center;
        vertical-align: middle;
        white-space: nowrap;
      }
      :host(:not[link]) {
        background-color: #fff;
        border-radius: 4px;
        border: 1px solid #ccc;
        color: #333;
      }
      :host([link]) {
        color: #23527c;
        text-decoration: underline;
      }
      :host([active]),
      :host([pressed]) {
        color: #333;
        background-color: #e6e6e6;
        border-color: #adadad;
      }
      :host([big]) {
        border-radius: 6px;
        font-size: 18px;
        line-height: 1.3333333;
        padding: 10px 16px;
      }
      :host([disabled]) {
        background-color: #e0e0e0;
        border-color: #ccc;
      }
      :host([focused]) {
        background-color: #e6e6e6;
        border-color: #8c8c8c;
        color: #333;
        text-decoration: none;
      }
    </style>
    <!-- end styles -->

    <!-- write your template here -->
    <content></content>
    <!-- end template -->
  </template>

  <script>
    Polymer({
      is: 'mythemename-button',

      behaviors: [
        Polymer.KoaButtonBehavior
      ]
    });
  </script>
</dom-module>
```

## CSS propiedades customizadas y mixins

Los temas de King of App utilizan propiedades CSS customizadas.

### Definición de propiedades CSS customizadas

En `styles/default-theme.html` se define el valor de las variables.

*Ejemplo:*
```css
:root {
  --primary-text-color: #636363;
  --primary-background-color: #ffffff;
  --secondary-text-color: #636363;
  --disabled-text-color: #2f2b16;
  /* ... */
}
```

También, es necesario definir esos valores en la parte de defaulConfig - colors del `config.json`.

Ver [config.json > defaultConfig > colors](../objects/colors-object.md)

### Usando propiedades CSS customizadas

En la etiqueta `<style is="custom-style">`, puedes utilizar propiedades CSS customizadas.
*Sintaxis:*
```
var(variable, defaultValue)
```

```html
<style is="custom-style">
  :host {
    color: var(--button-text-color, #ffffff);
  }
</style>
```


También puedes utilizar otra propiedad CSS cutomizada como valor por defecto:


```html
<style is="custom-style">
  :host {
    color: var(--button-text-color, --primary-text-color);
  }
</style>
```

### Definición de fuentes

Por el momento solo soportamos Google Fonts como fuentes externas.

En `default-theme.html` se definen las fuentes.

*Ejemplo:*
```html
<style is="custom-style">
  :host {
    /* ... */
    --primary-font-family: 'Roboto';
    --title-font-family: 'Verdana';
    /* ... */
  }
</style>
```

También, es necesario definir esos valores en la parte de defaulConfig - fonts del `config.json`.

Ver [config.json > defaultConfig > fonts](../objects/fonts-object.md)


### Color de fondo e imagen de fondo

En `styles/default-theme.html` se definen.

*Ejemplo:*
```html
<style is="custom-style">
  :host {
    --background-color: #f8ecc2;
    --background-image: url('images/background.png');
  }
</style>
```

También, es necesario definir esos valores en la parte de defaulConfig - colors del `config.json`.

Ver [config.json > defaultConfig > colors](../objects/colors-object.md)


En caso de ser una imagen también es necesario definir esos valores en la parte de defaulConfig - images del `config.json`.

Ver [config.json > defaultConfig > images](../objects/images-object.md)


### Colores

En `styles/default-theme.html` se definen.

*Ejemplo:*
```html
<style is="custom-style">
  :root {
    --primary-text-color: #212121;
    --primary-background-color: #ffffff;
    --secondary-text-color: #737373;
    --disabled-text-color: #9b9b9b;
    --divider-color: #dbdbdb;
    --primary-color: #3f51b5;
    --light-primary-color: #c5cae9;
    --dark-primary-color: #303f9f;
    --accent-color: #ff4081;
    --light-accent-color: #ff80ab;
    --dark-accent-color: #f50057;
    --error-color: #dd2c00;

    --background-color: #ffffff;
  }
</style>
```

También, es necesario definir esos valores en la parte de defaulConfig - colors del `config.json`.

Ver [config.json > defaultConfig > colors](../objects/colors-object.md)


## Set de iconos

Puedes crear set de iconos utilizando [Polymer `iron-iconset-svg`](https://elements.polymer-project.org/elements/iron-iconset-svg).


El componente `iron-iconset-svg` permite a definir tus propios set de iconos utilizando svg.

Los componentes de icono svg deberían ser hijos del componente `iron-iconset-svg`. En el caso de crear multiples iconos es importante definir diferentes ids para identificarlos.

Si deseas dar soporte a todos los iconos, puedes utilizar [PolymerElements/iron-icons/iron-icons.html](https://github.com/PolymerElements/iron-icons/blob/master/iron-icons.html) y editar las rutas svg.

*Ejemplo:*
```html
<link rel="import" href="../iron-icon/iron-icon.html">
<link rel="import" href="../iron-iconset-svg/iron-iconset-svg.html">

<iron-iconset-svg name="myiconsetname" size="24">
  <svg>
    <defs>
      [...]
      <g id="add"><path d="M19 13h-6v6h-2v-6H5v-2h6V5h2v6h6v2z"/></g>
      <g id="arrow-drop-down"><path d="M7 10l5 5 5-5z"/></g>
      <g id="arrow-drop-up"><path d="M7 14l5-5 5 5z"/></g>
      [...]
    </defs>
  </svg>
</iron-iconset-svg>
```

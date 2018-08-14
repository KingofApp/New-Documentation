# &lt;koa-card&gt;

Es un contenedor sombreado del tipo "tarjeta de información".

### Demo

* Demo con [paper-card](https://elements.polymer-project.org/elements/paper-card?view=demo).
* Demo con [ios-card](https://kingofapp.github.io/ios-card).

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--card-header-color` | El color del texto de cabecera. | `#000`
`--card-header` | Mixin aplicado a la cabecera de la tarjeta. | `{}`
`--card-header-text` | Mixin aplicado al título en la sección de cabecera de la tarjeta. | `{}`
`--card-header-image` | Mixin aplicado a la imagen de la cabecera de la tarjeta. | `{}`
`--card-content` | Mixin aplicado a la sección de contenido de la tarjeta. | `{}`
`--card-actions` | Mixin aplicado a la sección de acciones de la tarjeta. | `{}`
`--card` | Mixin aplicado a la tarjeta. | `{}`

---

### [KoaCardBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-card-behavior.html)

#### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
***fadeImage*** | `Boolean` | Cuando `preloadImage` es verdadero (true), establece el `fadeImage` a true y hará que la imagen se desvanezca. | `false`
***heading*** | `String` | El título de la tarjeta. | `''`
***image*** | `String` | La url del título de la imagen de la tarjeta. | `''`
***preloadImage*** | `Boolean` | Cuando es `verdadero` (true), cualquier cambio en la url de la imagen causará que el `placeholder` de la imagen se vea hasta que la imagén se renderice completamente. | `false`

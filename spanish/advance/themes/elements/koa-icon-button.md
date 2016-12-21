# &lt;koa-icon-button&gt;

Es un botçon con una imagen en el centro.

Incluye un set de iconos por defecto. Usa `icon` para especificar que icono del set de iconos quieres usar.


### Demo

* Demo con [paper-icon-button](https://elements.polymer-project.org/elements/paper-icon-button?view=demo).
* Demo con [ios-icon-button](https://kingofapp.github.io/ios-icon-button).

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--icon-button-disabled-text` | El color del texto del botón deshabilitado | `--disabled-text-color`
`--icon-button` | Mixin para el botón | `{}`
`--icon-button-disabled` | Mixin para el botón deshabilitado | `{}`
`--icon-button-pressed-background-color` | Color de fondo cuando el botón está pulsado | `--disabled-text-color`

---

### [KoaIconButtonBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-icon-button-behavior.html)

#### Comportamientos

##### [Polymer.IronButtonState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronButtonState)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*active* | `Boolean` | Sí verdadero, el botón es un toggle y está marcado como activo. | `false`
*pressed* | `Boolean` | Sí verdadero, el usuario está actualmente pulsando el botón. | `false`
*toggles* | `Boolean` | Sí verdadero, el botón cambia al estado activo en cada tap o pulsando la tecla de espacio. | `false`

##### [Polymer.IronControlState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronControlState)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*disabled* | `Boolean` | Sí verdadero, el usuario no puede interactuar con este elemento. | `false`
*focused* | `Boolean` | Sí verdadero, el elemento tiene el foco. | `false`

#### Atributos del Host

Atributo | Valor
----------|------
***role*** | `'button'`
***tabindex*** | `0`

#### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
***alt*** | `String` | Especifica el texto alternativo para el botón, para accesibilidad. | `false`
***icon*** | `String` | Especifica el nombre del icono o el indice en el set de iconos disponible. Sií la propiedad del icono esta especificada, el src no debería. |
***src*** | `String` | La URL de una imagen para el icono. Sí la propiedad src está especificada el icon no debería. |

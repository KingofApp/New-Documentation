# &lt;koa-button&gt;

Es un botón con los comportamientos de los paper-button de Polymer.

### Demo

* Demo con [paper-button](https://elements.polymer-project.org/elements/paper-button?view=demo).
* Demo con [ios-button](https://kingofapp.github.io/ios-button).

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--button` | Mixin aplicado al botón. | `{}`
`--button-disabled` | Mixin aplicado al botón deshabilitado. Hay que tener en cuenta que también se puede usar el selector. `koa-button[disabled]` | `{}`
`--button-keyboard-focus` | Mixin aplicado al botón después de que sea seleccionado con el teclado. | `{}`
`--button-link-keyboard-focus` | Mixin aplicado al botón de tipo link después de que sea seleccionado con el teclado. | `{}`
`--button-big-keyboard-focus` | Mixin aplicado a un botón grande después de que sea seleccionado con el teclado. | `{}`

---

### [KoaButtonBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-button-behavior.html)

#### Comportamientos

##### [Polymer.IronButtonState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronButtonState)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*active* | `Boolean` | Si es verdadero (true), el botón es un toggle con el estado activo permanente. | `false`
*pressed* | `Boolean` | Es verdadero (true) cuando el usuario mantiene pulsado el botón. | `false`
*toggles* | `Boolean` | Si es verdadero (true), el botón cambiará al estado activo en cada tap o pulsando la tecla de espacio. | `false`

##### [Polymer.IronControlState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronControlState)

###### Properties

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*disabled* | `Boolean` | Si es verdadero (true), el usuario no puede interactuar con este elemento. | `false`
*focused* | `Boolean` | Si es verdadero (true), el elemento tiene el foco inicialmente. | `false`

#### Atributos del Host

Atributo | Valor
----------|------
***role*** | `'button'`
***tabindex*** | `0`

#### Propiedades

Name | Type | Description | Default
-----|------|-------------|--------
***big*** | `Boolean` | Si es verdadero, el botón será más grande. | `false`
***link*** | `Boolean` | Si es verdadero, el botón tendrá aspecto de enlace. | `false`

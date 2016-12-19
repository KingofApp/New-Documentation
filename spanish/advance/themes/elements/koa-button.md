# &lt;koa-button&gt;

Es un botón con los comportamientos de los paper-buttons de polymer.

### Demo

* Demo con [paper-button](https://elements.polymer-project.org/elements/paper-button?view=demo).
* Demo con [ios-button](https://kingofapp.github.io/ios-button).

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--button` | Mixin aplicado al botón | `{}`
`--button-disabled` | Mixin aplicado al botón deshabilitado. Ten en cuenta que también puedes usar el selector `koa-button[disabled]` | `{}`
`--button-keyboard-focus` | Mixin aplicado al botón después de que sea seleccionado con el teclado | `{}`
`--button-link-keyboard-focus` | Mixin aplicado al botón de tipo link después de que sea seleccionado con el teclado | `{}`
`--button-big-keyboard-focus` | Mixin aplicado a un botón grande después de que sea seleccionado con el teclado | `{}`

---

### [KoaButtonBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-button-behavior.html)

#### Comportamientos

##### [Polymer.IronButtonState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronButtonState) contiene

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*active* | `Boolean` | Sí verdadero, el botón es un toggle con el estado activo permanente. | `false`
*pressed* | `Boolean` | Sí verdadero, el usuario esatrá manteniendo el botón pulsado. | `false`
*toggles* | `Boolean` | Sí verdadero, el botón cambiará al estado activo en cada Tap o pulsando la tecla de espacio. | `false`

##### [Polymer.IronControlState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronControlState) contiene

###### Properties

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*disabled* | `Boolean` | Sí verdadero, el usuario no puede interactuar con este elemento. | `false`
*focused* | `Boolean` | Sí verdadero, el elemento tiene el foco inicialmente. | `false`

#### Atributos del Host

Atributo | Valor
----------|------
***role*** | `'button'`
***tabindex*** | `0`

#### Propiedades

Name | Type | Description | Default
-----|------|-------------|--------
***big*** | `Boolean` | Sí verdadero, el botón deberá ser más grande. | `false`
***link*** | `Boolean` | Sí verdadero, el botón tendrá aspecto de enlace. | `false`

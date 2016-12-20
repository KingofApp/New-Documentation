# &lt;koa-dropdown-menu&gt;

Es similar al elemento nativo del navegador `select`. Funciona con un contenido seleccionable. El elemento seleccionado se muestra en el control. Sí no hay ningún elemento seleccionado se muestra la etiqueta en su lugar.

El elemento hijo con la clase `dropdown-content` será usado como el menu del dropdown.

### Demo

* Demo con [paper-dropdown-menu](https://elements.polymer-project.org/elements/paper-dropdown-menu?view=demo).

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--dropdown-menu` | Un mixin que es aplicado al host del elemento | `{}`
`--dropdown-menu-disabled` | Un mixin que es aplicado al host del elemento cuando esta deshabilitado | `{}`
`--dropdown-menu-button` | Un mixin que es aplicado al menu del botón | `{}`
`--dropdown-menu-input` | Un mixin que es aplicado al input | `{}`
`--dropdown-menu-icon` | Un mixin que es aplicado al icono | `{}`

---

### [KoaDropdownMenuBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-dropdown-menu-behavior.html) offers

#### Comportamientos

##### [Polymer.IronButtonState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronButtonState)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*active* | `Boolean` | Sí verdadero, el botón es un toggle y esta activo. | `false`
*pressed* | `Boolean` | Sí verdadero, el usuario es actualmente pulsando el botón. | `false`
*toggles* | `Boolean` | Sí verdadero, el toggle del botón esta activo con cada tap o pulsando la tecla de espacio. | `false`

##### [Polymer.IronControlState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronControlState)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*disabled* | `Boolean` | Sí verdadero, el usuario no puede interactuar con este elemento. | `false`
*focused* | `Boolean` | Sí verdadero, el elemento actualmente tiene el foco. | `false`

##### [Polymer.IronFormElementBehavior](https://elements.polymer-project.org/elements/iron-form-element-behavior)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*name* | `String` | El nombre del elemento. |
*required* | `Boolean` | Establece a verdadero para hacer que el input sea requerido. Sí lo usas en un formulario, un elemento personalizadoque use este comportamiento deberá también usar `Polymer.IronValidatableBehavior` y definir un método de validación personalidado. De otro modo, un elemento requerido siempre será considerado válido. Es muy recomendable que proporciones un estilo visual para el elemento cuando  su valor sea invalido. | `false`
*value* | `String` | El valor de este elemento será usado cuando se envia en un formulario, es de solo lectura y tendrá siempre el mismo valor que `selectedItemLabel`. |

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
***label*** | `String` | La etiqueta del dropdown. |
***noAnimations*** | `Boolean` | Establece a verdadero para deshabilitar animaciones cuando se abre y cierra el dropdown. | `false`
***opened*** | `Boolean` | Verdadero si el dropdown está abierto. De otra forma, falso. | `false`
***placeholder*** | `String` | El placeholder del dropdown. |
***selectedItem*** | `Object` | El último elemento seleccionado. Un elemento es seleccionado si el menu del dropdown tiene un hijo con la clase `dropdown-content`, y este hijo contiene un evento `iron-select` con el elemento seleccionado `item` en el `detail`. |
***selectedItemLabel*** | `String` | La "etiqueta" derivada del elemento seleccionado actualmente. Este valor es la propiedad del `label` del elemento seleccionado si esta establecido, en caso contrario será el contenido reducido del texto del elemento seleccionado. |
***value*** | `String` | El valor de este elemento será usado cuando se envie en un formulario. Es de solo lectura y siempre tendrá el mismo valor que `selectedItemLabel`. |

###### Métodos

Nombre | Descripción
-----|------------
***close()*** | Oculta el contenido del dropdown.
***open()*** | Muestra el contenido del dropdown.

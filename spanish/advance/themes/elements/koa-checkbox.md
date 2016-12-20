# &lt;koa-checkbox&gt;

Es un botón del tipo checkbox que puede estar marcado o desmarcado. El usuario puede hacer tap en el botón para marcar o desmarcarlo. Normalmente, este tipo de botón se usa para permitir al usuario seleccionar una o varias opciones de un conjunto.

### Demo

* Demo con [paper-checkbox](https://elements.polymer-project.org/elements/paper-checkbox?view=demo).
* Demo con [ios-checkbox](https://kingofapp.github.io/ios-checkbox).

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--checkbox-unchecked-background-color` | Color del fondo del checkbox cuando no esta marcado | `transparent`
`--checkbox-unchecked-color` | Color del borde del checkbox cuando no esta marcado | `--primary-text-color`
`--checkbox-checked-color` | Color del checkbox cuando esta marcado | `--default-primary-color`
`--checkbox-checkmark-color` | Color de la marca del checkbox | `white`
`--checkbox-label-color` | Color de la etiqueta | `--primary-text-color`
`--checkbox-label-spacing` | Espacio entre la etiqueta y el checkbox | `8px`
`--checkbox-error-color` | Color del checkbox cuando es invalido | `#db4437`

---

### [KoaCheckboxBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-checkbox-behavior.html)

#### Comportamientos

##### [Polymer.IronButtonState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronButtonState)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*active* | `Boolean` | Sí verdadero, el botton es un toggle con el estado activo. | `false`
*pressed* | `Boolean` | Sí verdadero, el usuario está pulsando el botón. | `false`
*toggles* | `Boolean` | Sí verdadero, el botón cambia al estado activo con cada tap o pulsando la barra de espacio. | `true`

##### [Polymer.IronControlState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronControlState)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*disabled* | `Boolean` | Sí verdadero, el usuario no puede interactuar con este elemento. | `false`
*focused* | `Boolean` | Sí verdadero, el elemento tiene el foco. | `false`

##### [Polymer.IronCheckedElementBehavior](https://elements.polymer-project.org/elements/iron-checked-element-behavior)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*checked* | `Boolean` | Obtiene o establece el estado, verdadero es marcado y falso desmarcado. | `false`
*name* | `String` | El nombre de este elemento. |
*required* | `Boolean` | Establece a verdadero para hacer que el input sea requerido. Sí lo usas en un formulario, un elemento personalizadoque use este comportamiento deberá también usar Polymer.IronValidatableBehavior y definir un método de validación personalidado. De otro modo, un elemento requeridosiempre será considerado válido. Es muy recomendable que proporciones un estilo visual para el elemento cuando  su valor sea invalido. | `false`
*toggles* | `Boolean` | Sí verdadero, el botón the button cambia al estado activo con cada tap o pulsando la tecla de espacio. | `true`
*value* | `String` | El valor para este elemento. | `'on'`

#### Atributos del Host

Atributo | Valor
----------|------
***aria-checked*** | `false`
***role*** | `'checkbox'`
***tabindex*** | `0`

# &lt;koa-input&gt; & &lt;koa-textarea&gt;

## &lt;koa-input&gt;

Es un campo de texto simple.

### Demo

* Demo con [paper-input](https://elements.polymer-project.org/elements/paper-input?view=demo).
* Demo con [ios-input](https://kingofapp.github.io/ios-input).

### Estilos

Ver `<koa-input-container>` para obtener la lista de las propiedades personalizadas usadas para eltilizar el elemento.

---

### [Polymer.KoaInputBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html)

#### Comportamientos

##### [Polymer.IronFormElementBehavior](https://elements.polymer-project.org/elements/iron-form-element-behavior)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*name* | `String` | El nombre de este elemento. |
*required* | `Boolean` | Establece a verdadero para hacer que el input sea requerido. Sí lo usas en un formulario, un elemento personalizadoque use este comportamiento deberá también usar `Polymer.IronValidatableBehavior` y definir un método de validación personalidado. De otro modo, un elemento requerido siempre será considerado válido. Es muy recomendable que proporciones un estilo visual para el elemento cuando  su valor sea invalido. | `false`
*value* | `String` | El valor de este elemento. |

##### [Polymer.IronControlState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronControlState) contiene

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*disabled* | `Boolean` | Sí verdadero, el usuario no podrá interactuar con este elemento. | `false`
*focused* | `Boolean` | Sí verdadero, el elemento tendrá el foco. | `false`

#### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
***accept*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `accept`, usado con type=file. |
***allowedPattern*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `allowedPattern`. |
***autocapitalize*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocapitalize`. | `none`
***autocomplete*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocomplete`. | `off`
***autocorrect*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocorrect`. | `off`
***autofocus*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `autofocus`. |
***autosave*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autosave`, usado con type=search. |
***autoValidate*** | `String` | Establece a verdadero para auto-validar el valor del input. Enlaza esto con la propiedad input-container `autoValidate`. | `false`
***charCounter*** | `Boolean` | Establece a verdadero para mostrar el contador de carácteres. | `false`
***disabled*** | `Boolean` | Establece a verdadero para deshabilitar este input. Enlaza los dos `<koa-input-container>` y la propiedad `disabled` del input. | `false`
***errorMessage*** | `String` | El mensaje de error se mostrará cuando el input es invalido. Enlaza esto con el contenido de `<koa-input-error>`, sí se usa. |
***inputmode*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `inputmode`. |
***invalid*** | `Boolean` | Devuelve verdadero sí el valor es invalido. Enlaza los dos `<koa-input-container>` y la propiedad del input `invalid`. | `false`
***label*** | `String` | La etiqueta para este input. Enlaza esto con el contenido de `<label>` y la propiedad `hidden`, e.j. `<label hidden$="[[!label]]">[[label]]</label>` en tu `template` |
***list*** | `String` | El datalist del input (sí lo hay). Este debe coincidor con el id de un `<datalist>` existente. Enlaza esto con la propiedad `<input is="iron-input">` `list`. |
***max*** | `String` | El máximo (numerico o date-time) valor del input. Puede ser un string (e.j. "2000-1-1") o un numero (e.j. 2). Enlaza esto con la propiedad `<input is="iron-input">` `max`. |
***maxlength*** | `Number` | La longitud máxima del valor del input. Enlaza esto con la propiedad `<input is="iron-input">` `maxlength`. |
***min*** | `String` | El minimo (numerico o date-time) valor del input. Enlaza esto con la propiedad `<input is="iron-input">` `min`. |
***minlength*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `minlength`. |
***multiple*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `multiple` property, usado con type=file. |
***name*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `name`. |
***pattern*** | `String` | Un patrón para validar el ancho del input. Enlaza esto con la propiedad `<input is="iron-input">` `pattern`. |
***placeholder*** | `String` | Un texto para el placeholder (para extender la etiqueta). Sí esta establecido, la etiqueta estará siempre flotada. | `''`
***preventInvalidInput*** | `Boolean` | Establece a verdadero para prevenir que el usuario introduzca un input no válido. Enlaza esto con la propiedad `<input is="iron-input">` `preventInvalidInput`. |
***readonly*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `readonly`. |
***required*** | `Boolean` | Establece a verdadero para marcar el input como requerido. Enlaza esto con la propiedad `<input is="iron-input">` `required`. |  `false`
***results*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `results`, usado con type=search. |
***size*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `size`. |
***step*** | `String` | Limita los incrementos del numerico o del date-time. Enlaza esto con la propiedad `<input is="iron-input">` `step`. |
***type*** | `String` | El tipo del input. Los tipos soportados son text, number y password. Enlaza esto con la propiedad `<input is="iron-input">` `type`. |
***validator*** | `String` | Nombre del validador para usar. Enlaza esto con la propiedad `<input is="iron-input">` `validator` |
***value*** | `String` | El valor de este input. Enlaza esto con la propiedad `<input is="iron-input">` `bindValue`, o  la propiedad `value` del input que es `notify:true`. |

#### Métodos

Nombre | Descripción
-----|------------
***validate()*** | Valida el elemento del input y establece un estilo al error sí es necesario.


## &lt;koa-textarea&gt;

Es un campo de texto multilínea.

### Demo

* Demo con [paper-textarea](https://elements.polymer-project.org/elements/paper-input?view=demo).
* Demo con [ios-textarea](https://kingofapp.github.io/ios-input).

### Styling

Ver `<koa-input-container>` para el listado de las propiedades personalizadas usadas para estilizar este elemento.

---

### [Polymer.KoaTextareaBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-textarea-behavior.html) ofrece

#### Comportamientos

##### [Polymer.KoaInputBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
***accept*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `accept`, usado con type=file. |
***allowedPattern*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `allowedPattern`. |
***autocapitalize*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocapitalize`. | `none`
***autocomplete*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocomplete`. | `off`
***autocorrect*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocorrect`. | `off`
***autofocus*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `autofocus`. |
***autosave*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autosave`, usado con type=search. |
***autoValidate*** | `String` | Establece a verdadero para auto validar el valor del input. Enlaza esto con la propiedad del input-container `autoValidate`. | `false`
***charCounter*** | `Boolean` | Establece a verdadero para mostrar el contador de caracteres. | `false`
***disabled*** | `Boolean` | Establece a verdadero para deshabilitar el input. Enlaza ambos al `<koa-input-container>` y a la propiedad `disabled`. | `false`
***errorMessage*** | `String` | El mensaje de error a mostrar cuando el input no es válido. Enlaza esto con el contenido `<koa-input-error>`, sí se usa. |
***inputmode*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `inputmode`. |
***invalid*** | `Boolean` | Devuelve verdadero si el valor no es válido. Enlaza esto a `<koa-input-container>` y a la propiedad `invalid` del input. | `false`
***label*** | `String` | La etiqueta para este input. Enlaza esto al contenido del `<label>` y a la propiedad `hidden`, e.j. `<label hidden$="[[!label]]">[[label]]</label>` in your `template` |
***list*** | `String` | El datalist del input (sí lo hay). Este debe coincidor con el id de un `<datalist>` existente. Enlaza esto con la propiedad `<input is="iron-input">` `list`. |
***max*** | `String` | El máximo (numerico o date-time) valor del input. Puede ser un string (e.j. "2000-1-1") o un numero (e.j. 2). Enlaza esto con la propiedad `<input is="iron-input">` `max`. |
***maxlength*** | `Number` | La longitud máxima del valor del input. Enlaza esto con la propiedad `<input is="iron-input">` `maxlength`. |
***min*** | `String` | El minimo (numerico o date-time) valor del input. Enlaza esto con la propiedad `<input is="iron-input">` `min`. |
***minlength*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `minlength`. |
***multiple*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `multiple` property, usado con type=file. |
***name*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `name`. |
***pattern*** | `String` | Un patrón para validar el ancho del input. Enlaza esto con la propiedad `<input is="iron-input">` `pattern`. |
***placeholder*** | `String` | Un texto para el placeholder (para extender la etiqueta). Sí esta establecido, la etiqueta estará siempre flotada. | `''`
***preventInvalidInput*** | `Boolean` | Establece a verdadero para prevenir que el usuario introduzca un input no válido. Enlaza esto con la propiedad `<input is="iron-input">` `preventInvalidInput`. |
***readonly*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `readonly`. |
***required*** | `Boolean` | Establece a verdadero para marcar el input como requerido. Enlaza esto con la propiedad `<input is="iron-input">` `required`. |  `false`
***results*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `results`, usado con type=search. |
***size*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `size`. |
***step*** | `String` | Limita los incrementos del numerico o del date-time. Enlaza esto con la propiedad `<input is="iron-input">` `step`. |
***type*** | `String` | El tipo del input. Los tipos soportados son text, number y password. Enlaza esto con la propiedad `<input is="iron-input">` `type`. |
***validator*** | `String` | Nombre del validador para usar. Enlaza esto con la propiedad `<input is="iron-input">` `validator` |
***value*** | `String` | El valor de este input. Enlaza esto con la propiedad `<input is="iron-input">` `bindValue`, o  la propiedad `value` del input que es `notify:true`. |

#### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
***rows*** | `Number` | El numero inicial de filas. | `1`
***maxRows*** | `Number` | El máximo numero de filas que este elemento puede crecer hasta hacer scroll. 0 Significa que no hay máximo. | `0`


## &lt;koa-input-container&gt;

Es un contenedor para `<label>`, `<input is="iron-input">` o `<iron-autogrow-textarea>` y más elementos add-on opcionales como el mensaje de error o el contador de caracteres.

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--input-container-color` | Etiqueta y linea inferior cuando el input esta con el foco | `--secondary-text-color`
`--input-container-focus-color` | Label and underline color when the input is focused | `--default-primary-color`
`--input-container-invalid-color` | Label and underline color when the input is is invalid | `--google-red-500`
`--input-container-input-color` | Input foreground color | `--primary-text-color`
`--input-container` | Mixin applied to the container | `{}`
`--input-container-disabled` | Mixin applied to the container when it's disabled | `{}`
`--input-container-label` | Mixin applied to the label | `{}`
`--input-container-label-focus` | Mixin applied to the label when the input is focused | `{}`
`--input-container-input` | Mixin applied to the input | `{}`
`--input-container-underline` | Mixin applied to the underline | `{}`
`--input-container-underline-focus` | Mixin applied to the underline when the input is focused | `{}`
`--input-container-underline-disabled` | Mixin applied to the underline when the input is disabled | `{}`
`--input-prefix` | Mixin applied to the input prefix | `{}`
`--input-suffix` | Mixin applied to the input suffix | `{}`

---

### [Polymer.KoaInputContainerBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html) offers

#### Properties

Name | Type | Description | Default
-----|------|-------------|--------
***attrForValue*** | `String` | The attribute to listen for value changes on. | `'bind-value'`
***autoValidate*** | `Boolean` | Establece a verdadero para auto-validate the input value when it changes. | `false`
***focused*** | `Boolean` | True if the input has focus. | `false`
***invalid*** | `Boolean` | True if the input is invalid. This property is set automatically when the input value changes if auto-validating, or when the `iron-input-validate` event is heard from a child. | `false`


## &lt;koa-input-error&gt;

It is an error message for use with `<koa-input-container>`. The error is displayed when the `<koa-input-container>` is `invalid`.

### Styling

Custom property | Description | Default
----------------|-------------|--------
`--input-container-invalid-color` | Label and underline color when the input is is invalid | `#db4437`
`--input-error` | Mixin applied to the error | `{}`

---

### [Polymer.KoaInputErrorBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html) offers

#### Behaviors

##### [Polymer.KoaInputAddonBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html)

###### Host attributes

Attribute | Value
----------|------
***add-on*** | `''`

###### Methods

Name | Description
-----|------------
***update()*** | The function called by `<koa-input-container>` when the input value or validity changes.

#### Properties

Name | Type | Description | Default
-----|------|-------------|--------
***invalid*** | `Boolean` | True if the error is showing. |

#### Methods

Name | Description
-----|------------
***update()*** |


## &lt;koa-input-char-counter&gt;

It is a character counter for use with `<koa-input-container>`. It shows the number of characters entered in the input and the max length if it is specified.

### Styling

Custom property | Description | Default
----------------|-------------|--------
`--input-char-counter` | Mixin applied to the element	| `{}`

---

### [Polymer.KoaInputCharCounterBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html) offers

#### Behaviors

##### [Polymer.KoaInputAddonBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html)

###### Host attributes

Attribute | Value
----------|------
***add-on*** | `''`

###### Methods

Name | Description
-----|------------
***update()*** | The function called by `<koa-input-container>` when the input value or validity changes.

#### Methods

Name | Description
-----|------------
***update()*** |

# &lt;koa-input&gt; & &lt;koa-textarea&gt;

## &lt;koa-input&gt;

Es un campo de texto simple.

### Demo

* Demo con [paper-input](https://elements.polymer-project.org/elements/paper-input?view=demo).
* Demo con [ios-input](https://kingofapp.github.io/ios-input).

### Estilos

Mira `<koa-input-container>` para obtener la lista de las propiedades personalizadas usadas para eltilizar el elemento.

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
***list*** | `String` | The datalist of the input (if any). This should match the id of an existing `<datalist>`. Enlaza esto con la propiedad `<input is="iron-input">` `list`. |
***max*** | `String` | The maximum (numeric or date-time) input value. Can be a String (e.g. "2000-1-1") or a Number (e.g. 2). Enlaza esto con la propiedad `<input is="iron-input">` `max`. |
***maxlength*** | `Number` | The maximum length of the input value. Enlaza esto con la propiedad `<input is="iron-input">` `maxlength`. |
***min*** | `String` | The minimum (numeric or date-time) input value. Enlaza esto con la propiedad `<input is="iron-input">` `min`. |
***minlength*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `minlength`. |
***multiple*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `multiple` property, usado con type=file. |
***name*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `name`. |
***pattern*** | `String` | A pattern to validate the input with. Enlaza esto con la propiedad `<input is="iron-input">` `pattern`. |
***placeholder*** | `String` | A placeholder string in addition to the label. If this is set, the label will always float. | `''`
***preventInvalidInput*** | `Boolean` | Establece a verdadero para prevent the user from entering invalid input. Enlaza esto con la propiedad `<input is="iron-input">` `preventInvalidInput`. |
***readonly*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `readonly`. |
***required*** | `Boolean` | Establece a verdadero para mark the input as required. Enlaza esto con la propiedad `<input is="iron-input">` `required`. |  `false`
***results*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `results` property, usado con type=search. |
***size*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `size`. |
***step*** | `String` | Limits the numeric or date-time increments. Enlaza esto con la propiedad `<input is="iron-input">` `step`. |
***type*** | `String` | The type of the input. The supported types are text, number and password. Enlaza esto con la propiedad `<input is="iron-input">` `type`. |
***validator*** | `String` | Name of the validator to use. Enlaza esto con la propiedad `<input is="iron-input">` `validator` |
***value*** | `String` | The value for this input. Enlaza esto con la propiedad `<input is="iron-input">` `bindValue` property, or the `value` property of your input that is `notify:true`. |

#### Methods

Name | Description
-----|------------
***validate()*** | Validates the input element and sets an error style if needed.


## &lt;koa-textarea&gt;

It is a multi-line text field.

### Demo

* Demo with [paper-textarea](https://elements.polymer-project.org/elements/paper-input?view=demo).
* Demo with [ios-textarea](https://kingofapp.github.io/ios-input).

### Styling

See `<koa-input-container>` for a list of custom properties used to style this element.

---

### [Polymer.KoaTextareaBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-textarea-behavior.html) offers

#### Behaviors

##### [Polymer.KoaInputBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html)

###### Properties

Name | Type | Description | Default
-----|------|-------------|--------
***accept*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `accept`, usado con type=file. |
***allowedPattern*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `allowedPattern`. |
***autocapitalize*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocapitalize`. | `none`
***autocomplete*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocomplete`. | `off`
***autocorrect*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocorrect`. | `off`
***autofocus*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `autofocus`. |
***autosave*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autosave`, usado con type=search. |
***autoValidate*** | `String` | Establece a verdadero para auto-validate the input value. Enlaza esto con la propiedad input-container's `autoValidate`. | `false`
***charCounter*** | `Boolean` | Establece a verdadero para show a character counter. | `false`
***disabled*** | `Boolean` | Establece a verdadero para disable this input. Bind this to both the `<koa-input-container>` and the input's `disabled`. | `false`
***errorMessage*** | `String` | The error message to display when the input is invalid. Enlaza esto con la propiedad `<koa-input-error>` content, if using. |
***inputmode*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `inputmode`. |
***invalid*** | `Boolean` | Returns true if the value is invalid. Bind this to both the `<koa-input-container>` and the input's `invalid`. | `false`
***label*** | `String` | The label for this input. Bind this to `<label>` content and `hidden` property, e.g. `<label hidden$="[[!label]]">[[label]]</label>` in your `template` |
***list*** | `String` | The datalist of the input (if any). This should match the id of an existing `<datalist>`. Enlaza esto con la propiedad `<input is="iron-input">` `list`. |
***max*** | `String` | The maximum (numeric or date-time) input value. Can be a String (e.g. "2000-1-1") or a Number (e.g. 2). Enlaza esto con la propiedad `<input is="iron-input">` `max`. |
***maxlength*** | `Number` | The maximum length of the input value. Enlaza esto con la propiedad `<input is="iron-input">` `maxlength`. |
***min*** | `String` | The minimum (numeric or date-time) input value. Enlaza esto con la propiedad `<input is="iron-input">` `min`. |
***minlength*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `minlength`. |
***multiple*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `multiple` property, usado con type=file. |
***name*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `name`. |
***pattern*** | `String` | A pattern to validate the input with. Enlaza esto con la propiedad `<input is="iron-input">` `pattern`. |
***placeholder*** | `String` | A placeholder string in addition to the label. If this is set, the label will always float. | `''`
***preventInvalidInput*** | `Boolean` | Establece a verdadero para prevent the user from entering invalid input. Enlaza esto con la propiedad `<input is="iron-input">` `preventInvalidInput`. |
***readonly*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `readonly`. |
***required*** | `Boolean` | Establece a verdadero para mark the input as required. Enlaza esto con la propiedad `<input is="iron-input">` `required`. |  `false`
***results*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `results` property, usado con type=search. |
***size*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `size`. |
***step*** | `String` | Limits the numeric or date-time increments. Enlaza esto con la propiedad `<input is="iron-input">` `step`. |
***type*** | `String` | The type of the input. The supported types are text, number and password. Enlaza esto con la propiedad `<input is="iron-input">` `type`. |
***validator*** | `String` | Name of the validator to use. Enlaza esto con la propiedad `<input is="iron-input">` `validator` |
***value*** | `String` | The value for this input. Enlaza esto con la propiedad `<input is="iron-input">` `bindValue` property, or the `value` property of your input that is `notify:true`. |

#### Properties

Name | Type | Description | Default
-----|------|-------------|--------
***rows*** | `Number` | The initial number of rows. | `1`
***maxRows*** | `Number` | The maximum number of rows this element can grow to until it scrolls. 0 means no maximum. | `0`


## &lt;koa-input-container&gt;

It is a container for a `<label>`, an `<input is="iron-input">` or `<iron-autogrow-textarea>` and optional add-on elements such as an error message or character counter.

### Styling

Custom property | Description | Default
----------------|-------------|--------
`--input-container-color` | Label and underline color when the input is not focused | `--secondary-text-color`
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



























---

---

---

---

---

## &lt;koa-input&gt;

It is a single-line text field.

### Demo

* Demo with [paper-input](https://elements.polymer-project.org/elements/paper-input?view=demo).
* Demo with [ios-input](https://kingofapp.github.io/ios-input).

### Styling

Custom property | Description | Default
----------------|-------------|--------
`--input-container-color` | Label and underline color when the input is not focused | `--secondary-text-color`
`--input-container-focus-color` | Label and underline color when the input is focused | `--default-primary-color`
`--input-container-invalid-color` | Label and underline color when the input is is invalid | `#db4437`
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

### [KoaInputBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html) offers

#### Behaviors

##### [Polymer.PaperInputBehavior](https://elements.polymer-project.org/elements/paper-input?active=Polymer.PaperInputBehavior)

###### Properties

Name | Type | Description | Default
-----|------|-------------|--------
*accept* | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `accept` property, usado con type=file. |
*allowedPattern* | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `allowedPattern`. |
*autocapitalize* | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocapitalize`. | `none`
*autocomplete* | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocomplete`. | `off`
*autocorrect* | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocorrect`. | `off`
*autofocus* | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `autofocus`. |
*autosave* | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autosave` property, usado con type=search. |
*disabled* | `Boolean` | Establece a verdadero para disable this input. |
*focused* | `Boolean` | Sí verdadero, the element currently has focus. |
*inputmode* | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `inputmode`. |
*invalid* | `Boolean` | Returns true if the value is invalid. |
*list* | `String` | The datalist of the input (if any). This should match the id of an existing `<datalist>`. Enlaza esto con la propiedad `<input is="iron-input">` `list`. |
*max* | `String` | The maximum (numeric or date-time) input value. Can be a String (e.g. "2000-1-1") or a Number (e.g. 2). Enlaza esto con la propiedad `<input is="iron-input">` `max`. |
*maxlength* | `Number` | The maximum length of the input value. Enlaza esto con la propiedad `<input is="iron-input">` `maxlength`. |
*min* | `String` | The minimum (numeric or date-time) input value. Enlaza esto con la propiedad `<input is="iron-input">` `min`. |
*minlength* | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `minlength`. |
*multiple* | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `multiple` property, usado con type=file. |
*name* | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `name`. |
*pattern* | `String` | A pattern to validate the input with. Enlaza esto con la propiedad `<input is="iron-input">` `pattern`. |
*placeholder* | `String` | A placeholder string in addition to the label. |
*preventInvalidInput* | `Boolean` | Establece a verdadero para prevent the user from entering invalid input. Enlaza esto con la propiedad `<input is="iron-input">` `preventInvalidInput`. |
*readonly* | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `readonly`. |
*required* | `Boolean` | Establece a verdadero para mark the input as required. Enlaza esto con la propiedad `<input is="iron-input">` `required` pro
*results* | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `results` property, usado con type=search. |
*size* | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `size`. |
*step* | `String` | Limits the numeric or date-time increments. Enlaza esto con la propiedad `<input is="iron-input">` `step`. |
*type* | `String` | The type of the input. The supported types are text, number and password. Enlaza esto con la propiedad `<input is="iron-input">` `type`. |
*value* | `String` | The value for this input. Enlaza esto con la propiedad `<input is="iron-input">` `bindValue` property, or the `value` property of your input that is notify:true. |

#### Properties

Name | Type | Description | Default
-----|------|-------------|--------
***label*** | `String` | The label for this input. |

### Methods

Name | Description
-----|------------
***inputElement()*** | Returns a reference to the input element.


## &lt;koa-textarea&gt;

It is a multi-line text field.

### Demo

* Demo with [paper-textarea](https://elements.polymer-project.org/elements/paper-input?view=demo).
* Demo with [ios-textarea](https://kingofapp.github.io/ios-input).

### Styling

Custom property | Description | Default
----------------|-------------|--------
`--input-container-color` | Label and underline color when the input is not focused | `--secondary-text-color`
`--input-container-focus-color` | Label and underline color when the input is focused | `--default-primary-color`
`--input-container-invalid-color` | Label and underline color when the input is is invalid | `--google-red-500`
`--input-container-input-color` | Input foreground color | `--primary-text-color`
`--input-container` | Mixin applied to the container | `{}`
`--input-container-disabled` | Mixin applied to the container when it's disabled | `{}`
`--input-container-label` | Mixin applied to the label | `{}`
`--input-container-label-focus` | Mixin applied to the label when the input is focused | `{}`
`--input-container-input` | Mixin applied to the input | `{}`
`--input-container-underline` | Mixin applied to the underline | `{}`
`--input-container-underline-focus` | Mixin applied to the underline when the input is focued | `{}`
`--input-container-underline-disabled` | Mixin applied to the underline when the input is disabled | `{}`

---

### [KoaTextareaBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-textarea-behavior.html) offers

#### Behaviors

##### [Polymer.PaperInputBehavior](https://elements.polymer-project.org/elements/paper-input?active=Polymer.PaperInputBehavior)

###### Properties

The same as `koa-input` and:

Name | Type | Description | Default
-----|------|-------------|--------
***rows*** | `Number` | The initial number of rows. | `1`
***maxRows*** | `Number` | The maximum number of rows this element can grow to until it scrolls. 0 means no maximum. | `0`

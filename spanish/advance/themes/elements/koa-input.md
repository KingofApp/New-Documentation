# &lt;koa-input&gt; & &lt;koa-textarea&gt;

## &lt;koa-input&gt;

Es un campo de texto simple.

### Demo

* Demo con [paper-input](https://elements.polymer-project.org/elements/paper-input?view=demo).
* Demo con [ios-input](https://kingofapp.github.io/ios-input).

### Estilos

Ver [<koa-input-container>](#koa-input-container) para obtener la lista de las propiedades personalizadas usadas para utilizar el elemento.

---

### [Polymer.KoaInputBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html)

#### Comportamientos

##### [Polymer.IronFormElementBehavior](https://elements.polymer-project.org/elements/iron-form-element-behavior)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*name* | `String` | El nombre de este elemento. |
*required* | `Boolean` | Se establece a verdadero (true) para hacer que el input sea requerido. Sí lo usas en un formulario, un elemento personalizado que use este comportamiento deberá también usar `Polymer.IronValidatableBehavior` y definir un método de validación personalidado. De otro modo, un elemento requerido siempre será considerado válido. Es muy recomendable que proporciones un estilo visual para el elemento cuando su valor sea invalido. | `false`
*value* | `String` | El valor de este elemento. |

##### [Polymer.IronControlState](https://elements.polymer-project.org/elements/iron-behaviors?active=Polymer.IronControlState) contiene

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*disabled* | `Boolean` | Si es verdadero (true), el usuario no podrá interactuar con este elemento. | `false`
*focused* | `Boolean` | Si es verdadero (true), el elemento tendrá el foco. | `false`

#### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
***accept*** | `String` | Expresión regular que lista los caracteres permitidos como entrada. Este patrón representa los caracteres permitidos para el campo; A medida que el usuario ingresa texto, cada carácter individual se verificará contra el patrón (en lugar de comprobar todo el valor como un todo). El formato recomendado debe ser una lista de caracteres permitidos; Por ejemplo, [a-zA-Z0-9. + - !;:] `<input is="iron-input">` `accept`, usado con type=file. |
***allowedPattern*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `allowedPattern`. |
***autocapitalize*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocapitalize`. | `none`
***autocomplete*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocomplete`. | `off`
***autocorrect*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autocorrect`. | `off`
***autofocus*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `autofocus`. |
***autosave*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `autosave`, usado con type=search. |
***autoValidate*** | `String` | Se establece a verdadero (true) para auto-validar el valor del input. Enlaza esto con la propiedad input-container `autoValidate`. | `false`
***charCounter*** | `Boolean` | Se establece a verdadero (true) para mostrar el contador de caracteres. | `false`
***disabled*** | `Boolean` | Se establece a verdadero (true) para deshabilitar este input. Enlaza los dos `<koa-input-container>` y la propiedad `disabled` del input. | `false`
***errorMessage*** | `String` | El mensaje de error se mostrará cuando el input no es válido. Enlaza esto con el contenido de `<koa-input-error>`, si se usa. |
***inputmode*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `inputmode`. |
***invalid*** | `Boolean` | Devuelve verdadero (true) si el valor no es válido. Enlaza los dos `<koa-input-container>` y la propiedad del input `invalid`. | `false`
***label*** | `String` | La etiqueta para este input. Enlaza esto con el contenido de `<label>` y la propiedad `hidden`, e.j. `<label hidden$="[[!label]]">[[label]]</label>` en el `template` |
***list*** | `String` | El datalist del input (si lo hay). Este debe coincidor con el id de un `<datalist>` existente. Enlaza esto con la propiedad `<input is="iron-input">` `list`. |
***max*** | `String` | El máximo (numérico o date-time) valor del input. Puede ser un string (e.j. "2000-1-1") o un número (e.j. 2). Enlaza esto con la propiedad `<input is="iron-input">` `max`. |
***maxlength*** | `Number` | La longitud máxima del valor del input. Enlaza esto con la propiedad `<input is="iron-input">` `maxlength`. |
***min*** | `String` | El mínimo (numérico o date-time) valor del input. Enlaza esto con la propiedad `<input is="iron-input">` `min`. |
***minlength*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `minlength`. |
***multiple*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `multiple` property, usado con type=file. |
***name*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `name`. |
***pattern*** | `String` | Un patrón para validar el ancho del input. Enlaza esto con la propiedad `<input is="iron-input">` `pattern`. |
***placeholder*** | `String` | Un texto para el placeholder (para extender la etiqueta). Si esta establecido, la etiqueta estará siempre flotando. | `''`
***preventInvalidInput*** | `Boolean` | Se establece a verdadero (true) para prevenir que el usuario introduzca un input no válido. Enlaza esto con la propiedad `<input is="iron-input">` `preventInvalidInput`. |
***readonly*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `readonly`. |
***required*** | `Boolean` | Se establece a verdadero (true) para marcar el input como requerido. Enlaza esto con la propiedad `<input is="iron-input">` `required`. |  `false`
***results*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `results`, usado con type=search. |
***size*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `size`. |
***step*** | `String` | Limita los incrementos del número o del date-time. Enlaza esto con la propiedad `<input is="iron-input">` `step`. |
***type*** | `String` | El tipo del input. Los tipos soportados son text, number y password. Enlaza esto con la propiedad `<input is="iron-input">` `type`. |
***validator*** | `String` | Nombre del validador para usar. Enlaza esto con la propiedad `<input is="iron-input">` `validator` |
***value*** | `String` | El valor de este input. Enlaza esto con la propiedad `<input is="iron-input">` `bindValue`, o  la propiedad `value` del input que es `notify:true`. |

#### Métodos

Nombre | Descripción
-----|------------
***validate()*** | Valida el elemento del input y establece un estilo al error si es necesario.


## &lt;koa-textarea&gt;

Es un campo de texto multilínea.

### Demo

* Demo con [paper-textarea](https://elements.polymer-project.org/elements/paper-input?view=demo).
* Demo con [ios-textarea](https://kingofapp.github.io/ios-input).

### Styling

Ver [<koa-input-container>](#koa-input-container) para el listado de las propiedades personalizadas usadas para estilizar este elemento.

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
***autoValidate*** | `String` |Se establece a verdadero (true) para auto validar el valor del input. Enlaza esto con la propiedad del input-container `autoValidate`. | `false`
***charCounter*** | `Boolean` |Se establece a verdadero (true) para mostrar el contador de caracteres. | `false`
***disabled*** | `Boolean` |Se establece a verdadero (true) para deshabilitar el input. Enlaza ambos al `<koa-input-container>` y a la propiedad `disabled`. | `false`
***errorMessage*** | `String` | El mensaje de error a mostrar cuando el input no es válido. Enlaza esto con el contenido `<koa-input-error>`, sí se usa. |
***inputmode*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `inputmode`. |
***invalid*** | `Boolean` | Devuelve verdadero si el valor no es válido. Enlaza esto a `<koa-input-container>` y a la propiedad `invalid` del input. | `false`
***label*** | `String` | La etiqueta para este input. Enlaza esto al contenido del `<label>` y a la propiedad `hidden`, e.j. `<label hidden$="[[!label]]">[[label]]</label>` en el `template` |
***list*** | `String` | El datalist del input (sí lo hay). Este debe coincidor con el id de un `<datalist>` existente. Enlaza esto con la propiedad `<input is="iron-input">` `list`. |
***max*** | `String` | El máximo (numérico o date-time) valor del input. Puede ser un string (e.j. "2000-1-1") o un número (e.j. 2). Enlaza esto con la propiedad `<input is="iron-input">` `max`. |
***maxlength*** | `Number` | La longitud máxima del valor del input. Enlaza esto con la propiedad `<input is="iron-input">` `maxlength`. |
***min*** | `String` | El mínimo (numérico o date-time) valor del input. Enlaza esto con la propiedad `<input is="iron-input">` `min`. |
***minlength*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `minlength`. |
***multiple*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `multiple`, usado con type=file. |
***name*** | `String` | Enlaza esto con la propiedad `<input is="iron-input">` `name`. |
***pattern*** | `String` | Un patrón para validar el ancho del input. Enlaza esto con la propiedad `<input is="iron-input">` `pattern`. |
***placeholder*** | `String` | Un texto para el placeholder (para extender la etiqueta). Sí está establecido, la etiqueta estará siempre flotante. | `''`
***preventInvalidInput*** | `Boolean` | Se establece a verdadero (true) para prevenir que el usuario introduzca un input no válido. Enlaza esto con la propiedad `<input is="iron-input">` `preventInvalidInput`. |
***readonly*** | `Boolean` | Enlaza esto con la propiedad `<input is="iron-input">` `readonly`. |
***required*** | `Boolean` | Se establece a verdadero (true) para marcar el input como requerido. Enlaza esto con la propiedad `<input is="iron-input">` `required`. |  `false`
***results*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `results`, usado con type=search. |
***size*** | `Number` | Enlaza esto con la propiedad `<input is="iron-input">` `size`. |
***step*** | `String` | Limita los incrementos del número o del date-time. Enlaza esto con la propiedad `<input is="iron-input">` `step`. |
***type*** | `String` | El tipo del input. Los tipos soportados son text, number y password. Enlaza esto con la propiedad `<input is="iron-input">` `type`. |
***validator*** | `String` | Nombre del validador para usar. Enlaza esto con la propiedad `<input is="iron-input">` `validator` |
***value*** | `String` | El valor de este input. Enlaza esto con la propiedad `<input is="iron-input">` `bindValue`, o  la propiedad `value` del input que es `notify:true`. |

#### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
***rows*** | `Number` | El número inicial de filas. | `1`
***maxRows*** | `Number` | El máximo número de filas que este elemento puede crecer hasta hacer scroll. 0 Significa que no hay máximo. | `0`


## &lt;koa-input-container&gt;

Es un contenedor para `<label>`, `<input is="iron-input">` o `<iron-autogrow-textarea>` y más elementos add-on opcionales como el mensaje de error o el contador de caracteres.

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--input-container-color` | Color de la etiqueta y de la línea inferior del input. | `--secondary-text-color`
`--input-container-focus-color` | Color de la etiqueta y de la línea inferior cuando el input está con el foco. | `--default-primary-color`
`--input-container-invalid-color` | Color de la etiqueta y de la línea inferior cuando el input es no válido. | `--google-red-500`
`--input-container-input-color` | Color del input. | `--primary-text-color`
`--input-container` | Mixin aplicado al contenedor. | `{}`
`--input-container-disabled` | Mixin aplicado al contenedor cuando está deshabilitado. | `{}`
`--input-container-label` | Mixin aplicado a la etiqueta. | `{}`
`--input-container-label-focus` | Mixin aplicado a la etiqueta cuando el input tiene el foco. | `{}`
`--input-container-input` | Mixin aplicado al input. | `{}`
`--input-container-underline` | Mixin aplicado a la línea inferior. | `{}`
`--input-container-underline-focus` | Mixin aplicado a la línea inferior cuando el input tiene el foco. | `{}`
`--input-container-underline-disabled` | Mixin aplicado a la línea inferior cuando el input está deshabilitado. | `{}`
`--input-prefix` | Mixin aplicado al prefijo del input. | `{}`
`--input-suffix` | Mixin aplicado al sufijo del input. | `{}`

---

### [Polymer.KoaInputContainerBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html) ofrece

#### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
***attrForValue*** | `String` | El atributo que escucha cambios en el valor. | `'bind-value'`
***autoValidate*** | `Boolean` | Se establece a verdadero (true) para auto validar el valor del input cuando cambia. | `false`
***focused*** | `Boolean` | Es verdadero (true) sí el input tiene el foco. | `false`
***invalid*** | `Boolean` | Es verdadero (true) sí el input no es válido. Esta propiedad se establece automáticamente cuando el valor del input cambia si está auto validada o cuando el evento `iron-input-validate` está escuchando de un hijo. | `false`


## &lt;koa-input-error&gt;

Es un mensaje de error usado con el  [<koa-input-container>](#koa-input-container) . El error se muestra cuando el `<koa-input-container>` es `invalid`.

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--input-container-invalid-color` | Color de la etiqueta y de línea inferior cuando el input no es válido | `#db4437`
`--input-error` | Mixin aplicado al error | `{}`

---

### [Polymer.KoaInputErrorBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html) ofrece

#### Comportamientos

##### [Polymer.KoaInputAddonBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html)

###### Atributos del Host

Atributo | Valor
----------|------
***add-on*** | `''`

###### Métodos

Nombre | Descripción
-----|------------
***update()*** | La función llamada por el  [<koa-input-container>](#koa-input-container)  cuando el valor del input o la validez cambia.

#### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
***invalid*** | `Boolean` | Es verdadero (true) si el error se está mostrando. |


## &lt;koa-input-char-counter&gt;

Es un contador de caracteres usado con el  [<koa-input-container>](#koa-input-container) . Muestra el número de caracteres insertados en el input y el tamaño máximo de este si está definido.

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--input-char-counter` | Mixin aplicado al elemento.	| `{}`

---

### [Polymer.KoaInputCharCounterBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html) ofrece

#### Comportamientos

##### [Polymer.KoaInputAddonBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-input-behavior.html)

###### Atributos del Host

Atributo | Valor
----------|------
***add-on*** | `''`

###### Métodos

Nombre | Descripción
-----|------------
***update()*** | La función llamada por el [<koa-input-container>](#koa-input-container) cuando el valor del input o la validez cambia.

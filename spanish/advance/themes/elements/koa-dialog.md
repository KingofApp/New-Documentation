# &lt;koa-dialog&gt;

Es un diálogo (tipo modal). Proporciona estilos a las cabeceras, área de contenido y área de acción para botones.

### Demo

* Demo con [paper-dialog](https://elements.polymer-project.org/elements/paper-dialog?view=demo).

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--dialog-background-color` | Color de fondo del dialogo | `--primary-background-color`
`--dialog-color` | Color principal del dialogo | `--primary-text-color`
`--dialog` | Mixin aplicado al dialogo | `{}`
`--dialog-title` | Mixin aplicado al elemento del título (`<h2>`) | `{}`
`--dialog-button-color` | Color principal del área de botones | `--default-primary-color`

---

### [KoaDialogBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-dialog-behavior.html)

#### Comportamientos

##### [Polymer.IronOverlayBehavior](https://elements.polymer-project.org/elements/iron-overlay-behavior?active=Polymer.IronOverlayBehavior)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*canceled* | `Boolean` | Verdadero sí la superposición se cancela cuando se cerro por última vez. | `false`
*noCancelOnEscKey* | `Boolean` | Establece a verdadero para deshabilitar la acción de cancelar cuando se pulsa la tecla de ESC. | `false`
*noCancelOnOutsideClick* | `Boolean` | Establece a verdadero para deshabilitar la acción de cancelar cuando se pulsa fuera del dialogo. | `false`
*opened* | `Boolean` | Verdadero sí la superposición se muestra actualmente. | `false`
*withBackdrop* | `Boolean` | Establece a verdadero para mostrar un backDrop detrás de la superposición. | `false`

###### Métodos

Nombre | Descripción
-----|------------
*cancel()* | Cancela la superposición.
*center()* | Centra horizontalmente y verticalmente sí no esta ya posicionado. Esto tambien establece `position:fixed`.
*close()* | Cierra la superposición.
*open()* | Abre la superposición.
*toggle()* | Cambia el estado de apertura de la superposición.

#### Atributos del Host

Atributo | Valor
----------|------
***role*** | `'dialog'`
***tabindex*** | `-1`

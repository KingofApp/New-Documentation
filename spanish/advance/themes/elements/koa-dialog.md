# &lt;koa-dialog&gt;

Es una ventana emergente (tipo modal). Dicha ventana emergente puede personalizarse proporcionando estilos a las cabeceras, área de contenido y área de acción para botones.

### Demo

* Demo con [paper-dialog](https://elements.polymer-project.org/elements/paper-dialog?view=demo).

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--dialog-background-color` | Color de fondo de la ventana emergente. | `--primary-background-color`
`--dialog-color` | Color principal de la ventana emergente. | `--primary-text-color`
`--dialog` | Mixin aplicado a la ventana emergente. | `{}`
`--dialog-title` | Mixin aplicado al elemento del título. (`<h2>`) | `{}`
`--dialog-button-color` | Color principal del área de botones. | `--default-primary-color`

---

### [KoaDialogBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-dialog-behavior.html)

#### Comportamientos

##### [Polymer.IronOverlayBehavior](https://elements.polymer-project.org/elements/iron-overlay-behavior?active=Polymer.IronOverlayBehavior)

###### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
*canceled* | `Boolean` | Es verdadero (true) sí la ventana emergente fue cancelada cuando se cerró por última vez. | `false`
*noCancelOnEscKey* | `Boolean` | Se establece a verdadero (true) para deshabilitar la acción de cancelar cuando se pulsa la tecla ESC. | `false`
*noCancelOnOutsideClick* | `Boolean` | Se establece a verdadero (true) para deshabilitar la acción de cancelar cuando se pulsa fuera del dialogo. | `false`
*opened* | `Boolean` | Es verdadero (true) sí la ventana emergente se muestra actualmente. | `false`
*withBackdrop* | `Boolean` | Se establece a verdadero (true) para mostrar un backDrop detrás de la ventana emergente. | `false`

###### Métodos

Nombre | Descripción
-----|------------
*cancel()* | Cierra la ventana emergente.
*center()* | Centra horizontalmente y verticalmente la ventana emergente sí no esta ya posicionada. Esto tambien se establece con `position:fixed`.
*close()* | Cierra la ventana emergente.
*open()* | Abre la ventana emergente.
*toggle()* | Cambia el estado de apertura de la ventana emergente.

#### Atributos del Host

Atributo | Valor
----------|------
***role*** | `'dialog'`
***tabindex*** | `-1`

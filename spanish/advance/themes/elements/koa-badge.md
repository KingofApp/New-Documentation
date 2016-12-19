# &lt;koa-badge&gt;

Es un badge (icono de notificación) que se muestra en la esquina superior derecha del elemento, representado un estado o notificación

### Demo

* Demo con [paper-badge](https://elements.polymer-project.org/elements/paper-badge?view=demo).

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--badge-background` | Es el color de fondo del badge | `--accent-color`
`--badge-opacity` | La opacidad del badge | `1.0`
`--badge-text-color` | El color del texto del badge | `white`
`--badge-width` | El ancho del circulo del badge | `22px`
`--badge-height` | El alto del circulo del badge | `22px`
`--badge-margin-left` | Espacio opcional añadido a la izquierda del badge. | `0px`
`--badge-margin-bottom` | Espacio opcional añadido debajo del badge. | `0px`
`--badge` | Mixin aplicado al badge | `{}`

---

### [KoaBadgeBehavior](https://github.com/KingofApp/koa-behaviors/blob/master/koa-badge-behavior.html)

#### Atributos del host

Atributo | Valor
----------|------
***role*** | `'status'`
***tabindex*** | `0`

#### Propiedades

Nombre | Tipo | Descripción | Por defecto
-----|------|-------------|--------
***for*** | `String` | El id del elemento del badge al que quieres anclar. |
***label*** | `String` | La etiqueta que se verá en el badge. La etiqueta estará centrada e idealmente deberá tener pocos carácteres. |
***target*** |  | Devuelve el elemento al que el badge esta anclado. Es el mismo valor que  Returns the target element that this badge is anchored to. Es el elemento dado por el atributo for o el padre inmediato del badge.

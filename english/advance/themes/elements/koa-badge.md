# &lt;koa-badge&gt;

Es un badge (icono de notificación) que se muestra en la esquina superior derecha del elemento, representando un estado o notificación

### Demo

* Demo con [paper-badge](https://elements.polymer-project.org/elements/paper-badge?view=demo).

### Estilos

Propiedad personalizada | Descripción | Por defecto
----------------|-------------|--------
`--badge-background` | Es el color de fondo del badge | `--accent-color`
`--badge-opacity` | La opacidad del badge | `1.0`
`--badge-text-color` | El color del texto del badge | `white`
`--badge-width` | El ancho del círculo del badge | `22px`
`--badge-height` | El alto del círculo del badge | `22px`
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
***for*** | `String` | El id del elemento del badge al que se quiere anclar. |
***label*** | `String` | La etiqueta que se visualizará en el badge. La etiqueta aparecerá centrada e idealmente deberá contener pocos caracteres. |
***target*** |  | Devuelve el elemento al que el badge esta anclado. Es, o el elemento dado por el atributo for, o el padre inmediato del badge.

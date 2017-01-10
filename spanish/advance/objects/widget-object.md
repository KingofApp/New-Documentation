# Widget object

Este objeto se utiliza para definir como se mostrará la vista de administración del módulo dentro de builder. En caso de que no exista este objeto dentro del [objeto del módulo](module-object.md) se interpretará que el módulo o servicio no dispone de sección de administración.

A continuación describimos sus elementos:

| Campo | Descripción                                                                 | Requerido | Formato |
| ----- | --------------------------------------------------------------------------- | --------- | ------- |
| title | Nombre que se mostrará en la sección del builder para identificar el widget | Si        | String  |
| url   | Url donde se puede encontrar el fichero html del iframe a cargar            | Si        | URL     |


Ejemplo:

```json
{
  "title": "Push - Open Signals",
  "url"  : "/services/my-module/widget"
}
```


Documentación relacionada | Objetos donde se usa
--------------------------|--------------------------
<ul><li>[Widgets en modulos](../modules/widget.md)</li></ul> | <ul><li>[Module object object](module-object.md)</li></ul>

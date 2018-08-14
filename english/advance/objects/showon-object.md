# showOn

Este objeto indica donde va a ser visible un plugin (módulo, tema o servicio).

* market: Valor booleano, indica si el plugin va a listarse en el market.
* menu: Valor booleano, indica si el plugin va a mostrarse en el menú de dentro de la aplicación. En caso de tratsrse de un módulo o servicio de tipo transversal, como por ejemplo el login, tiene más sentido que no se muestre.
* dropDown: Valor booleano, indica si el módulo va a mostrarse en la vista Drag and Drop de módulos, En el caso de que sea un módulo hijo de otro tiene sentido que no se muestre .


```json
{
  "showOn": {
    "market": true,
    "menu": true,
    "dropDown": true
  }

}
```

*En el caso de los temas, solo tiene sentido mostrar el market*

*En el caso de los servicios, el dropDown no tendrá ningún efecto*

*En el caso de los módulos, las 3 variables pueden ser usadas*

## Referencias

Documentación relacionada | Objetos donde se usa
--------------------------|--------------------------
<ul><li>[Temas -> Más cosas del config.json](../themes/themes.md#más-cosas-del-configjson)</li></ul> | <ul></ul>

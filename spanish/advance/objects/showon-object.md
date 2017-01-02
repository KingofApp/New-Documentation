# showOn

Este objeto indica donde se quiere que el módulo, tema o servicio sea visible.

* market: Valor booleano, indica si quieres que sea listado en el market.
* menu: Valor booleano, indica si quieres que se muestre en el menú de dentro de la aplicación, tiene sentido no mostrarlo en caso de que sea un módulo o servicio del tipo transversal, como por ejemplo login.
* dropDown: Valor booleano, indica si quieres que se muestre en la vista Drag and Drop de módulos, tiene sentido ocultar este módulo en el caso de que sea un módulo hijo de otro.


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


### Referencias
* Ver [Temas -> Más cosas del config.json](../themes/themes.md#mas-cosas-del-config.json)

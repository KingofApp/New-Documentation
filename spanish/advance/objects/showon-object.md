# showOn

Este objeto indica donde quieres que el módulo, tema o servicio sea visible.

* market: Sí verdadero, indica si quieres que sea listado en el market.
* menu: Sí verdadero, indica si quieres que se pueda mostrar en el menú de dentro de la aplicación, tiene sentido no mostrarlo en caso de que sea un módulo o servicio del tipo transversal como por ejemplo login.
* dropDown: Sí verdadero, indica si quieres que se muestre en la vista drag and drop de módulos, tiene sentido ocultar este módulo en el caso de que sea un módulo hijo de otro.


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

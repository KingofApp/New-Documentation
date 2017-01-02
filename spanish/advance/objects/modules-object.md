# Modules objects

Este objeto es uno de los más importes de toda la aplicación, su función es establecer las vistas y como se ordenan dentro de la aplicación. El objeto utiliza como clave la ruta y anidación dentro de la aplicación.

Ejemplo:
```json
{
  "/menu-a0001"                       : {"Module": "Object"},
  "/menu-a0001/view1-a0002"           : {"Module": "Object"},
  "/menu-a0001/view2-a0003"           : {"Module": "Object"},
  "/menu-a0001/view3-a0004"           : {"Module": "Object"},
  "/menu-a0001/view3-a0004/sub-a0005" : {"Module": "Object"}
}
```

En el ejemplo anterios se estable 5 módulos:

| nombre | padres      | descripción |
| ------ | ----------- | ----------- |
| menu   | -           | Es el módulo que permite la navegación entre los diferentes elementos. Dentro de la aplicación puede que no sea posible acceder a el de forma independiente. Sirve de soporte para los demás módulos |
| view1  | `menu`        | Es la primera vista de la aplicación. En caso de que el menú determine que siga siendo visible, lo será. |
| view2  | `menu`        | Tiene el mismo comportamiento que la vista anterior. Obviamente cada vista tiene sus propios datos y funcionalidad |
| view3  | `menu`        | Este módulo es un híbrido entre las vistas anteriores y el menú. Es lo que se llama un [Módulo contenedor - ToLink]() |
| sub    | `menu` `view3` | Este submodulo actua como módulo final y comparte el espacio visual con el módulo `menu` y el módulo `view3` |

Visita la sección [Module object](module-object.md) encontrar una explicación completa del objeto de definición de cada módulo.

## Composicion de rutas

Todas las rutas se generan usando para cada sección un par compuesto por el `identifier` del módulo correspondiente y un código alfanumérico de 5 caracteres. Este par se repite tantas veces como sea necesirio generar la composición de módulos deseada.

```
[identifier1-alfanum]/[identifier1-alfanum]/...
```

Nota: Es importante utilizar nombres que tengan sentido y respeten la misma filosofía que la declaración de variables (minúsculas, sin acentos, etc...)

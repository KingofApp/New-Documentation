# Event object

Este objeto define los tipos de servicios o módulos que provee o requiere un módulo. Ejemplo:

```json
{
  "events" : {
    "require": [],
    "provide": ["payment"]
  }
}
```
En él se encuentran dos arrays `"require"` y `"provide"`, dentro de este array se formarán los strings de los eventos que provee o requiere dicho moódulo.

Por ejemplo si un módulo requiere de un servicio de pago, tendra que insertar en el array "require" el string "payment"

| Clave | Descripción  | Formato |
| ----- | ------------ | ------- |
| require | Array de strings indicando los módulos o servicios que requiere. | Array de strings |
| provide | Array de strings indicando los módulos o servicios que provee. | Array de strings |

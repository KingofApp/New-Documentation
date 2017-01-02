# Services object

Describe cada uno de los servicios que están configurados para la aplicación. Cada servicio solo puede estar presente una única vez en la aplicación.

Por ese motivo la estructura de este objecto tiene formato de *objeto de objetos* donde las claves del mismo son los `identifier` de cada uno de los servicios configurados.

Los objetos internos tienen el formato [Module object](module-object.md) pese a ser servicios, ya que ambos objetos contienen los mismos datos.

Ejemplo:
```json
{
  "googleanalytics" : {"Module": "object"},
  "pushnotification": {"Module": "object"},
  "moreservices"    : {"Module": "object"}
}
```

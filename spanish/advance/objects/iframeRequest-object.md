# IframeRequestObject

Este objeto se utiliza únicamente para configurar las comunicaciones entre los iframes utilizados en los widgets de administración y configuración de módulos.

El objeto se divide en dos apartados:

| Clave | Descripción                                                            | Requerido | Formato             |
| ----- | ---------------------------------------------------------------------- | --------- | ------------------- |
| urls  | Especifica las URLs a las que el widget podrá conectarse de forma segura | Si        | Iframe URLs object  |
| vars  | Indica las variable con las que se trabajará en la conexión segura     | Si        | Iframe Vars object  |

## Iframe URLs object

Indica las urls permitidas agrupándolas por el tipo de petición. Los verbos más comunes son HEAD, GET, POST, PUT o DELETE, pero se podría usar cualquier verbo valido.

Ejemplo:
```json
{
  "GET"  : [
    "https://example.com/api/v1/apps",
    "https://example.com/api/v1/users"
  ],
  "POST" : [
    "https://example.com/api/v1/apps",
    "https://example.com/api/v1/users"
  ],
  "PUT"  : [
    "https://example.com/api/v1/apps"
  ]
}
```

## Iframe Vars object

Las variables se agrupan en dos secciones:

| Clave   | Descripción                                                            | Requerido | Formato             |
| ------- | ---------------------------------------------------------------------- | --------- | ------------------- |
| allowed | Especifica las variables que la conexión segura debe reemplazar.       | Si        | Array de Strings    |
| blocked | Lista de los datos que se han de eliminar de la respuesta para no comprometer la seguridad. | Si        | Array de Strings    |

Ejemplo:

```json
{
  "allowed" : [
    "app.appleApnsp12",
    "app.appleApnsp12Pwd",
    "plugin.token"
  ],
  "blocked" : [
    "players",
    "messagable_players",
    "apns_certificates"
  ]
}
```

# Theme default config

Cada vez que añadimos un nuevo tema en el Builder, este nos pregunta si queremos utilizar los parametros por defecto del tema. Estos parametros por defecto se definen en este objeto y son:

* Colores,
* Imágenes de la aplicación,
* Fuentes
* Menú por defecto.

| Campo  | Descripción                                                  | Requerido | Formato                           |
| ------ | ------------------------------------------------------------ | --------- | --------------------------------- |
| colors | Identifica los colores por defecto asociados al tema.        | No        | [Color object](colors-object.md)  |
| images | Identifica las imágenes por defecto asociados al tema.       | No        | [Images object](images-object.md) |
| fonts  | Identifica las fuentes por defecto asociados al tema.        | No        | [Fonts object](fonts-object.md)   |
| menu   | Identifica el menú principal por defecto asociado al tema. Debe coincidier con el `identifier` del modulo que se desea utilizar. | No | String |

Ejemplo:
```json
"colors" : {
    "primaryTextColor" : "rgba(99,99,99,1)",
    "primaryBackgroundColor" : "rgba(255,255,255,1)",
    "secondaryTextColor" : "rgba(99,99,99,1)",
    "disabledTextColor" : "rgba(47,43,22,1)",
    "dividerColor" : "rgba(224,224,224,1)",
    "primaryColor" : "rgba(255,0,60,1)",
    "lightPrimaryColor" : "rgba(197,202,233,1)",
    "darkPrimaryColor" : "rgba(255,0,60,1)",
    "accentColor" : "rgba(250,190,40,1)",
    "lightAccentColor" : "rgba(250,190,40,1)",
    "darkAccentColor" : "rgba(250,190,40,1)",
    "errorColor" : "rgba(221,44,0,1)",
    "backgroundColor" : "rgba(248,236,194,1)"
},
"images" : {
    "background" : ""
},
"fonts" : {
    "primaryFontFamily" : {
        "name" : "Raleway",
        "url" : "https://fonts.googleapis.com/css?family=Raleway"
    },
    "titleFontFamily" : {
        "name" : "Bitter",
        "url" : "https://fonts.googleapis.com/css?family=Bitter"
    }
},
"menu" : "polymermenu"
```

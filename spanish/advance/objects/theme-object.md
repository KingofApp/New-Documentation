# Theme object

Describe todos los parámetros de un Tema:

| Campo | Descripción                                                                | Requerido | Formato       |
| ----- | -------------------------------------------------------------------------- | --------- | ------------- |
| _id   | Identificador único del tema. Se genera automáticamente en el Visualizer.  | No        | Hex (16 char) |
| name  | Nombre del tema que permite identificarlo de forma sencilla. Este valor se muestra en el *market place* de KingOfApp. | No | String |
| identifier | Identifica de forma inequívoca el tema.                               | Si        | [KoApp Plugin string](spanish/objects/koapp-plugin-string.md) |
| version | Código de versión. Cada vez que se actualiza el tema, se ha de incrementar. | Si | [Semantic versioning](http://semver.org/) |
| images | Define todas las imagenes que se mostrarán del tema dentro del *market place* de KingOfApp. | Si | [Plugin inmages object](spanish/objects/plugin-images-object.md) |

"price" : 0.0000000000000000,

"defaultConfig" : {
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
},
"main" : "http://dev.resources.kingofapp.com/themes/koapp-theme-candy/koapp-theme-candy.html",
"createdAt" : ISODate("2012-12-19T06:01:17.171Z"),
"path" : "http://dev.resources.kingofapp.com/themes/koapp-theme-candy/koapp-theme-candy.html",
"preview" : "http://dev.resources.kingofapp.com/themes/koapp-theme-candy/images/screenshot01.png",
"status" : false,
"isUpdated" : false

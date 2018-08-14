# Theme object

Describe todos los parámetros de un Tema:

| Campo | Descripción                                                                | Requerido | Formato       |
| ----- | -------------------------------------------------------------------------- | --------- | ------------- |
| _id   | Identificador único del tema. Se genera automaticamente en el Visualizer.  | No        | Hex (16 char) |
| name  | Nombre del tema que permite identificarlo de forma sencilla. Este valor se muestra en el *market place* de KingOfApp. | No | String |
| identifier | Identifica de forma inequívoca el tema.                               | Si | [KoApp Plugin string](koapp-plugin-string.md) |
| version | Código de versión. Cada vez que se actualiza el tema, se ha de incrementar.  | Si | [Semantic versioning](http://semver.org/) |
| price   | Precio del tema.                                                          | Si | Float |
| images  | Define todas las imágenes que se mostrarán del tema dentro del *market place* de KingOfApp. | Si | [Plugin images object](plugin-images-object.md) |
| defaultConfig | Define la configuración por defecto asociada a la plantilla. Se puede exportar a la aplicación. | No | [Theme default config](theme-default-config.md) |
| path | Fichero HTML principal que contiene todos los elementos del [tema](../themes/themes.md). | Si | Ruta a fichero HTML |
| createrAt | Fecha de creación del tema.                                                       | No | ISO Date            |
| status | Indica si actualmente hay alguna plantilla configurada para el entorno (Android, iOS, ...). | No | Ruta a fichero HTML |
| isUpdated | Fichero HTML principal que contiene todos los elementos del [tema](../themes/themes.md). | Si | Ruta a fichero HTML |

## Referencias

Documentación relacionada | Objetos donde se usa
--------------------------|--------------------------
<ul><li>[Temas ->Como crear temas](../themes/themes.md)</li></ul> | <ul></ul>

# Theme object

Describe todos los parámetros de un Tema:

| Campo | Descripción                                                                | Requerido | Formato       |
| ----- | -------------------------------------------------------------------------- | --------- | ------------- |
| _id   | Identificador único del tema. Se genera automaticamente en el Visualizer.  | No        | Hex (16 char) |
| name  | Nombre del tema y permite identificarlo de forma sencilla. Este valos se muestra en el *market place* de KingOfApp. | No | String |
| identifier | Identifica de forma inequívoca el tema.                               | Si | [KoApp Plugin string](koapp-plugin-string.md) |
| version | Código de versión. Cada vez que se actualiza el tema ha de incrementar.  | Si | [Semantic versioning](http://semver.org/) |
| price   | Precio del tema                                                          | Si | Float |
| images  | Define todas las imagenes que se mostrarán del tema dentro del *market place* de KingOfApp. | Si | [Plugin images object](plugin-images-object.md) |
| defaultConfig | Define como la configuración general asociada a la plantilla que puede exportar a la aplicación cuando es aplicada. | No | [Theme default config](theme-default-config.md) |
| path | Fichero html principal que contiene todos los elementos de [tema](../themes/themes.md). | Si | Ruta a fichero HTML |
| createrAt | Fecha de creación de la tema                                                       | No | ISO Date            |
| status | Indica si actualmente hay alguna plantilla configurada para el entorno (Android, iOS, ...). | No | Ruta a fichero HTML |
| isUpdated | Fichero html principal que contiene todos los elementos de [tema](../themes/themes.md). | Si | Ruta a fichero HTML |

Más información:
* [Como crear temas](../themes/themes.md)

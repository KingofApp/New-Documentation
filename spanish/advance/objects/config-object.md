# Config object

| Campo | Descripción                                                                | Requerido | Formato       |
| ----- | -------------------------------------------------------------------------- | --------- | ------------- |
| index | Ruta del módulo que se cargará por defecto al arrancar la aplicación.      | Si        | String (path) |
| colors | Especifica los valores de los colores definidos en la platadorma.         | Si        | [Colors object](colors-object.md) |
| fonts | Especifica las fuentes del texto de la aplicación.                                   | Si        | [Fonts object](fonts-object.md) |
| images | Permite enlazar todas las imagenes que utiliza la aplicación.             | Ver más   | [Images object](images-object.md) |
| lang   | Identifica todos los idiomas en los que está disponible la aplicación     | Si        | Array de [Country-Region Locale](https://developer.apple.com/library/content/documentation/MacOSX/Conceptual/BPInternational/LanguageandLocaleIDs/LanguageandLocaleIDs.html) |
| version | Código de versión. Cada vez que se sube una nueva versión a cualquier *market place* se ha de incrementar para reflejar la actualización de la aplicación. | Si | [Semantic versioning](http://semver.org/) |
| iconset | Set de iconos utilizado en la aplicación                                 | Si        |   [IconSet object](iconset-object.md) |
| theme | Nombre del tema activo. Debe ser uno de los incluidos en la sección Themes del objeto de configuración | Si | String |
| spinner | Datos del spinner que se deasea utilizar en la aplicación | Si | [Spinner object](spinner-object.md)

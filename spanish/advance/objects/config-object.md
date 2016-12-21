# Config object

| Campo | Descripción                                                                | Requerido | Formato       |
| ----- | -------------------------------------------------------------------------- | --------- | ------------- |
| index | Ruta del módulo que se cargará por defecto al arrancar la aplicación.      | Si        | String (path) |
| colors | Especifica los valores de los colores definidos en la platadorma.         | Si        | [Colors object](spanish/objects/colors-object.md) |
| fonts | Especifica las fuentes de la aplicación.                                   | Si        | [Fonts object](spanish/objects/fonts-object.md) |
| images | Permite enlazar todas las imagenes que utiliza la aplicación.             | Ver más   | [Images object](spanish/objects/images-object.md) |
| lang   | Identifica todos los idiomas en los que está disponible la aplicación     | Si        | Array de [Country-Region Locale](https://developer.apple.com/library/content/documentation/MacOSX/Conceptual/BPInternational/LanguageandLocaleIDs/LanguageandLocaleIDs.html) |
| version | Código de versión. Cada vez que se sube una nueva versión a cualquier *market place* ha de incrementar. | Si | [Semantic versioning](http://semver.org/) |
| iconset | Set de iconos utilizado en la aplicación                                 | Si        |   [IconSet object](spanish/objects/iconset-object.md) |
| theme | Nombre del theme activo. Debe ser uno de los incluidos en la sección Themes del objeto de configuración | Si | String |
| spinner | Datos del spinner que se deasea utilizar en la aplicación | Si | [Spinner object](spanish/objects/spinner-object.md)

# Plugin images object

Describe cada una de las imagenes que se publicarán de un plugin dentro del *market place* de KingOfApp. Los formatos recomendados son: jpg, jpeg, png y gif aunque puede usarse cualquier formato que tenga compatibilidad completa con la mayoría de [navegadores](https://en.wikipedia.org/wiki/Comparison_of_web_browsers#Image_format_support).

Los campos que componen este objeto son:

| Campo       | Descripción                                                                | Requerido | Formato       |
| ----------- | -------------------------------------------------------------------------- | --------- | ------------- |
| list        | Imagen principal que aparece de cada plugin en la vista de listado del *market place*. Su tamaño debe ser 404x220px | No        | Image string |
| popover     | Imagen destacada del plugin que aparece al poner el cursor sobre la imagen list. Su tamaño debe ser 404x220px | No        | Image string |
| banner      | Imagen que aparece en la cabecera de la vista de detalle de un plugin. Su tamaño debe ser 404x220px | No        | Image string |
| screenshots | Imagenes que aparecen a modo de ejemplo del resultado final en la vista de detalle de un plugin. Su tamaño es libre | No        | Array de Image string |


Ejemplo:
```json
{
    "list"    : "images/list.png",
    "popover" : "images/popover.png",
    "banner"  : "images/banner.png",
    "screenshots" : [
        "images/screenshot01.png",
        "images/screenshot02.png"
    ]
}
```

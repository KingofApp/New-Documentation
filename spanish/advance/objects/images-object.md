# Images object

Este objeto define las imágenes usadas por el **Builder** en la fase de compilación de imágenes. No son necesarias para hacer pruebas en el entorno local. La única que afecta al **Visualizer** es el `background`.


```json
{
  "icon"       : "image_icon.png",
  "splash"     : "image_spalsh.png",
  "background" : "image_background.png",
  "logo"       : null,
  "banner"     : null,
  "promo"      : null
}
```

## Themes

En el caso de themes, solo será necesario establecer el background dentro del objeto defaultConfig.
```json
{
  "defaultConfig": {
    "background" : "background-image.png"
  }
}
```


### Referencias
Documentación relacionada | Objetos donde se usa
--------------------------|--------------------------
<ul><li>[Temas -> Color de fondo e imagen de fondo](../themes/themes.md#color-de-fondo-e-imagen-de-fondo)</li></ul> | <ul><li>[Config object](https://github.com/KingofApp/New-Documentation/blob/master/spanish/advance/objects/config-object.md)</li></ul>

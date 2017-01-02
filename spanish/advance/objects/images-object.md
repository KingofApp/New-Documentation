# Images object

La mayor parte de las imágenes que describe este objeto no son necesarias para hacer pruebas en entorno local y solo son usadas por el **Builder** en la fase de compilación de las imágenes. La única que afecta realmente al **Visualizer** es el `background`.


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

En el caso de themes, solo será necesario establecer el background dentro de la parte de defaultConfig.
```json
{
  "defaultConfig": {
    "background" : "background-image.png"
  }
}
```


### Referencias
* Ver [Temas -> Color de fondo e imagen de fondo](../themes/themes.md#color-de-fondo-e-imagen-de-fondo)

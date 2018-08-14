# Dependencias cordova en módulos
### Funcionamiento
La lista de dependencias cordova se usara en el momento de compilar la aplicacion para añadir los plugins de cordova al proyecto.

Listado de plugins oficiales de cordova: [https://cordova.apache.org/plugins/](https://cordova.apache.org/plugins/).

Los plugins de cordova se registran en el apartado deps del structure.json, por ejemplo:

```json
"deps": [
  "https://git-wip-us.apache.org/repos/asf/cordova-plugin-inappbrowser.git",
  "cordova-plugin-camera"
],
```
`Soporta tanto enlaces de github como identificador oficial en caso de estar listado en la web de cordova`

### Referencias

Documentación relacionada | Módulos de ejemplo donde se usa
--------------------------|--------------------------
<ul></ul> | <ul><li>[RSS module](https://github.com/KingofApp/koapp-module-rss)</li></ul>

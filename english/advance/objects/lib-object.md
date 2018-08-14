# Lib module

Este objeto define una dependencia utilizada en un módulo o servicio. Ejemplo:

```json
{
    "bower" : {
        "PolymerElements/iron-flex-layout" : "^1.3.0"
    },
    "src" : "http://resources.kingofapp.com/bower_components/iron-flex-layout/iron-flex-layout.html"
}
```


| Clave | Descripción  | Formato |
| ----- | ------------ | ------- |
| bower | Dependecia con formato Bower donde se indica el identificador de la dependencia y su versión o rango de versiones. | [Bower object](https://bower.io/) |
| src   | Ruta local del archivo principal de la dependencia | URL |

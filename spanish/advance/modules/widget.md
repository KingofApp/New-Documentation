# Widgets en modulos

### Administración para modulos

Los modulos pueden registrar widgets en el Builder a modo de administración para añadir una experiencia post-app a los modulos / servicios. El Builder se encargara de pinchar como iFrame esta seccion para los usuarios que tengan el módulo configurado.

Por ejemplo un módulo de noticias podrá declarar este widget en el Builder para que posteriormente los usuarios que lo tengan montado en una aplicación puedan acceder a este area para insertar las noticias.

Los widget de administración se registran en el apartado widget del structure.json, por ejemplo:

```json
"widget": {
  "title": "Admin - Test module",
  "url": "/modules/testmodule/widget/index.html"
},
```

### Autoconfig para Formly

La función autoconfig permite a los desarrolladores de módulos ayudar a los usuarios con la fase de configuración, existe un nuevo elemento para añadir en el config que habilita un iframe donde se le mandan los datos con el [koapp widget communicator](https://github.com/KingofApp/koapp-widget-communicator) y que al final permite modificar y devolver el objecto `data.plugin.scope` con todo configurado.

El nuevo elemento de tipo frame se registra dentro del config del structure.json:
```json
"config": [{
    "type": "frame",
    "templateOptions": {
      "url": "/modules/testmodule/builder/config.html",
      "label": "Iframe config button",
      "buttonText": "Config Service",
      "description": "",
      "width": "",
      "height": ""
    }
  }],
```

### Estructuras.

Es recomendable alojar los archivos del widget dentro del propio módulo. Así, serviremos los archivos desde Kingofapp. De todos modos es posible elegir una direccion url utilizando la propiedad `templateOptions.url` dentro de la estructura de configuración en el structure.json.

Estructura de archivos:
```
koapp-module-testmodule
├── widget
│   │
│   ├── index.html
│   │
│   ├── main.js
│   │
│   └── style.css
│   
├── config.json
│
├── index.html
│
├── controller.js
│
└── ...
```

### Recibiendo datos.
Para recibir los datos del Builder incluir [koapp widget communicator](https://github.com/KingofApp/koapp-widget-communicator) en el html y utilizar el siguiente `snippet`:
```javascript
koappComm.iframe.ready();
koappComm.iframe.onData(function(data){
  if(data._id && data.lang && data.accessToken){
    //Set language to the one used in builder
    $translate.use(data.lang);
    $translate.refresh();
    console.log("Data is: ", data);
  }
});
```

El resultado del Objeto ejemplo:
```json
{
  "data" : {
    "_id": "YYYY",
    "accessToken": "XXXX",
    "lang": "es_ES",
    "name": "App Name",
    "packageName": "com.kingofapp.STRedXXXX",
    "plugin": {
      "_id": "ZZZZ",
      "identifier": "moduleid",
      "name": "Module Name",
      "scope": {
        "variable": "data",
        "variable2": "data2"
      },
      "uniqueId": "module-XYZY",
      ...
    },
    ...
  }
}
```

Key | Description | Default value
----------------|-------------|--------
`data._id` | Identificador de aplicación | ""
`data.accessToken` | Token de acceso para utilizar en peticiones [Iframe requests]("/spanish/advance/objects/iframeRequest-object")| ""
`data.lang` | Idioma utilizado en el builder | ""
`data.name` | Nombre App | ""
`data.packageName` | Nombre único del paquete | ""
`data.plugin` | Configuracion del módulo | {}
`data.plugin._id` | Identificador del módulo | ""
`data.plugin.identifier` | Nombre único del modulo | ""
`data.plugin.name` | Nombre del módulo | ""
`data.plugin.scope` | Variables de configuración del módulo | {}
`data.plugin.uniqueId` | Identificador único de ruta | ""

### Enviando datos al Builder.
Para enviar datos tratados de vuelta al builder (sobretodo para la funcion `autoconfig`):

```javascript
//Send back data object.
koappComm.iframe.sendData(data);
//Signal to close iframe popup in builder.
koappComm.iframe.close();
```

### Referencias

Documentación relacionada | Módulos de ejemplo donde se usa
--------------------------|--------------------------
<ul></ul> | <ul><li>[Autoconfig facebookfeed module](https://github.com/KingofApp/koapp-module-facebookfeed)</li></ul>

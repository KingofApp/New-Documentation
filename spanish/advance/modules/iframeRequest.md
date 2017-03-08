# Utilizando iframeRequest
### Funcionamiento
IframeRequest es un intermediario que tiene KingOfApp para controlar los accesos a datos protegidos por parte de los desarrolladores de módulos o servicios. Ejemplo:

* Tokens de servicio
* Certificados de publicación

## Archivos y configuración


Dentro de un módulo / servicio config.json
```json
{
  ...
  "iframeRequests":{
    "urls":{
      "POST": ["https://externalurl.com/api/notifications", "https://externalurl.com/api/apps"],
      "GET": ["https://externalurl.com/api/notifications", "https://externalurl.com/api/apps"],
      "PUT": ["https://externalurl.com/api/apps"],
      "DEL": ["https://externalurl.com/api/apps"]
    },
    "vars": {
      "allowed": ["app.appleApnsp12", "app.appleApnsp12Pwd", "plugin.Token"],
      "blocked": ["secret","passwords"]
    }
  },
  ...
}
```

Clave | Descripción | Tipo de datos
----------------|-------------|--------
`iframeRequests.urls.POST` | POST url | []
`iframeRequests.urls.GET` | GET url | []
`iframeRequests.urls.PUT` | PUT url | []
`iframeRequests.urls.DEL` | DEL url | []
`vars.allowed` | Variables protegidas del sistema | []
`vars.blocked` | Variables bloqueadas en la respuesta de la API | []

### iFrame Request
Iframe request contiene las `urls` de las peticiones autorizadas por el widget de un módulo o servicio. Cualquier otra petición que se realice no funcionara si no aparece en la lista.

`Blocked vars` son la lista de variables que se interceptan para que no lleguen al usuario. Normalmente son utilizadas cuando se utilizan llamadas a apis de terceros y se quiere ocultar algunos contenidos.

`Allowed vars` prefijo:

Key | Description
----------------|-------------
`app` | Varibles del sistema (Pregunta al equipo King Of App)
`plugin` | Previamente registradas por el módulo o servicio.

## Ejemplos

Servicio principal koaApiCall:

```javascript
angular
  .module('koa.api.service', [])
  .service('koaApiCall', koaApiCall);

koaApiCall.$inject = ['$http', '$location'];

function koaApiCall($http, $location) {
  var urlBase = "";

  if ($location.absUrl().indexOf('dev.resources.kingofapp.com') !== -1) {
    urlBase = 'http://dev.api.kingofapp.com/iframe/request';
  } else {
    urlBase = 'http://api.kingofapp.com/iframe/request';
  }

  var headers = {
    'x-access-token': 'X',
    'content-type': 'application/json'
  };

  this.setHeaders = function (sessionToken) {
    headers['x-access-token'] = sessionToken;
  }

  this.callApi = function (data) {
      return $http.post(urlBase, data, { 'headers': headers});
  };

}
```

### Uso del servicio KoaApiCall

Asumimos que los datos ya se han sacado previamente como explican [aqui](https://github.com/KingofApp/New-Documentation/blob/master/spanish/advance/modules/widget.md) . Estos datos son pasados a la funcion config.

```javascript
var request = {};
var data = {};
function config(received) {
    data = received;
    //King Of App builder user session token
    koaApiCall.setHeaders(data.accessToken);
    request = {
      'appId': data._id,
      'moduleId': data.plugin._id,
      'request': {
      }
    };
  }
```

Creando una petición:
```javascript
function createObject() {
  request.request = {
    method : 'PUT',
    json : true,
    uri : 'https://external.com/api/apps/',
    body : {
      type: 'production',
      secret:':app.secret',
      apns_p12_password: data.plugin.scope.variable,
    },
    headers: { 'Authorization': 'Basic :plugin.oneSignalToken' }
  };
  return koaApiCall.callApi(request);
}
```

## Objeto respuesta explicado
```json
{
  "appId": data._id,
  "moduleId": data.plugin._id,
  "request": {
    "method" : "PUT",
    "json" : true,
    "uri" : "https://external.com/api/apps/",
    "body" : {
      "type": "production",
      "secret":":app.secret",
      "apns_p12_password": data.plugin.scope.variable,
    },
    "headers": { "Authorization": "Basic :plugin.oneSignalToken" }
  }
}
```

Clave | Descripción | Valor
----------------|-------------|--------
`appId` | Identificador de la app | ""
`moduleId` | Identificador del módulo, tambien se puede usar el (serviceId) para servicios | ""
`request.method` | PUT, POST, GET, DEL | ""
`request.json` | Tipo de respuesta JSON | true
`request.uri` | Peticion de Url de terceros. (Debera estar listada en `iframeRequests.urls`) | ""
`request.body` | Variables enviadas a la peticion de `request.uri`  | {}
`request.headers` | Cabeceras enviadas a la peticion de `request.uri` | {}


## Registrando variables protegidas.

Para registrar variables debes contactar con el equipo de King Of App.

### Referencias

Documentación relacionada | Módulos de ejemplo donde se usa
--------------------------|--------------------------
<ul><li>[Objeto iframeRequest](../objects/iframeRequest-object.md)</li></ul> |

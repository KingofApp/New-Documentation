# Services object

Describe cada uno de los servicios que están configurados para la aplicación. Cada servicio solo puede estar presente una única vez en la aplicación.

Por ese motivo la estructura de este objecto tiene formato de *objeto de objetos* donde las claves del mismo son los `identifier` de cada uno de los servicios configurados.

Ejemplo:
```json
{
  "googleanalytics" : {"object"},
  "pushnotification": {"object"},
  "moreservices"    : {"object"}
}
```

Los objetos internos tienen el formato [Module object](module-object.md) pese a ser servicios, salvo que en vez de utilizar `files` utilizan `vendor` debido al tipo de inyección.


```json
...
"vendor": {
  "paypal": "services/paypal/services.js",
  "cordovaPaypalService": "services/paypal/paypalCordova.js",
  "paypalSandboxService": "services/paypal/paypalSandbox.service.js",
  "ignore": "js/paypal-mobile-js-helper.js"
},
...
```
La `clave` contendra la parte variable del modulo con la siguiente nomenclatura `king.services.XXXX`. En el primer caso, para un modulo llamado `king.services.paypal` usariamos como clave `paypal`.


El `valor` contendra la url del modulo.


## Referencias

Documentación relacionada | Objetos donde se usa
--------------------------|--------------------------
Servicios | [Link ](https://github.com/KingofApp/New-Documentation/blob/master/spanish/advance/services.md)

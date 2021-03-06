# Módulos como menús

Los menús pueden construirse con Polymer o con Angular.

**Particularidades con Polymer:**
* Controlador específico
* La directiva pasa los elementos del menu a Polymer
* Acceso al ámbito (scope) de la barra de navegación (toolbar) desde la propia vista.

[Ejemplo](https://github.com/KingofApp/koapp-module-polymermenu)

**Particularidades con Angular:**
* Controlador específico
* styles.html específico para trabajar con las variables de color de las plantillas
* Acceso al ámbito (scope) de la barra de navegación (toolbar) desde la propia vista.

[Ejemplo](https://github.com/KingofApp/koapp-module-angularmenu)


:::: @Jovi AMPLIAR LAS DIFERENCIAS Y DEFINIR CUAL ES EL RECOMENDADO (#156668)::::


### Definiendo Rutas

Para definir correctamente una ruta dentro del menú necesitaremos especificar el objeto correctamente dentro del Array que compone *menuItems*.

*bgColor* y *bgImage* definen los detalles del fondo del módulo que se solicita en la ruta (*path*).

- **Requisitos**

Clave | Descripción | Ejemplos
----------------|-------------|--------
`path` | Ruta al módulo.
`bgImage` | Background URL
`bgColor` | Color Hexadecimal (ex: #ECECEC)


- **Ejemplo**
```json
"menuItems": [
  {
    "path": "/menu-abcd/home-abcd",
    "bgImage": "http://i.imgur.com/X2KTVXE.jpg",
    "bgColor": ""
  },
  {
    "path": "/menu-abcd/map-abcd",
    "bgImage": "",
    "bgColor": "#ECECEC"
  }
]
```


**Interacción con el usuario**

Puedes configurar el menú para que el usuario final puede seleccionar los detalles del background desde los ajustes del módulo en el Builder.

- [Más información](interaction.md#ejemplo)


#### Funcionalidad (Go Back)

Para mejorar la experiencia de usuario se ha creado una funcionalidad que nos permite volver al módulo previo. Creando así un menú dinámico que mejorar la usabilidad.

Recomendamos encarecidamente incluir esta funcionalidad en los menús que tengan barra de navegación (toolbar).

- Necesitamos incluir el siguiente código en nuestro controlador:
```javascript
  $scope.showBack = false;

  if(structureService.getMenuItems().indexOf($location.$$path) === -1 && $rootScope.current != 'topmenu'){
    $scope.showBack = true;
  }
  $scope.goBack = function() {
    var tempUrl = angular.copy($rootScope.backUrl);
    if (tempUrl.length - 2 > -1) {
      $rootScope.backUrl.pop();
      $location.path(tempUrl[tempUrl.length - 2]);
    }
  };
```

- En la vista de la barra de navegación (toolbar):
```html
  <koa-toolbar>
    <koa-icon-button icon="{{topmenu.icon}}" ng-if="!showBack" ng-click="showBoxMenu()"></koa-icon-button>
    <koa-icon-button icon="arrow-back" ng-click="goBack()" ng-if="showBack"></koa-icon-button>
    <img id="logo" ng-src="{{topmenu.modulescope.toolbarLogo}}" ng-if="topmenu.modulescope.toolbarLogo">
    <span class="title" ng-if="topmenu.modulescope.toolbarTitle">{{toolbar.title}}</span>
  </koa-toolbar>
```

#### Referencias

Documentación relacionada | Lista de menús
--------------------------|--------------------------
<ul></ul> | <ul><li>[koapp-module-polymermenu](https://github.com/KingofApp/koapp-module-polymermenu)</li><li>[koapp-module-fullmenu](https://github.com/KingofApp/koapp-module-fullmenu)</li><li>[koapp-module-topmenu](https://github.com/KingofApp/koapp-module-topmenu)</li><li>[koapp-module-boxmenu](https://github.com/KingofApp/koapp-module-boxmenu)</li><li>[koapp-module-bottommenu](https://github.com/KingofApp/koapp-module-bottommenu)</li><li>[koapp-module-angularmenu](https://github.com/KingofApp/koapp-module-angularmenu)</li></ul>

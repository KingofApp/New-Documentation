# Módulos contenedor

Los módulos contenedor son módulos que tienen un espacio habilitado para contener a otros módulos dentro de ellos mismos.

Utilizan la misma estructura que los modulos regulares, con la particularidad de la opción `canContain` habilitada en el structure.json:
```json
"canContain": true,
```

En cuanto a la vista del html:
```html
<div ng-controller="containermoduleCtrl" class="module containermodule">
  <!-- Module html can be coded here -->

  <!-- Specific div for container modules -->
  <div ng-include="containermoduleTemplate">
    <!-- Do not code anything here, adopted modules will use this space -->
  </div>

</div>
```


### Referencias

`Todos los módulos menu son modulos contenedores`

[Módulos menu](menus.md)

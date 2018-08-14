# Soporte a JSDoc3

:::::::: DESCRIPCIÓN (@Ulises) :::::::::

:::::::: CAPTURA (@Ulises):::::::::::

```javascript
(function() {
  'use strict';

  angular
    .module('nuevaVersion', [])
    .controller('nuevaVersionController', loadFunction);

  loadFunction.$inject = ['$scope', 'structureService', '$location'];
  /**
    * Function that loads the module
    * @function
    * @name loadFunction
    * @since  0.0.1
    * @Author Ulises Gascón
    * @example
    *   function loadFunction($scope, structureService, $location) {
    *   structureService.registerModule($location, $scope, 'nuevaVersion');
    *   console.info("Hi! from nuevaVersionController");
    * }
    * @param  {service} $scope - {@link https://docs.angularjs.org/guide/scope}
    * @param  {object} structureService - {@link http://docs.kingofapp.com/modules/}
    * @param  {service} $location - {@link https://docs.angularjs.org/api/ng/service/$location}
    */
  function loadFunction($scope, structureService, $location) {
    // Register upper level modules
    structureService.registerModule($location, $scope, 'nuevaVersion');
    // --- Start nuevaVersionController content ---
    console.info("Hi! from nuevaVersionController");
    // --- End nuevaVersionController content ---
  }
}());
```

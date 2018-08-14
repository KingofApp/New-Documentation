# Testing con módulos

### End to End (E2E)

Los test End to End nos permiten comprobar la integridad de nuestro módulo, ya que testean los diferentes componenetes que interactuan en la renderización de la vista.

Esta metodología toma como partida la navegación del usuario final y nos permite centrarnos en los errores de comportamiento.

Por defecto en el [generador de módulos](https://www.npmjs.com/package/generator-koapp-module) ya incluimos un test de ejemplo para que realizar este tipo de test no sea un problema cuando desarrollemos nuestros módulos.

Nuestro entorno de testing esta basado en [Karma](https://www.npmjs.com/package/karma), [Mocha](https://www.npmjs.com/package/mocha), [Chai](https://www.npmjs.com/package/chai) y [Protractor](https://www.npmjs.com/package/protractor). Para organizar todo y automatizar las tareas utilizamos [Gulp](https://www.npmjs.com/package/gulp).

Para configurar las especificaciones de Selenium podemos editar el archivo *[protractor.conf.js](tests/protractor.conf.js)*, también podemos modificar, añadir o eliminar pruebas desde *[spec.js](https://github.com/KingofApp/generator-koapp-module/blob/master/generators/app/templates/tests/e2e/spec.js)*.

Podemos facilmente definir los archivos que serán testeados o ignorados desde *[Gulpfile.js](https://github.com/KingofApp/generator-koapp-module/blob/master/generators/app/templates/Gulpfile.js)*.

Cada módulo tendra dentro de su carpeta un archivo `module.e2e.test.js` que contendra los test. Por ejemplo el [módulo helloworld](https://github.com/KingofApp/koapp-module-helloworld):

```javascript
(function(){
	describe('HelloWorld Module test', function() {
		beforeEach(function(){
		    browser.driver.manage().window().setSize(379, 666);
		    browser.ignoreSynchronization = true;
		});

		it('should load helloworld module', function() {
			browser.get('/#/menu-abcd/hello');
			isPresent('.helloworld android-item');

      //Painting and cycles to complete
      browser.sleep(2000);

      expectmodule();

		});
		function isPresent(selector) {
			browser.wait(function() {
					return $(selector).isPresent();
			}, 6000, 'Main (' + selector + ') not present');
		}
		function expectmodule() {
			//Expect text
      var locator = by.css('.helloworld android-item');
      var item = element.all(locator).first();
      expect(item.getText()).toContain('Hello Name');
		}

		afterEach(function() {
			browser.ignoreSynchronization = false;
		});
	});
}());

```

**Lanzar tests**

Para lanzar los test:
```bash
grunt test
```


**Otras configuraciones**

Es posible utilizar un entorno diferente, pero dependerá de cada desarrollador organizar su propio entorno.


**Más Información:**

- [Protractor](http://www.protractortest.org/#/)
- [Protractor Styleguide](https://github.com/CarmenPopoviciu/protractor-styleguide)
- [Selenium Webdriver](https://www.npmjs.com/package/selenium-webdriver)
- [Selenium API](http://seleniumhq.github.io/selenium/docs/api/javascript/)
- [Selenium Docs](http://docs.seleniumhq.org/docs/)


### Unit Testing

::::::: @Jovi Preparar Documentación/Ejemplo de Test unitario. (#156672) :::::::

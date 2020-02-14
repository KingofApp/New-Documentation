## Configuración de prestashop para su uso en King Of App

### Embed:
Embeber contenido web es una forma simple de trasladar directamente el contenido previamente creado en nuestra  página a una aplicación. Con el objetivo de facilitar esta tarea hemos desarrollado en King Of App un módulo de Prestashop que te permitirá crear una plantilla de css personalizada que se aplique solo en tu app. De esta forma podrás ocultar contenido exclusivo de la web y reemplazarlo por el contenido mobile que ofrecen el resto de nuestros módulos. 

#### Instalación del módulo en prestashop:
 1. Descarga [nuestro módulo para Prestashop](https://s3.eu-central-1.amazonaws.com/kingofapp.com/embed+plugins/koaembed_prestashop_plugin.zip).
 2. Accede a la zona de administración de tu instalación de Prestashop. 
 3. En el menú lateral busca la sección "improve/Modules/Module Catalog"
 4. Haz click en el botón install module en la parte superior de la pantalla.
 5. Arrastra el archivo que descargaste en el paso 1 hasta la zona de subida que ha aparecido.

#### Configuración de nuestro módulo en prestashop:

 1. En el menú lateral del administrador de prestashop accede a  "improve/Modules/Module Manager"
 2. Haz scroll hasta el final de la página, en la sección "Otros" verás que aparece el módulo recién instalado.
 3. Presiona el botón Configurar del módulo.
 4. Rellena el campo "Key Word" con la palabra clave que se usará en la app para avisar a prestashop que está en una versión mobile.
 5. Rellena el campo "Add Styles" con tantas [reglas css](https://www.w3schools.com/css/) como consideres.

#### ¿Cómo funciona?
Una vez instalado y configurado adecuadamente, el módulo revisará la url de tu web en busca de la palabra clave que has introducido en el campo "Key Word" durante la configuración. 
Para hacerlo agrega ( ?yourKeyword=true ) al final de la url de tu sitio. Nuestro módulo lo detectará y agregará los estilos que le has especificado durante su configuración. Si has dejado los estilos predeterminados verás que la cabecera y el pie de página de tu sitio han desaparecido. 
No te preocupes, pues ese cambio solo es visible en tu navegador para volver a la normalidad solo tienes que recargar la página agregando         ( ?yourKeyword=false ) al final de la url.

#### ¿Cómo aplico todo esto en mi app?

 1. Accede a nuestro [builder de aplicaciones](http://builder.kingofapp.com/) utilizando tu cuenta, o crea una nueva.
 2. Accede a tu aplicación o crea una nueva utilizando una de nuestras numerosas plantillas.
 3. Haz click en la sección "Módulos" y luego en el botón "Añadir módulo"
 4. Busca "Prestashop Embed" en el buscador y haz click en el botón usar del módulo con el mismo nombre.
 5. Ahora al final de la estructura de tu app, ha aparecido el módulo recién agregado.
 6. Marca el módulo como principal y haz click en el icono  para acceder a la configuración del mismo.
 7. En el campo url, agrega la url de una página de tu sitio agregando ?yourKeyword=true al final.
 8. Haz click en el botón "Guardar" arriba a la derecha.

Ahora en el mobil a la derecha verás aparecer tu web con los estilos que has especificado.

 

###Wordpress Posts Pro
![img](http://resources.kingofapp.com/modules/wppostspro/images/wordpress-post-pro_list.png)

¡Transforma tu Web hecha en Wordpress en una App nativa! Con este módulo descarga el contenido de cualquier página y se convertirá en una aplicación móvil dispuesta para todo el mundo. Necesitarás descargar un plugin e instalarlo en la Web: https://wordpress.org/plugins/json-rest-api/

**Detalles**
- Autor: King of App
- Precio: 19.99€
- Descargas: 7
- Valoración: King of App: 2.5 | Usuarios: 2.5
- Plataformas: android, ios, windows
- Categorías: news, social


# **(How to) Configurar el módulo Wordpress Feed Pro**

Wordpress es, sin lugar a duda, el principal motor de creación de webs del mundo. Por ello, y para facilitar la integración de cualquier página en una App, en King of App hemos creado este módulo, el Wordpress Feed Pro. Aprende aquí a configurarlo.

Lo primero que tienes que hacer es instalar dos plugins en tu página de wordpress:

**KOAPP-CORS**: [https://es.wordpress.org/plugins/koapp-cors/](https://es.wordpress.org/plugins/koapp-cors/)

**Json API**: [https://wordpress.org/plugins/json-api/](https://wordpress.org/plugins/json-api/)

La configuración de ambos es muy sencilla pero requiere prestar un poco de atención.

Por un lado, el KOAPP-CORS solo necesita estar activado.

Para el plugin Json API hay que tener en cuenta varias cuestiones. Por un lado, que todas las opciones estén habilitadas y, por el otro, darle un nombre al campo _API base._ Este último dato es muy importante ya que es el que deberemos introducir en la configuración del módulo en el builder de King of App.

[![FireShot Capture 210 - JSON API Settings ‹ K_ - http___koa.pepocivs.com_wp-admin_options-general.php](http://kingofapp.es/wp-content/uploads/2016/03/FireShot-Capture-210-JSON-API-Settings-‹-K_-http___koa.pepocivs.com_wp-admin_options-general.php_.png)](http://kingofapp.es/wp-content/uploads/2016/03/FireShot-Capture-210-JSON-API-Settings-‹-K_-http___koa.pepocivs.com_wp-admin_options-general.php_.png)

Con esta configuración debidamente cumplimentada en tu página de Wordpress llega el momento de configurar el módulo en King of App.

Como ves, para activar este módulo te pedimos rellenar una serie de campos.

_Domain_: aquí debes introducir el dominio de tu página de wordpress (recuerda que debe ir en el siguiente formato: http://www.tudominio.tudominio)

_API Base_: aquí debes introducir el identificador utilizado en la configuración del plugin Json API (únicamente el campo editado por ti)

_fixedHeadImage_: Este campo sirve para definir una imagen de cabecera, que presidirá el módulo. Copia la url de la imagen que quieras y pégala aquí.

_SelectedFilter_: Aquí debes elegir que filtro se aplicará (categoría...)

_Filter_: Aquí debes, por ejemplo en el caso de que el filtro sea por categoría, decirnos el nombre de la categoría.

_FirstPost_: Aquí debes entrar el ID del post que quieres que se presente en primera posición, que abra el contenido del módulo. Lo encontrarás en la URL del post.

_Visualización_: puede elegir cómo se presenta la información.

El resto de opciones, que se acompañan de un checkbox, son para que decidas si quieres mostrar el autor, la fecha de publicación, los comentarios, la descripción o la imagen de cada uno de los posts.

Con todo, debidamente configurado, tu módulo **Wordpress Feed Pro** ya estará listo y activado.
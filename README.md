# King of App - Documentación y herramientas

![logo_doc](http://kingofapp.es/wp-content/uploads/2013/03/reino.jpg)

## Importante

Este repositorio **debe permanecer privado**, ya que engloba la documentación externa (para clientes y comunidad) e interna (solo para nosotros).

### Contribuir

La documentación es necesaria para mejorar la manera en la que trabajamos con la plataforma. Si quieres hacer cambios, ¡hazlos!... pero si no estas seguro de como hacerlo siempre puedes abrir un issue o hablar con Ulises.

Esta documentación se utilizará también para alimentar [nuestra documentación online](http://docs.kingofapp.com)

Para poder gestionar mejor el proceso de documentación, existen dos tablas que muestran los trabajos actuales. [Traducciones](#traducciones) y [contenidos](#contenidos) en los campos de la tabla podemos encontrar [emojis](http://www.webpagefx.com/tools/emoji-cheat-sheet/) que nos representan el estado actual de cada tema. En algunos casos podemos encontrar información adicional.

### Leyenda

**Estados**
- :question: - Desconocido
- :bangbang: - Desactualizado
- :skull: - Depreciado
- :white_check_mark: - Listo/Nada pendiente
- :x: - Pendiente/No realizado
- :no_entry: - Parado

**Marcadores**
- :fire: - Bugs críticos prioritarios por resolver
- :sunrise: - Faltan imágenes/gráficos
- :rocket: - Pendiente de subir a docs.kingofapp...
- :neckbeard: - Falta por desarrollar código (herramienta/demo/script...)
- :large_orange_diamond: - Depende de módulos que no están listos
- :lock: - **Privado, no publicar**

**Asignaciones**
- :flashlight: @persona - Pendiente de completar por una persona
- :warning: @persona - En revisión por una persona del equipo
- :construction: @persona - Realizando cambios por alguien del equipo...


### Contenidos

Tema | Estado
------------ | -------------
**[Getting Started](spanish/getting_started/readme.md)** | :x:
— [Introducción](spanish/getting_started/intro.md) | :x:
— [Filosofía](spanish/getting_started/philosophy.md) | :x:
— [Builder](spanish/getting_started/builder/readme.md) | :white_check_mark:
—— [Tu primera App](spanish/getting_started/builder/first_app.md) | :x:
—— [Plantillas](spanish/getting_started/builder/templates.md) | :white_check_mark:
—— [Administración](spanish/getting_started/builder/administration.md) | :white_check_mark:
—— [Funcionalidad](spanish/getting_started/builder/functionality/readme.md) | :white_check_mark:
——— [Módulos](spanish/getting_started/builder/functionality/modules/readme.md) | :white_check_mark:
———— [Módulos Avanzado](spanish/getting_started/builder/functionality/modules/advance_modules.md) | :white_check_mark:
———— [Listado de Módulos](spanish/getting_started/builder/functionality/modules/modules_list.md) | :lock: :white_check_mark:
——— [Servicios](spanish/getting_started/builder/functionality/services/readme.md) | :white_check_mark:
———— [Listado de Servicios](spanish/getting_started/builder/functionality/services/services_list.md) | :lock: :white_check_mark:
—— [Apariencia](spanish/getting_started/builder/look_and_feel/readme.md) | :white_check_mark:
——— [Listado de Temas](spanish/getting_started/builder/look_and_feel/themes_list.md) | :lock:  :white_check_mark:
—— [Publica tu App](spanish/getting_started/builder/publication/readme.md) | :white_check_mark:
**[Advance](spanish/advance/readme.md)** | :x:
— [Introducción](spanish/advance/intro.md) | :x:
— [¡Ponte al dia!](spanish/advance/catch_up.md) | :construction: @Ulises
— [Visualizer](spanish/advance/visualizer/readme.md) | :white_check_mark:
—— [Instalación en local](spanish/advance/visualizer/local_installation.md) | :white_check_mark:
—— [Instalación en c9](spanish/advance/visualizer/c9_installation.md) | :neckbeard: :construction: @Ulises
— [Spinners](spanish/advance/spinners/readme.md) | :white_check_mark:
—— [Ejemplo Sencillo](spanish/advance/spinners/example.md) | :white_check_mark:
—— [Ejemplo Avanzado](spanish/advance/spinners/advance_example.md) | :white_check_mark:
— [Temas](spanish/advance/themes.md) | :x:
— [Módulos](spanish/advance/modules/readme.md) | :large_orange_diamond: :construction: @Ulises
—— [Interacción con el usuario](spanish/advance/modules/interaction.md) | :flashlight: @Pepo
—— [Funcionalidades de los módulos](spanish/advance/modules/features.md) | :x:
—— [Menus](spanish/advance/modules/menus.md) | :flashlight: @Jovi
—— [Testing](spanish/advance/modules/testing.md) | :flashlight: @Jovi
—— [Ejemplo Sencillo](spanish/advance/modules/example.md) | :x:
—— [Ejemplo Avanzado](spanish/advance/modules/advance_example.md) | :x:
— [Services](spanish/advance/services.md) | :large_orange_diamond: :neckbeard:
— [API](spanish/advance/api.md) | :lock: :x:
**[Comunidad](spanish/community/readme.md)** | :x:
— [Eventos](spanish/community/events.md) | :x:
— [Como contribuir](spanish/community/contribution.md) | :x:
— [Mejores prácticas](spanish/community/best_practices.md) | :x:
— [Guías de estilos](spanish/community/style_guide.md) | :x:
— [F.A.Q](spanish/community/faq.md) | :x:
**[Logros](spanish/achievements/readme.md)** | :x:
— [Lista de Apps publicadas](spanish/achievements/apps_list.md) | :x:
— [Historias de clientes](spanish/achievements/clients.md) | :x:
— [Lista de Módulos](spanish/achievements/modules_list.md) | :x:
— [Lista de Servicios](spanish/achievements/services_list.md) | :x:
— [Lista de Temas](spanish/achievements/themes_list.md) | :x:


### Traducciones

Una vez terminado el contenido principal... empezaremos con las traducciones.

### Herramientas

**Generator-koapp-module**

Paquete de NPM que nos permite generar la estructura completa de un módulo.
- [en NPM](https://www.npmjs.com/package/generator-koapp-module)
- [en GitHub](https://github.com/kingofapp/generator-koapp-module)


**Generator-koapp-spinner**

Paquete de NPM que nos permite generar la estructura completa de un spinner.
- [en NPM](https://www.npmjs.com/package/generator-koapp-spinner)
- [en GitHub](https://github.com/kingofapp/generator-koapp-spinner)


**:lock: Petición de Tokens a la API**

Script para Node que nos permite hacer llamadas a la API gestionando los tokens en cada llamada, funciona como un paquete (require).
- [en Resources](https://github.com/KingofApp/com.kingofapp.resources/blob/dev/scripts/peticion_token.js)


**:lock: Modules list**

Script de Node que descarga toda la información de los módulos en una estructura de archivos markdown, idéntico a la documentación.
- [en Español](https://github.com/KingofApp/com.kingofapp.resources/blob/dev/scripts/modules_list_es-ES.js)
- [en Inglés](https://github.com/KingofApp/com.kingofapp.resources/blob/dev/scripts/modules_list_en-US.js)


**:lock: Services list**

Script de Node que descarga toda la información de los Servicios en una estructura de archivos markdown, idéntico a la documentación.
- [en Español](https://github.com/KingofApp/com.kingofapp.resources/blob/dev/scripts/services_list_es-ES.js)
- [en Inglés](https://github.com/KingofApp/com.kingofapp.resources/blob/dev/scripts/services_list_en-US.js)


**:lock: Themes list**

Script de Node que descarga toda la información de los Themes en una estructura de archivos markdown, idéntico a la documentación.
- [en Español](https://github.com/KingofApp/com.kingofapp.resources/blob/dev/scripts/themes_list_es-ES.js)
- [en Inglés](https://github.com/KingofApp/com.kingofapp.resources/blob/dev/scripts/themes_list_en-US.js)


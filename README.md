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
- :ok_hand: - Listo/Nada pendiente
- :x: - Pendiente/No realizado
- :no_entry: - Parado

**Marcadores**
- :fire: - Bugs críticos prioritarios por resolver
- :sunrise: - Faltan imágenes/gráficos
- :rocket: - Pendiente de subir a docs.kingofapp...
- :lock: - **Privado, no publicar**

**Asignaciones**
- :warning: @persona - En revisión por una persona del equipo
- :construction: @persona - Realizando cambios por alguien del equipo...


### Contenidos

Tema | Estado
------------ | -------------
**[Getting Started](spanish/getting_started/readme.md)** | :x:
— [Introducción](spanish/getting_started/intro.md) | :x:
— [Filosofía](spanish/getting_started/philosophy.md) | :x:
— [Builder](spanish/getting_started/builder/readme.md) | :ok_hand:
—— [Tu primera App](spanish/getting_started/builder/first_app.md) | :x:
—— [Plantillas](spanish/getting_started/builder/templates.md) | :ok_hand:
—— [Administración](spanish/getting_started/builder/administration.md) | :ok_hand:
—— [Funcionalidad](spanish/getting_started/builder/functionality/readme.md) | :ok_hand:
——— [Módulos](spanish/getting_started/builder/functionality/modules/readme.md) | :ok_hand:
———— [Módulos Avanzado](spanish/getting_started/builder/functionality/modules/advance_modules.md) | :ok_hand:
———— [Listado de Módulos](spanish/getting_started/builder/functionality/modules/modules_list.md) | :lock: :ok_hand:
——— [Servicios](spanish/getting_started/builder/functionality/services/readme.md) | :ok_hand:
———— [Listado de Servicios](spanish/getting_started/builder/functionality/services/services_list.md) | :lock: :ok_hand:
—— [Apariencia](spanish/getting_started/builder/look_and_feel/readme.md) | :x:
——— [Listado de Temas](spanish/getting_started/builder/look_and_feel/themes_list.md) | :lock:  :ok_hand:
—— [Publica tu App](spanish/getting_started/builder/publication/readme.md) | :ok_hand:
**[Advance](spanish/advance/readme.md)** | :x:
— [Introducción](spanish/advance/intro.md) | :x:
— [¡Ponte al dia!](spanish/advance/catch_up.md) | :x:
— [Visualizer](spanish/advance/visualizer.md) | :x:
— [Spinners](spanish/advance/spinners.md) | :x:
— [Temas](spanish/advance/themes.md) | :x:
— [Módulos](spanish/advance/modules.md) | :x:
— [Services](spanish/advance/services.md) | :x:
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


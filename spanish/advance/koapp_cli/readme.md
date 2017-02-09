# Koapp CLI

Para facilitar el desarrollo de Apps con nuestra plataforma, hemos desarrollado nuestra propia interfaz de línea de comandos.

## Instalación

```bash
$ npm install -g koapp-cli
```

### Requisitos
- [ImageMagick](https://www.imagemagick.org/script/download.php#macosx)
- [npm](https://docs.npmjs.com/getting-started/installing-node)

Una vez que lo tengas, ejecuta los siguientes comandos desde consola:

```bash
$ npm install -g cordova
$ npm install -g yo
$ npm install -g generator-koapp-module
$ npm install -g generator-koapp-theme
$ npm install -g generator-koapp-spinner
$ npm install -g cordova-icon
$ npm install -g cordova-splash
```

Si tienes problemas de permisos a la hora de instalar con npm, echale un ojo a la guía de npm para [arreglar los permisos](https://docs.npmjs.com/getting-started/fixing-npm-permissions).

## Uso

### Crear un proyecto

Abre tu consola favorita en el directorio en el que quieras crear tu proyecto, ejecuta el siguiente comando:

```bash
koapp init <projectName>
```

Con este comando, Koapp CLI generará una carpeta contenedora en la que podrás encontrar una copia de nuestro [Visualizer]('../visualizer/readme.md') con la que podrás trabajar.

### Crear un módulo, tema o spinner

Entra en el directorio ``com.kingofapp.visualizer/www`` de tu proyecto. Una vez hecho esto, accede a la carpeta correspondiente (``modules``, ``themes`` o ``spinners``) y ejecuta el siguiente comando:

```bash
koapp create <module|spinner|theme>
```

Esto lanzará un asistente que nos pedirá los datos necesarios para que [Yeoman](http://yeoman.io/) genere la estructura de archivos y contenido necesarios para comenzar a desarrollar nuestro módulo.

Una vez se haya generado todo, conviene integrarlo en nuestra aplicación.

### Añadir un módulo, tema o spinner

Si por el contrario, queremos añadir un módulo, tema o spinner ya existente, podemos utilizar la koapp-cli para descargar e instalar el plugin que deseemos

```bash
koapp add <module|spinner|theme> <pluginName> [moduleName]
```

Este comando se encargará de descargar el paquete de npm y de integrarlo en el structure.json de tu aplicación. En el caso de los módulos un asistente nos dará a elegir los posibles menús donde podremos colocar nuestro módulo. El parámetro moduleName es opcional y sirve para que indicar un nombre para el módulo dentro de la aplicación,

### Servir nuestra aplicación

Una vez que hayamos creado y configurado nuestra aplicación, podremos previsualizar el resultado en nuestro navegador. Para ello debemos entrar en la raíz del visualizer de nuestro proyecto y ejecutar el comando

```bash
koapp serve
```

Este comando lanzará el visualizer en nuestro navegador y nos permitirá ver los progresos en el desarrollo de nuestra aplicación.

### Construir nuestra aplicación

Crea y construye el proyecto Córdova con el nombre indicado con todas sus dependencias para la plataforma introducida para poder probar tu aplicación.

```bash
koapp build <cordovaProject> <platform>
```
Para poder construir tu aplicación necesitas tener instalado el [SDK de Android](https://developer.android.com/studio/index.html?hl=es-419) y/o [XCode](https://developer.apple.com/xcode/).

### Help

Si necesitamos saber las opciones que nos ofrece Koapp CLI podemos servirnos del comando ``help`` para consultar una pequeña ayuda de un comando concreto o simplemente consultar la lista de comandos disponibles

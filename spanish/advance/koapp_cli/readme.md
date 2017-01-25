# Koapp CLI

Para facilitar el desarrollo de Apps con nuestra plataforma, hemos desarrollado nuestra propia interfaz de línea de comandos.

## Instalación

Primero, necesitarás tener instalado el gestor de paquetes [npm](https://www.npmjs.com/). Una vez que lo tengas, ejecuta los siguientes comandos desde consola:

```bash
#dependencias
npm install -g cordova
npm install -g yo
npm install -g generator-koapp-module
npm install -g generator-koapp-theme
npm install -g generator-koapp-spinner
#koapp-cli
npm install -g koapp-cli
```

Si tienes problemas de permisos a la hora de instalar con npm, echale un ojo a la guía de npm para [arreglar los permisos](https://docs.npmjs.com/getting-started/fixing-npm-permissions).

## Uso

### Crear un proyecto

Abre tu consola favorita en el directorio en el que quieras crear tu proyecto, ejecuta el siguiente comando:

```bash
koapp init <projectName>
```

Con este comando, Koapp CLI generará una carpeta contenedora en la que podrás encontrar una copia de nuestro [Visualizer]('../visualizer/readme.md') con la que podrás trabajar así como una carpeta con el proyecto Cordova ya creado con la que podrás construir tu aplicación.

### Crear un módulo, tema o spinner

Una vez que hayas creado, entra en el directorio ``com.kingofapp.visualizer/www`` de tu proyecto. Una vez hecho esto, accede a la carpeta correspondiente (``modules``, ``themes`` o ``spinners``) y ejecuta el siguiente comando:

```bash
koapp create module
```

Esto lanzará un asistente que nos pedirá los datos necesarios para que [Yeoman](http://yeoman.io/) genere la estructura de archivos y contenido necesarios para comenzar a desarrollar nuestro módulo.

Una vez se haya generado todo, conviene integrarlo en nuestra aplicación.

### Añadir un módulo, tema o spinner

Si por el contrario, queremos añadir un módulo, tema o spinner ya existente, podemos utilizar la koapp-cli para descargar e instalar el plugin que deseemos

```bash
koapp add <module|spinner|theme> <pluginName>
```

Este comando se encargará de descargar el paquete de npm y de integrarlo en el structure.json de tu aplicación. En el caso de los módulos un asistente nos dará a elegir los posibles menús donde podremos colocar nuestro módulo.

### Servir nuestra aplicación

Una vez que hayamos creado y configurado nuestra aplicación, podremos previsualizar el resultado en nuestro navegador. Para ello debemos entrar en la raíz del visualizer de nuestro proyecto y ejecutar el comando

```bash
koapp serve
```

Este comando lanzará el visualizer en nuestro navegador y nos permitirá ver los progresos en el desarrollo de nuestra aplicación.

### Help

Si necesitamos saber las opciones que nos ofrece Koapp CLI podemos servirnos del comando ``help`` para consultar una pequeña ayuda de un comando concreto o simplemente consultar la lista de comandos disponibles

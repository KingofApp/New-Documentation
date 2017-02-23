
# Instalación de Visualizer en el entorno local

Estas instrucciones son validas para Windows, Mac y Linux

### Pasos Previos

- Necesitaras instalar [Node.js](https://nodejs.org/en/) y [Npm](https://www.npmjs.com/)
  - [Instrucciones generales](https://nodejs.org/en/download/)
  - [Instrucciones especificas solo para Mac (usando Homebrew)](http://blog.teamtreehouse.com/install-node-js-npm-mac)

### Instalación global de Paquetes
- Paquetes:
    - [Bower](https://bower.io/)
    - [Gulp](http://gulpjs.com/)
    - [Grunt](http://gruntjs.com/)
    - [Yeoman](http://yeoman.io/)

- Ejecutar en la terminal (se requieren permisos de superusuario)
```bash
npm install -g bower && npm install -g gulp && npm install -g grunt && npm install -g yo && yo doctor
```

- Resultado esperado
```bash
Yeoman Doctor
Running sanity checks on your system

✔ Global configuration file is valid
✔ NODE_PATH matches the npm root
✔ Node.js version
✔ No .bowerrc file in home directory
✔ No .yo-rc.json file in home directory
✔ npm version

Everything looks all right!
```


### Descarga e instalación de Koapp Visualizer

- Ejecutar en la terminal

  ```bash
  git clone -b dev https://git@github.com/KingofApp/com.kingofapp.visualizer.git && cd com.kingofapp.visualizer
  ```


### Arrancar el Visualizer
- Ejecutar en la terminal

  ```bash
  npm start
  ```
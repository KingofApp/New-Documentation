# Instalación de Visualizer en C9.io

Cloud9 nos permite trabajar directamente en la nube. Para ello... c9 nos ofrece maquinas virtuales basadas en Ubuntu.

Tenemos varias opciones disponibles para instalarlos Visualizer en un workspace de c9.

- [Instalación automática](#instalaci%C3%B3n-autom%C3%A1tica)

Partiendo de un script de Bash instalaremos cómodamente todo lo necesario. Este script realiza de manera automática los pasos de la instalación manual.

- [Clonación de un workspace](#clonaci%C3%B3n-de-un-workspace)

Es la solución más sencilla, podemos clonar un workspace que ya tiene todo instalado.

- [Instalación manual](#instalaci%C3%B3n-manual)

Es la solución más lenta pero nos permite alterar el proceso de instalación. Este método también esta recomendado en caso de encontrar problemas con las otras alternativas. 


### Instalación automática
  **Próximamente (script sh)**

### Clonación de un workspace
  **Próximamente**

### Instalación manual

**Verificamos las versiones de [Node.js](https://nodejs.org/en/) y [Npm](https://www.npmjs.com/)**
- Ejecutar en la terminal
  ```
    node --version && npm --version
  ```

- Esperado (pueden variar las versiones):
  ```
    v4.5.0
    2.15.9
  ```

**Arreglamos el problema con [sudo](https://c9.io/blog/how-to-use-yeoman-on-cloud9/).**

- Verificar que utilizamos la ruta de nuestra versión de Node.js y ejecutamos en la terminal

  ```
    echo "export NODE_PATH=$NODE_PATH:/home/ubuntu/.nvm/versions/node/v4.5.0/lib/node_modules" >> ~/.bashrc && source ~/.bashrc
  ```


**Actualizamos Npm e instalamos la dependencias globales ([Gulp](http://gulpjs.com/), [Grunt](http://gruntjs.com/), [Bower](https://bower.io/), [Yeoman](http://yeoman.io/))**
  ```
    npm update -g npm && npm install -g gulp && npm install -g grunt && npm install -g bower && npm install -g yo && yo doctor
  ```

  - Resultado esperado:
  ```
    Yeoman Doctor
    Running sanity checks on your system

    ✔ Global configuration file is valid
    ✔ Node.js version
    ✔ No .bowerrc file in home directory
    ✔ No .yo-rc.json file in home directory
    ✔ npm version
    ✔ NODE_PATH matches the npm root
  ```

  **Descarga e instalación de King Of App Visualizer**

  - Ejecutar en la terminal

    ```
    git clone -b dev https://git@github.com/KingofApp/com.kingofapp.visualizer.git && cd com.kingofapp.visualizer
    ```

  **Ajustar Visualizer al entorno de C9.io (puertos)**

  - Sustituir *Grunfile.js* con los datos de *[este archivo](https://gist.github.com/UlisesGascon/54acff02948964554726708f04a25937#file-gruntfile-js)*
  - Sustituir *gulp-tasks/serve.js* con los datos de *[este archivo](https://gist.github.com/UlisesGascon/54acff02948964554726708f04a25937#file-serve-js)*
    - Ejecutar en la terminal
  ```
    npm start
  ```
  - Abre una nueva pestaña con esta URL: `https://<workspacename>-<username>.c9users.io`



## Pasos para insertar tu web en King of App:

- Cambia el valor de la cabecera **x-frame-options de tu servidor**  por **ALLOWALL**. Esto habilita tu sitio para ser insertado en una etiqueta *iframe* de HTML.

- Inserta el código a continuación en la cabecera de todas las páginas de tu sitio.

- No olvides reemplazar las variables **keyWord** y **css** por tu palabra clave y el css respectivamente.

```
<script>

var  keyWord = "kingOfApp"; //query string to find in the url

var  css = `header, footer{ display:none}`; //style to add if keyWord is true

  

const  urlParams = new  URLSearchParams(window.location.search);

const  myParam = urlParams.get(keyWord);

if(myParam){

localStorage.setItem(keyWord, myParam);

}

if(localStorage.getItem(keyWord) && localStorage.getItem(keyWord) === "true"){

addStyle();

}

function  addStyle(){

var  head = document.head || document.getElementsByTagName('head')[0];

var  style = document.createElement('style');

  

head.appendChild(style);

  

style.type = 'text/css';

if (style.styleSheet){

// This is required for IE8 and below.

style.styleSheet.cssText = css;

} else {

style.appendChild(document.createTextNode(css));

}

}

</script>

<script  type="text/javascript"  src="https://cdnjs.cloudflare.com/ajax/libs/iframe-resizer/4.2.9/iframeResizer.contentWindow.min.js"></script>
```
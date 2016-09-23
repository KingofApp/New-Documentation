###Puship Notifications
![img](http://resources.kingofapp.com/services/puship/images/list.png)

Permite enviar notificaciones push mediante Puship.

**Detalles**
- Autor: King of App
- Precio: 10€
- Descargas: 18
- Valoración: King of App: 3 | Usuarios: 5
- Plataformas: android, ios, windows
- Categorías: push


# **(How to) Configurar el servicio de mensajería push**

****

La **mensajería push** es, sin lugar a duda, la gran virtud de las aplicaciones móviles. Por ello, en King of App hemos querido dar opción de contar con varios **proveedores** de este servicio. Para este módulo, hemos confiado en **Push IP** para que gestiones la comunicación con los usuarios de tus Apps.

Para configurar este módulo es necesario que crees una **cuenta de usuario** en puship.com. En el apastado “_My Apps_” del panel de gestión daremos de alta la aplicación sobre la que se instalará el sistema de mensajería [Como crear una aplicacion PushIp](https://www.puship.com/es/documentacion/server). Al crearla, el propio servicio nos ofrecerá un identificador de la App. Este código es el primero que debemos copiar en el campo “_push App id_” de nuestra configuración.

El segundo código de acceso que pedimos es el “_Google Cloud Messaging Token_”. Este se consigue teniendo una cuenta de gmail y accediendo a la **consola de gestion de Google Cloud**: https://console.cloud.google.com/

Será en este panel de control donde deberemos activar la **API** correspondiente al servicio “_Cloud Messaging_” [Como obtener las claves para GoogleCloudMessaging](https://www.youtube.com/watch?v=kdvqJTLgq6M). Al hacerlo, Goole te dará un código. Este el que debes pegar en el segundo campo de nuestra configuración.

A partir de ahí, ya está todo listo para que puedas lanzar mensajes push a los usuarios de tu App.

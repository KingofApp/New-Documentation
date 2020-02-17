# Como importar una app externa en King of App

## Requisitos Android:

Con el fin de proteger a los usuarios y a los desarrolladores, google requiere que todas las apps que pretendan subirse a su plataforma, estén protegidas por una firma digital. Este proceso se realiza mediante un archivo único que se agrega al apk de tu aplicación y es registrado por google durante la subida de la app. 
En King of App todo ese proceso se realiza de forma automatica, sin embargo para aplicaciones que no se hallan creado en nuestra plataforma, es necesario solicitar una serie de datos adicionales para una correcta configuración y posterior subida al Market de Google play.
Los siguientes puntos constituyen una lista de la información que deberá proporcionarnos:

 - El archivo de firma con el que se publica la app de forma habitual:
	 - El archivo debe tener el mismo nombre con que fue creado.
	 - El archivo debe tener extensión **.jks**
 - Durante la creación de una de estas claves, se solicitan una serie de datos para vincularla de forma segura a un usuario y cuenta de google. 
	 #### Obligatorios:
	 - Contraseña del archivo.
	 - Alias que le ha dado a su clave.
	 - Contraseña del alias de su clave.
	 - Años de validez de la clave ( Debe ser mayor que 20).
	#### Opcionales:
	 -  Nombre completo que se utilizó para rellenar la clave.
	 - Tipo de organización con la que se firmó su clave.
	 - Nombre de su organización.
	 - La localidad de su organización.
	 - Provincia o estado de su organización.
	 - Código del país de su organización ( ES -> España, EU -> Estados Unidos, etc )
 ![Google play create key](https://s3-us-west-2.amazonaws.com/images.docs.kingofapp.com/buildSystem+/google_play_create_key.png)

## Requisitos iOS:

Las aplicaciones de apple se firman de forma distinta, vinculándolas a un equipo concreto y a una cuenta de usuario especifica. Para la publicación de apps en iOS con nosotros solo debe proporcionar los datos de acceso a su cuenta y estar pendiente de los códigos de doble verificación que recibirá durante las publicaciones.
Si ya tiene una app publicada en su cuenta de iTunnes Connect y desea publicarla con nosotros, deberá cumplir los siguientes requisitos:

- Su cuenta debe tener configurada la verificación de dos factores (6 dígitos )
- Apple solo acepta la creación de tres certificados de **distribución** por cada una de sus cuentas. Nuestro sistema requiere la utilización de uno de ellos para su correcto funcionamiento. Por eso es imprescindible que se asegure de no tener tres certificados en uso cuando compila una app con nosotros. Puede consultar sus certificados accediendo a su cuenta de apple developers y haciendo click en este link: [https://developer.apple.com/account/resources/certificates/list](https://developer.apple.com/account/resources/certificates/list)
- Apple proporciona un código que autoriza el acceso de aplicaciones externas para la utilización de algunos de sus servicios como la subida de apps a Test Fligth. Sin ese código nos resulta imposible subir su aplicación a su cuenta de iTunnes Connect. Puedes encontrar información al respecto en el siguiente enlace: [https://support.apple.com/es-es/HT204397](https://support.apple.com/es-es/HT204397)
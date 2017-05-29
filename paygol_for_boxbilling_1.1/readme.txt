******* English *******

Paygol module v1.1 for BoxBilling  

About this module:
- This module allows you to easily integrate Paygol on your platform. Paygol is an online payment gateway that offers a 
  wide array of both worldwide and local payment methods such as credit and debit card, paysafecard, bank transfers, cash payments, 
  SMS/call and more. More payment options and wider coverage means that paying for your products and services will be easier than ever 
  for your customers, which can lead to an increase in sales.

Requirements:
- Working BoxBilling installation (tested with version 4.20).
- Paygol account.
- Standard, "Integrated" type Paygol service.

Installation:
- Unzip paygol_for_boxbilling_1.0.zip directly into your Boxbilling folder.
- To install the module, go to your BoxBilling administration panel (Configuration -> Payment Gateways), select Paygol at the "New payment gateways" tab, then click "Install".
- Once installed, proceed to the module's configuration page (Configuration -> Payment Gateways), select Paygol and click "Edit".
- Enter the ID of your Paygol service (you can find this ID at the "My Services" section of your Dashboard, at Paygol's website).
- Enter the Secret key of your Paygol service (you can find this secret key at the "My Services" section of your Dashboard, at Paygol's website).
- Make sure that the module is configured as follows:
	- "Enabled: Yes".
	- "Allow one time payments: Yes".
	- "Enable test mode: No". (please check the "Testing" section of this document for information on how to test your service).
- Copy the "IPN Callback URL" exactly as shown and paste it into the "Process URL (IPN)" field of the configuration of your service, accessible through
  the "My Services" section of your Dashboard, at Paygol's website.

Testing:
- To test the newly installed module you can enable your service's test mode at the "My Services" section of your Dashboard, at Paygol's website. 
  Be sure to change it back when going live.  

Paygol button image:
In order for all instances of the Paygol button to be shown correctly, please do as follows:
- Edit "logos.css" from your BoxBilling installation. It's located at "bb-themes/huraga/assets/css/logos.css".
- Add the following lines to the end of the file.
  
  .logo-Paygol
	{
		background: transparent url("../img/gateway_logos/Paygol.png") no-repeat scroll 0% 0%;
		background-size: contain;
		width:80px;
		height: 28px;
		border: 0;
		margin: 10px;
	}
- Save changes.

Please note: if you are not using the default theme "huraga", you need to do the following:
- Modify the CSS file on the right folder, not in "huraga".
  e.g. "bb-themes/mytheme/assets/css/logos.css".
- Copy image "bb-themes/huraga/assets/img/gateway_logos/Paygol.png" to a similar path for the other theme.
  e.g. "bb-themes/mytheme/assets/img/gateway_logos/Paygol.png".
- As an alternative to the previous steps, just rename the folder name with the right one before copying it to your server.

Important Notes:
- While in test mode, an IPN request (payment notification) will be issued immediately to your platform after each test.
- After a payment is completed it will be shown as completed but Pending Setup until you activate it at your BoxBilling panel.
- Payments are usually notified immediately; however, certain payment methods may take longer to confirm the payment 
  (e.g. methods that take a few minutes to notify the transaction, or voucher-based transactions that require the payer 
  to print it in order to pay by cash at a given place). In these cases the product is shown as not paid, and only 
  once it's confirmed by the provider will it show as paid. We strongly recommend that you inform your customers about this 
  beforehand in order to avoid confusions.
  
  


    		

******* Español *******

Módulo de Paygol v1.1 para BoxBilling

Acerca de este módulo:
- Este módulo permite integrar Paygol fácilmente en tu sistema. Paygol es un sistema de pagos en línea que ofrece una amplia variedad 
  de métodos de pago tanto internacionales como locales tales como tarjeta de crédito y débito, paysafecard, transferencia bancaria, 
  pagos en efectivo, SMS/llamada y más. Más opciones de pago y mayor cobertura significan que para tus clientes es más fácil que nunca pagar 
  por tus productos y servicios, lo que se puede traducir en mayores ventas.

Requerimientos:
- Instalación funcional de BoxBilling (probado con versión 4.20).
- Cuenta en Paygol.
- Servicio Estándar de Paygol, de tipo "Integrado".

Instalación:
- Descomprime el archivo paygol_for_boxbilling_1.0.zip directamente en tu carpeta de BoxBilling.
- Para instalar el módulo, ve al panel de administración de BoxBilling (Configuration -> Payment Gateways), selecciona Paygol en la pestaña "New payment gateways", y haz click en "Install".
- Una vez instalado, procede a la página de configuración del módulo (Configuration -> Payment Gateways), selecciona Paygol y haz click en "Edit".
- Ingresa el ID de tu servicio de Paygol (puedes encontrarlo en la sección "Mis Servicios" de tu panel de control, en el sitio web de Paygol).
- Ingresa Secret key de tu servicio de Paygol (puedes encontrarlo en la sección "Mis Servicios" de tu panel de control, en el sitio web de Paygol).
- Asegúrate de que el módulo está configurado como se indica a continuación:
		- "Enabled: Yes".
		- "Allow one time payments: Yes".
		- "Enable test mode: No". (Favor de leer la sección "Pruebas" de este documento para información acerca de cómo probar tu servicio).
- Copia el "IPN Callback URL" exactamente como se muestra y pégalo en el campo "URL de proceso (IPN)" de la configuración de tu servicio, accesible a través 
  de la sección "Mis Servicios" de tu panel de control, en el sitio web de Paygol.

  
Pruebas:
- Para probar el módulo tras su instalación puedes activar el modo de pruebas de tu servicio en la sección "Mis Servicios" de tu panel de control, en el sitio web de Paygol. 
  Recuerda cambiarlo de vuelta cuando comiences a vender.

Imagen del botón de pago:
Para asegurarte de que todas las instancias del botón de pago de Paygol son mostradas correctamente, por favor sigue las siguientes instrucciones:
- Edit el archivo "logos.css" de tu instalación de BoxBilling. Este archivo se encuentra en "bb-themes/huraga/assets/css/logos.css".
- Agregar las siguientes lineas al final del codigo "logos.css".
	
	.logo-Paygol
	{
		background: transparent url("../img/gateway_logos/Paygol.png") no-repeat scroll 0% 0%;
		background-size: contain;
		width:80px;
		height: 28px;
		border: 0;
		margin: 10px;
	}
- Guardar cambios.	
	
Favor de considerar: en el caso de no utilizar la plantilla por defecto "huraga", es necesario hacer lo siguiente:
- Modificar el archivo CSS en la carpeta correcta, no en "huraga".
  Ej: "bb-themes/mytheme/assets/css/logos.css".
- Copiar la imagen "bb-themes/huraga/assets/img/gateway_logos/Paygol.png" a una ruta similar correspondiente a la otra plantilla.
  Ej: "bb-themes/mytheme/assets/img/gateway_logos/Paygol.png".
- Como alternativa a los puntos anteriores, simplemente cambia el nombre de la carpeta al correcto antes de copiarla a tu servidor.
  
Notas importantes:
- En modo de pruebas se realizará un llamado IPN (notificación de pago a tu plataforma) inmediatamente después de cada prueba.
- Una vez un pago sea completado, el mismo se mostrará como completado pero pendiente de instalación (Pending Setup) hasta que lo actives en tu panel de BoxBilling.
- Los pagos usualmente son notificados inmediatamente; ahora bien, algunos métodos de pago podrían tomar más tiempo en notificar 
  la transacción (ej: métodos que toman algunos minutos en realizar la notificación, o métodos basados en boletos que deben ser 
  impresos y pagados en efectivo). En esos casos el producto se mostrará como no pagado, y sólo una vez sea confirmado por el 
  proveedor se mostrará como pagado. Recomendamos que informes a tu clientela sobre esto a modo de evitar confusiones.
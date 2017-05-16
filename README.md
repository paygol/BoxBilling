# BoxBilling

Paygol module v1.0 for BoxBilling  

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
  
  .logo-PayGol
	{
		background: transparent url("../img/gateway_logos/PayGol.png") no-repeat scroll 0% 0%;
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
- Copy image "bb-themes/huraga/assets/img/gateway_logos/PayGol.png" to a similar path for the other theme.
  e.g. "bb-themes/mytheme/assets/img/gateway_logos/PayGol.png".
- As an alternative to the previous steps, just rename the folder name with the right one before copying it to your server.

Important Notes:
- While in test mode, an IPN request (payment notification) will be issued immediately to your platform after each test.
- After a payment is completed it will be shown as completed but Pending Setup until you activate it at your BoxBilling panel.
- Payments are usually notified immediately; however, certain payment methods may take longer to confirm the payment 
  (e.g. methods that take a few minutes to notify the transaction, or voucher-based transactions that require the payer 
  to print it in order to pay by cash at a given place). In these cases the product is shown as not paid, and only 
  once it's confirmed by the provider will it show as paid. We strongly recommend that you inform your customers about this 
  beforehand in order to avoid confusions.

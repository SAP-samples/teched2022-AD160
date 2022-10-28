Two destinations has been used in this scenerio.<br>
- One destination to connect SAP Build Process Automation with SAP Build Apps 
- To retrieve document from SAP Document Management Service to SAP Process Automation Service.
<BR><BR>

In the interest of time of this session, destinations have been pre-configured in this tenant. Below you can find the configuration setings <br>


Destination to connect SAP Build Process Automation with SAP Build Apps. <br>
Enter this value under URL <pre>https://spa-api-gateway-bpi-eu-prod.cfapps.eu10.hana.ondemand.com/public/workflow/rest/v1/workflow-instances</pre>.

Change the authentication to <b>OAuth2ClientCredentials</b>. Client ID, Client Secret and Token Service URL can retrieved from the SAP Build Process Automation Instance from your tenant.

Add these Additional Properties for this destination to work in SAP Build Apps.<br>
<b>AppgyverEnabled</b><br>
<b>HTML5.DynamicDestination</b><br>
<b>WebIDEEnabled</b>

<br>


![](images/Screenshot%202022-10-28%20at%2013.23.50.png)



Destination to connect SAP Document Management Service to SAP Process Automation Service.<br>
Change the authentication to <b>OAuth2ClientCredentials</b>. Client ID, Client Secret and Token Service URL can retrieved from the Document Management Service Instance from your tenant.

Add these Additional Properties for this destination to work in SAP Build Process Automation.<br>
<b>sap.processautomation.enabled<b>
<br>

![](images/Screenshot%202022-10-28%20at%2013.24.47.png)


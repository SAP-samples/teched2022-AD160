## Table of Contents
- [Overview](#overview)
- [Definition ID from SAP BUILD PROCESS AUTOMATION](#SPA)
- [Definition ID to SAP BUILD APPS](#build)
- [Testing the Scenerio](#Test)

## Testing the End to End Scnerio. <a name="overview"></a>
Although, your application is connected to SAP Build Process Automation service, it is not connected to the process you created yet. In this stage, you will see how to connect your app and process.

## Copy Definition ID from SAP Build Process Automation <a name="SPA"></a>
1. Open the <b>Application lobby</b> again. <br>
    Open the <b>Monitor</b> tab.<br><br>
![](images/ss1.png)

2. Click on <b>Process and Workflow</b> under the <b>Manage </b> section.<br><br>
![](images/Processes%20and%20Workflows.png)

3. Search for your project name under <b>Project</b>. Select the project you created with the ID provided to you. Ex: <b>Invoice Process AD160-XXX</b>.<br><br>
![](images/Search%20invoice.png)

4. After you find your process, copy its <b>Definition ID</b>.<br><br>
![](images/Def%20ID.png)

## Enter the Definition ID in SAP Build Apps. <a name="build"></a>

1. Now, Open your AppGyver Project and click on <b>DATA</b> tab. <br><br>
![](images/ss4.png)

2. Select the <b>SendtoSPA</b> data entity.<br><br>
![](images/ss5.png)

3. In the <b>create</b> tab, open the bindng menu for <b> Request body mapper</b>.<br><br>
![](images/ss6.png)

4. Open the formula editor. Enter the following formula.<br><pre>ENCODE_JSON({  "definitionId": "<b>Your Definition ID copied from SPA</b> ",  "context":  query.record })  </pre>
and click on <b>SAVE</b>.<br><br>
![](images/ss7.png)

5. Click on <b>SAVE</b>.<br><br>
![](images/ss8.png)

6. Now <b>SAVE DATA RESOURCE</b>.<br><br>
![](images/ss9.png)

7. Click on <b>SAVE</b> on the top right corner to the save the changes.
![](images/ss10.png)


## Testing the Scenerio <a name="Test"></a>

1. Now, open the <b>Launch</b> tab.<br><br>
![](images/ss11.png)

2. Click on <b> OPEN APP PREVIEW PORTAL</b>.<br><br>
![](images/ss12.png)

3. Select the AppGyver project you created.<br><br>
![](images/App.png)

4. Enter the name and upload the invoice to test the process.
The invoice can be downloaded here <a href="https://github.com/SAP-samples/teched2022-AD160/blob/main/exercises/1_CreateAppGyverProject/images/Invoice.png?raw=true">Invoice</a>.
![](images/ss14.png)


## summary

Now, you have successfully connected your app and process and also tested it End-to-End.
![Summary](./images/Summary.png)

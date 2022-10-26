
## Testing the End to End Scnerio.


1. Open the <b>Application lobby</b> again. <br>
    Open the <b>Monitor</b> tab.<br><br>
![](images/ss1.png)

2. Click on <b>Process and Workflow</b> under the <b>Manage </b> section.<br><br>
![](images/Processes%20and%20Workflows.png)

3. Search for your project name under <b>Project</b>. Select the project you created with the ID provided to you. Ex: <b>Invoice Process AD160-XXX</b>.<br><br>
![](images/Search%20invoice.png)

4. After you find your process, copy its <b>Definition ID</b>.<br><br>
![](images/Def%20ID.png)

5. Now, Open your AppGyver Project and click on <b>DATA</b> tab. <br><br>
![](images/ss4.png)

6. Select the <b>SendtoSPA</b> data entity.<br><br>
![](images/ss5.png)

7. In the <b>create</b> tab, open the bindng menu for <b> Request body mapper</b>.<br><br>
![](images/ss6.png)

8. Open the formula editor. Enter the following formula.<br><pre>ENCODE_JSON({  "definitionId": "<b>Your Definition ID copied from SPA</b> ",  "context":  query.record })  </pre>
and click on <b>SAVE</b>.<br><br>
![](images/ss7.png)

9. Click on <b>SAVE</b>.<br><br>
![](images/ss8.png)

10. Now <b>SAVE DATA RESOURCE</b>.<br><br>
![](images/ss9.png)

11. Click on <b>SAVE</b> on the top right corner to the save the changes.
![](images/ss10.png)

12. Now, open the <b>Launch</b> tab.<br><br>
![](images/ss11.png)

13. Click on <b> OPEN APP PREVIEW PORTAL</b>.<br><br>
![](images/ss12.png)

14. Select the AppGyver project you created.<br><br>
![](images/App.png)

15. Enter the name and upload the invoice to test the process.
The invoice can be downloaded here <a href="https://github.com/SAP-samples/teched2022-AD160/blob/main/exercises/1_CreateAppGyverProject/images/Invoice.png?raw=true">Invoice</a>.
![](images/ss14.png)

## summary

![Summary](./images/Summary.png)


## Testing the End to End Scnerio.


1. Open the <b>Application lobby</b> again. <br>
    Open the <b>Monitor</b> tab.
![](images/ss1.png)

2. Click on <b>Process and Workflow</b> Instances in the <b>Manage section</b>.
![](images/ss3.png)

3. Find your process and copy its <b>Definition ID</b>.
![](images/ss2.png)

4. Now, Open your AppGyver Project and click on <b>DATA</b> tab.
![](images/ss4.png)

5. Select the <b>SendtoSPA</b> data entity.
![](images/ss5.png)

6. In the <b>create</b> tab, open the bindng menu for <b> Request body mapper</b>.
![](images/ss6.png)

7. Open the formula editor. Enter the following formula.
<pre>ENCODE_JSON({  "definitionId": "<b>Your Definition ID copied from SPA</b> ",  "context":  query.record })  </pre>
and click on <b>SAVE</b>.
![](images/ss7.png)

8. Click on <b>SAVE</b>.
![](images/ss8.png)

9. Now <b>SAVE DATA RESOURCE</b>.
![](images/ss9.png)

10. Click on <b>SAVE</b> on the top right corner to the save the changes.
![](images/ss10.png)

11. Now, open the <b>Launch</b> tab.
![](images/ss11.png)

12. Click on <b> OPEN APP PREVIEW PORTAL</b>.
![](images/ss12.png)

13. Select the AppGyver project you created.

![](images/ss13.png)

14. Enter the name and upload the invoice to test the process.
The invoice can be downloaded here <a href="https://github.com/SAP-samples/teched2022-AD160/blob/main/exercises/1_CreateAppGyverProject/images/Invoice.png?raw=true">Invoice</a>.
![](images/ss14.png)

# summary

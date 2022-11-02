
## Table of Contents
- [Overview](#overview)
- [Create New Project](#buildapps)
- [Create UI](#UI)
- [Data Connection](#data)
- [Logic for Upload button](#upload)
- [Logic for Submit Button](#submit)
- [Summary](#Summary)


# Overview <a name="overview"></a>


In this exercise, you will build your app in SAP Build Apps to upload invoices.

![Scenario](images/scenario_appgyver.png)


## Create a Build Apps Project <a name="buildapps"></a>

1. Within the application development lobby, click <b>Create</b> and then select <b>Build Apps Project</b>.<br>
<br>![Create the project](images/011.png)

2. Under Project Name, enter <b><i>"Invoice AD160-XXX"</b></i>, replace XXX with your user ID. For example, <i>"Invoice AD160-087"</i>.<br>Click on <b>Create</b> to start building your application.
<br><br>![Name the project](images/New%20project.png)


## Create UI <a name="UI"></a>
1. You will be redirected to Build Apps Composer, which is like an IDE for SAP Build Apps. In the canvas, you can already see a <b>Title</b> and <b>Text</b> component.<br><br>![home page](images/01.png)

2. Click on “<i>Headline</i>” on the canvas to select the <b>Title</b> component.
Now, the properties tab on the right-hand side will show the properties of the Title component
where you can modify this component.<br> Under <b>Content</b>, enter “<i>Invoice Approval</i>”<br><br>![Title component](images/02%202.png)

3. Select the <b>Text</b>, modify the content of the component under the properties on right-hand side to "<i>Enter your name and upload your invoice</i>".<br><br>![text component](images/03.png)

4. Drag and drop a <b>Input field</b> from the <b>UI Component</b> library to the canvas. <br><br>![input component](images/04.png)

5. Under the properties of the Input field, clear the <b>Label</b> and change the placeholder text to "<i>Enter your name</i>".<br><br>![input properties](images/05.png)

6. Drag and drop a <b>Button</b> component from the component library on the left-hand side to the canvas. <br>Change the <b>Label</b> on the button in the properties tab of the button component to “<i>Upload your Invoice</i>”.<br><br>![Button](images/06.png)

7. Drag and drop an <b>Image</b> component, to the canvas.<br><br>
![Image](images/07.png)

8. Switch to <b>Variables</b> view.
> In <b>Variables view</b>, you can create variables which can store information temporarily.

  <br><br>![Variables](images/08.png)

9. Create an App Variable by clicking on <b>ADD APP VARIABLE</b> and rename it to "<i>name</i>".<br><br>
![create variable](images/09.png)

10. Add another <b>App Variable</b> and rename it to "<i>Invoicescan</i>".<br><br>
![create another variable](images/10.png)

11. Change the <b>Variable Value Type</b> of <b>Invoicescan</b> to <b>Local filesystem path</b>.<br><br>
![variable type](images/11.png)

12. Add another <b>App variable</b> and rename it to <b>filename</b>.<br><br>
![variable type](images/71.png)


13. Switch back to <b>VIEW</b>. <br><br>
![View](images/VIEW.png)

14. Under the properties tab of <b>Input field component</b>, open the binding menu for <b>Value</b> by clickin on "<b>X</b>" icon.<br><br>
![bind menu](images/13.png)

15. The binding menu will pop-up. Select <b> Data and Variables</b>.<br><br>![binding menu ](images/14.png)

16. Select <b> App Variable</b>.<br><br>
![app variable inbind menu](images/15.png)

17. Now, select <b>name</b> in the list of App variables available.<br><br>
![name of app vairble](images/16.png)

18. Click on <b>SAVE</b> button to the save the binding to the component value.<br><br>
![SAVE button](images/17.png)

19. A variable can be binded to this image component. Open the binding menu of the image under properties on the right-hand side.<br><br>
![bind menu](images/18.png)

20. The binding menu will be pop-up. Select <b>Data and Variables</b>.<br><br>
![bind image](images/19.png)

21. Select <b>App Variables</b>.<br><br>
![app variables](images/20.png)

22. Now select <b>Invoicescan</b> under the list of available app variables and click on <b>SAVE</b> to save the binding to the image component.<br><br>
![variable](images/21.png)

23. Drag and drop another <b>Button</b> component from component library to the canvas and rename the label to <b>Submit</b>.<br><br>
![Submit ](images/22.png)

24. The submit button should be visible only after the invoice is selected. Click on <b>ADDVANCED PROPERTIES</b> to change the visibility properties of the button. Open the binding menu for the visibility properites.<br><br>
![](images/23.png)

25. Select the <b>Formula</b>.<br><br>
![](images/24.png)

26. In the formula bar enter the following formula:
<br><br>

  <pre>IF(IS_EMPTY(appVars.Invoicescan),false,true)</pre>

  > This formula checks if the <b>InvoiceScan</b> page variable is empty, then the output will be false and component will be disabled. If the <b>InvoiceScan</b> page variable have some value, the output will change to true, and component will be displayed.<br>

  Click on <b>SAVE</b>.

  ![](images/25.png)

26. Click on <b>SAVE</b>.<br><br>
![](images/26.png)

27. Click on <b>SAVE</b> on the top right corner to the save the UI created so far.<br><br>
![](images/27.png)

## Data Connection <a name="Data"></a>

Now, your application will be connected to Document Management System and SAP Process Automation. First, you should enable BTP authentication to connect your app to SAP Process Automation via Destinations.

1. Chosse <b>AUTH</b> tab on the top of the screen.<br><br>
![](images/36.png)

2. Select on <b>Enable Authentication</b>.<br><br>
![](images/37.png)

3. Select <b>SAP BTP authentication</b>.
![](images/38.png)

4. Click on <b>OK</b> button to enable the BTP authentication to your application.
![](images/39.png)

5. Click on <b>DATA</b> tab now.
![](images/40.png)


6. Click on <b>CREATE DATA ENTITY</b> and select <b>SAP BTP destination REST API integration</b>.<br><br>
![](images/41.png)

7. In <b>BTP destination name</b>, select <b>AppgGyver_SPA</b>.<br><br>
![](images/Destination.png)

8.  Under <b> Data resource name</b>, a name can be given to this data connection, like "<i>SendtoSPA</i>".<br><br>
![](images/43.png)

9. Under <b>Resource schema</b>, click on <b>+ ADD NEW</b> to create a schema. Name the new schema as "<i>filename</i>" and select the field type to <b>Text</b>.

  > Schema is structure of the data. A schema is created which is similar to the Data base. In this scenerio the data base is Document Management System(DMS), and schema should be created matching the schema in DMS.

  ![](images/44.png)<br><br>

10. Similarily, add three other schema with the following names:
  - "<i>foldername</i>"
  - "<i>employeename</i>"
  - "<i>employeemail</i>"

  Select the field type for all of them as <b>Text</b>.

    ![](images/newdata.png)

11. Select the <b>create</b> tab, and enable it.<br><br>
![](images/46.png)

12. Open the binding menu for <b>Request Headers</b> by clicking on <b>X</b> icon.<br><br>
![](images/47.png)

13. In the binding menu, select <b>List of values</b>.<br><br>
![](images/48.png)

14. Click on <b>Add value</b>, and enter the following values:
  - <b>Header name</b>: <i> Content-Type</i><br>
  - <b>Header value</b>:<i> application/json</i><br><br>
  Click on <b>SAVE</b>.<br><br>
![](images/49.png)


15. <b>Request body mapper</b> value will be binded after creating the process using SAP BUILD PROCEESS AUTOMATION.

  Click on <b>SAVE DATA RESOURCE</b>. The a connection between your Application and Process is created using Destinations.
    ![](images/53.png)


16. Add another Data entity to store the invoice in Document Management Service.

  > For this data connection, Destinations are not used because, the response from Document Management Service is in XML format. AppGyver can only read JSON responses.<br> Because of this reason Document Management Service is connected using DIRECT REST API. <br><br>

  Click on <b> CREATE DATA ENTITY</b> and now select <b>REST API direct integration</b>.

  ![](images/54.png)<br><br>

17. In the <b>BASE</b> tab of the API configuration enter the following values:
  - <b>Resource ID</b> : Documentupload
  - <b>Resource URL</b>: https://end-to-end-demo-lcnc-trial.integrationsuitetrial-apim.eu10.hana.ondemand.com/end-to-end-demo-lcnc/httpjsonv2/docrepouploadteched

  ![](images/55.png)

18. Select the <b>CREATE RECORD</b> tab and enable it.<br><br>
![](images/56.png)

19. Switch to <b>SCHEMA</b> tab.<br>
 Under <b>Create record (POST) request schema</b> use the drop down list and select <b>Custom schema</b>.<br><br>
![](images/57.png)

20. Click on <b>ADD PROPERTY</b>. Rename the key in the property to “<i>base64</i>”.<br><br>
![](images/58.png)

21.  Add another property and rename it to “<i>fileName</i>”. and click on <b>SAVE DATA ENTITY</b>. <br><br>
![](images/59.png)

22. Click on <b>SAVE</b> on the top right corner of the screen.<br><br>
![](images/60.png)


## Create Logic for Upload button <a name="upload"></a>

1. Go to the **UI Canvas**. Select the <b>upload</b> button and click on the grey bar in the bottom to open the logic composer. <br><br>
![](images/28.png)

2. By default, the trigger event will be <b>Component tap</b>.<br>
Now you will download a new component from the <b>MARKETPLACE</b>.

  > MARKETPLACE</b> contains hundreds of pre-built visual and logic components, which can be installed and used with minimum or no customisation.
  Find more information on <a href="https://docs.appgyver.com/docs/marketplace?highlight=Market%20place">MARKETPLACE here</a>.

  ![](images/29.png)

3. In the search bar, search for “<i>pick image</i>”. Select the <b>Pick image from library </b>component.<br><br>
![](images/30.png)

4. Click on <b>Install</b> to install the logic component in the library.<br><br>
![](images/31.png)

5. Drag and drop the <b>Pick image from library</b> under Installed tab to the logic canvas. Connect output node of the <b>Component tap</b> logic component with the <b>Pick image
from library</b>.<br><br>
![](images/32.png)

6. From the Core tab of the component library drag and drop the <b>Set app variable</b> component and connect the node of <b>Pick image from library</b> and <b>Set app variable</b>.<br><br>
![](images/33.png)

7. In the properties tab of the <b>Set app variable</b>, select the variable <b>Invoicescan</b>.<br><br>
![](images/34.png)

8. Now open the binding menu for <b>Assigned Value</b>. <br><br>
![](images/101.png)

9. Select <b>Output value of another node</b>.<br><br>
![](images/102.png)

10. You can see the available nodes in the canvas. Select <b>Pick image from library</b> node. A list of outputs from node will appear. Select <b>
path</b>.<br><br>
![](images/103.png)

11. Click on <b>Save</b>.<br><br>
![](images/104.png)




## Create logic for Submit button. <a name="submit"></a>

1. Select the <b>Submit</b> button and click on the grey bar in the bottom to open the logic composer.<br><br>
![](images/63.png)

2. Download a new component from the <b>MARKETPLACE</b>.<br><br>
![](images/64.png)

3. In the search bar, search for “<i>base64</i>” and select <b>Convert file to base64</b>
and <b>Install</b> it. <br><br>
![](images/65.png)


4. Drag and drop <b>Convert file to base64</b> to the logic canvas.<br><br>
![Submit](images/66.png)

5. Connect the nodes of <b>Component tap</b> and <b>Convert file to base64</b>.
Open the binding menu for <b>Source file URL</b> of the <b>Convert file to base64</b> logic component.<br><br>
![Submit](images/67.png)

6. In the binding menu select <b>Data and Variables</b> and select <b>App variable</b>.<br><br>
![Submit](images/68.png)

7. Select <b>Invoicescan</b> and click on <b>SAVE</b>.<br><br>
![Submit](images/70.png)

8. Drag and drop <b>Set app variable component</b> from the component library and connect the node with <b>Convert file to base64</b>.
<br>In the properties tab, make sure the variable is <b>filename</b>, and now open the binding menu for the assigned value.<br><br>
![Submit](images/72.png)

9. Select <b>Formula</b> in the in the binding menu.<br><br>
![Submit](images/73.png)

10. Open the formula editor. Select App variable and double click on <b>appVars.name</b> to use the function.<br><br>
![Submit](images/74.png)

11. Add the following values.
<br><pre>+TIMESTAMP()+".png"</pre>
The overall formula will look like.<br><pre>appVars.name+TIMESTAMP()+".png"</pre>
Click on <b>SAVE</b>.
<br><br>![Submit](images/75.png)

12. Drag and drop <b>Create record</b> logic component to logic canvas. In the properties tab of the logic component check if the <b>Resource name</b> is <b>Documentupload</b>. Open the binding menu of <b>Record properties</b>.<br><br>
![Submit](images/76.png)

13. In the binding menu, select <b>Object with properties</b>.<br><br>
![Submit](images/77.png)

14.  Open the binding menu for <b>base64</b>.<br><br>
![Submit](images/78.png)

15. In the binding menu select <b>Formula</b> and open the formula editor.In the formula editor, enter the following formula.
<br><pre>REPLACE_ALL(outputs["Convert file to base64"].base64,"data:image/png;base64,","")</pre>
Click on <b>SAVE</b> button.<br><br>
![Submit](images/79.png)

16. Open the binding menu for <b>filename</b>.<br><br>
![Submit](images/80.png)

17. In the binding menu, select <b>Data and Variables</b> and select <b>App variable</b>. Select the variable <b>filename</b> and click on <b>SAVE</b>.<br><br>
![Submit](images/81.png)

18. Save the bindings.<br><br>
![Submit](images/82.png)

19. Drag and drop another <b>Create record</b> logic component to the logic canvas.
Change the resource name <b>SendtoSPA</b>.						
Open the binding menu for <b>Record properties</b>.<br><br>
![Submit](images/83.png)

20. In the binding menu, select <b>Object with properties</b>.<br><br>
![Submit](images/84.png)

21. Open the binding menu for <b>filename</b>.<Br><br>
![Submit](images/85.png)

22. In the binding menu, select <b>Data and Variables</b> and select <b>App variable</b> and select the variable <b>filename</b>.<br>
Click on <b>SAVE</b>.<br><br>
![Submit](images/86.png)

23. The folder name will be static, enter the value “<i>Invoices</i>”. <br><br>
![Submit](images/87.png)

24. Open the binding menu for the <b>employeename</b>.<br><br>
![Submit](images/88.png)

25. In the binding menu select <b>Data and Variables</b>. Select <b>App variables</b> and then choose <b>name</b>.<br><br>
![Submit](images/89.png)

26. The employeemail will be static, enter the email provided to you "ad160-XXX@education.cloud.sap".  For example: "<i>ad160-087@education.cloud.sap</i>"<br><br>
![Submit](images/90.png)

27. Save the bindings.<br><br>
![Submit](images/91.png)

28. Drag and drop a <b>Toast</b> component.

  > This component displays a message.<br>

  Connect the nodes of <b>Create record</b> and <b>toast</b>. Under properties of Toast component, enter "<i>Your Invoice has been submitted</i>" under toast message.<br><br>
![Submit](images/92.png)

29. **Save** youer work.

## Summary <a name="summary"></a>

Now, you have build app and completed the below steps.

![Summary](images/Scenario_summary.png)

Continue to - [Exercise 2 - Install and configure Desktop Agent 3](../2_InstallDesktopAgent3/Install-Desktop-Agent.md) and get started with SAP Build Process Automation.

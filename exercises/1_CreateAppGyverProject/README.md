
# Create an AppGyver Project

In this exercise, you will create a new AppGyver Project to start creating the application.

## Create a New Project

1. Within the application development lobby, click <b>Create</b> and then select <b><i>AppGyver Project</i></b>.
![Create the project](images/Create_AppGyver_Project.png)

2. Under Project Name, enter <b><i>"Company Name Invoice Approval"</b></i>. For example, <i>Cafe Invoice Approval</i>.
Enter a short description for your reference. <b><i>"An application to Scan or upload invoice”</b></i>. <br>
Click on <b>Create</b> to start building your application.

![Name the project](images/02.png)


## Create UI 
1. You will be redirected to AppGyver Composer, which is like an IDE for AppGyver. In the canvas, you can already see a <b>Title</b> and <b>Text</b> component.

![home page](images/01.png)

2. Click on “<i>Headline</i>” on the canvas to select the <b>Title</b> component.
Now, the properties tab on the right-hand side will show the properties of the Title component
where you can modify this component.<br> Under <b>Content</b>, enter “<i>Invoice Approval</i>”

![Title component](images/02%202.png)

3. Select the <b>Text</b>, modify the content of the component under the properties on right-hand side to "<i>Enter your name and upload your invoice</i>".

![text component](images/03.png)

4. Drag and drop a <b>Input field</b> from the <b>UI Component</b> library to the canvas.

![input component](images/04.png)

5. Under the properties of the Input field, clear the <b>Label</b> and change the placeholder text to "<i>Enter your name</i>".

![input properties](images/05.png)

6. Drag and drop a <b>Button</b> component from the component library on the left-hand side to the canvas. <br>Change the <b>Label</b> on the button in the properties tab of the button component to “<i>Upload your Invoice</i>”.

![Button](images/06.png)

7. Drag and drop an <b>Image</b> component, to the canvas.
![Image](images/07.png)

8. Switch to <b>Variables</b> view. 
In <b>Variables view</b>, you can create variables which can store information temporarily. 

![Variables](images/08.png)

9. Create an App Variable by clicking on <b>ADD APP VARIABLE</b> and rename it to "<i>name</i>".

![create variable](images/09.png)

10. Add another <b>App Variable</b> and rename it to "<i>Invoicescan</i>".

![create another variable](images/10.png)

11. Change the <b>Variable Value Type</b> of <b>Invoicescan</b> to <b>Local filesystem path</b>.

![variable type](images/11.png)

12. Switch back to <b>VIEW</b>.

![View](images/12.png)

13. Under the properties tab of <b>Input field component</b>, open the binding menu for <b>Value</b> by clickin on "<b>X</b>" icon.

![bind menu](images/13.png)

14. The binding menu will pop-up. Select <b> Data and Variables</b>.

![binding menu ](images/14.png)

15. Select <b> App Variable</b>.

![app variable inbind menu](images/15.png)

16. Now, select <b>name</b> in the list of App variables available.

![name of app vairble](images/16.png)

17. Click on <b>SAVE</b> button to the save the binding to the component value.

![SAVE button](images/17.png)

18. A variable can be binded to this image component. Open the binding menu of the image under properties on the right-hand side.

![bind menu](images/18.png)

19. The binding menu will be pop-up. Select <b>Data and Variables</b>.

![bind image](images/19.png)

20. Select <b>App Variables</b>.

![app variables](images/20.png)

21. Now select <b>Invoicescan</b> under the list of available app variables and click on <b>SAVE</b> to save the binding to the image component.

![variable](images/21.png)

22. Drag and drop another <b>Button</b> component from component library to the canvas and rename the label to <b>Submit</b>.

![Submit ](images/22.png)

23. The submit button should be visible only after the invoice is selected. Click on <b>ADDVANCED PROPERTIES</b> to change the visibility properties of the button. Open the binding menu for the visibility properites.

![](images/23.png)

24. Select the <b>Formula</b>.

![](images/24.png)

25. In the formula bar enter the following formula.
<pre>IF(IS_EMPTY(pageVars.InvoiceScan),false,true)</pre>
This formula checks if the <b>InvoiceScan</b> page variable is empty, then the output will be false and component will
be disabled. If the <b>InvoiceScan</b> page variable have some value, the output will change to
true, and component will be displayed.<br>
Click on <b>SAVE</b>.

![](images/25.png)

26. Click on <b>SAVE</b>.

![](images/26.png)

27. Click on <b>SAVE</b> on the top right corner to the save the UI created so far.
![](images/27.png)

## Data Connection

Now, your application will be connected to Document Management System and SAP Process Automation. first you should enable BTP authentication to connect your app to SAP Process Automation via Destinations. 

1. Click on <b>AUTH</b> tab on the top of the screen 
![](images/36.png)

2. Click on <b>Enable Authentication</b>. 

![](images/37.png)

3. Select <b>SAP BTP authentication</b>.
![](images/38.png)

4. Click on <b>OK</b> button to enable the BTP authentication to your application.
![](images/39.png)

5. Click on <b>DATA</b> tab now.
![](images/40.png)


6. Click on <b>CREATE DATA ENTITY</b> and select <b>SAP BTP destination REST API integration</b>.

![](images/41.png)

7. In <b>BTP destination name</b>, select <b>AppgGyver_SPA</b>.

![](images/42.png)

8.  Under <b> Data resource name</b>, a name can be given to this data connection, like "<i>SendtoSPA</i>".

![](images/43.png)

9. Under <b>Resource schema</b>, click on <b>+ ADD NEW</b> to create a schema. Name the new schema as "<i>filename</i>" and select the field type to <b>Text</b>

Schema is structure of the data. A schema is created which is similar to the Data base. In this scenerio the data base is Document Management System(DMS), and schema should be created matching the schema in DMS. 

![](images/44.png)

10. Similarily, add three other schema with the following names. <br> "<i>foldername</i>"<br>"<i>employeename</i>"<br>"<i>employeemail</i>" <br>
select the field type for all of them as <b>Text</b>.
![](images/newdata.png)

11. Select the <b>create</b> tab, and enable it.

![](images/46.png)

12. Open the binding menu for <b>Request Headers</b> by clicking on <b>X</b> icon.

![](images/47.png)

13. In the binding menu, select <b>List of values</b>
![](images/48.png)

14. Click on <b>Add value</b>, and enter the following values. <br>
<b>Header name</b>: <i> Content-Type</i><br>
<b>Header value</b>:<i> application/json</i>

Click on <b>SAVE</b>.

![](images/49.png)

15. <b>Request body mapper</b> value will be binded after creating the process using SAP PROCEESS AUTOMATION>. Now, Click on <b>SAVE DATA RESOURCES</b>.
![](images/53.png)


16. Now add another Data entity to store the invoice in Document Management Service.
Click on <b> CREATE DATA ENTITY</b> and now select <b>REST API direct integration</b>.
![](images/54.png)

17. In the <b>BASE</b> tab of the API configuration enter the following values.<br><br>
<b>Resource ID</b> : Documentupload<br><br>
<b>Resource URL</b>: https://end-to-end-demo-lcnc-trial.integrationsuitetrial-apim.eu10.hana.ondemand.com/end-to-end-demo-lcnc/httpjsonv2/docrepouploadteched<br>

![](images/55.png)

18. Now select the <b>CREATE RECORD</b> tab and enable it.
![](images/56.png)

19. Switch to <b>SCHEMA</b> tab.<br>
 Under <b>Create record (POST) request schema</b> use the drop down list and select <b>Custom schema</b>.
![](images/57.png)

20. Click on <b>ADD PROPERTY</b>.	<br>					
Rename the key in the property to “<i>base64</i>”.
![](images/58.png)

21.  Add another property and rename it to “<i>fileName</i>”. and click on <b>SAVE DATA ENTITY</b>
![](images/59.png)

22. Click on <b>SAVE</b> on the top right corner of the screen.
![](images/60.png)


## Create Logic

1. Open the logic composer for <b>Upload</b> button by click on the grey bar in the bottom
![](images/28.png)

2. By default, the trigger event will be <b>Component tap</b>.<br>
Now we are going to download a new component from the <b>MARKETPLACE</b>.

<b>MARKETPLACE</b> contains hundreds of pre-built visual and logic components, which can be installed and used with minimum or no customisation.
 
more information on <a href="https://docs.appgyver.com/docs/marketplace?highlight=Market%20place">MARKETPLACE</a> 

![](images/29.png)

3. In the search bar, search for “<i>pick image</i>”.<br> Now, select the <b>Pick image from library</b>component.

![](images/30.png)

4. Click on <b>Install</b> to install the logic component in the library.

![](images/31.png)

5. Drag and drop the <b>Pick image from library</b> under Installed tab to the logic canvas.<br>
Connect output node of the <b>Component tap</b> logic component with the <b>Pick image
from library</b>.

![](images/32.png)

6. From the Core tab of the component library drag and drop the <b>Set app variable</b> component and connect the node of <b>Pick image from library</b> and <b>Set app variable</b>.

![](images/33.png)

7. In the properties tab of the <b>Set app variable</b>, select the variable <b>Invoicescan</b>.
![](images/34.png)
## Summary

Now that you have ...
Continue to - [Exercise 1 - Exercise 1 Description](../ex1/README.md)

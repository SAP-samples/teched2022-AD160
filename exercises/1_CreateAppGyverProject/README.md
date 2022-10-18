
# Create an AppGyver Project

In this exercise, you will create a new AppGyver Project to start creating the application.

## Create a New Project

1. Within the application development lobby, click <b>Create</b> and then select <b><i>AppGyver Project</i></b>.
![Create the project](images/Create_AppGyver_Project.png)

2. Under Project Name, enter <b><i>"Company Name Invoice Approval"</b></i>. For example, <i>Cafe Invoice Approval</i>.
Enter a short description for your reference. <b><i>"An application to Scan or upload invoice”</b></i>. <br>
Click on <b>Create</b> to start building your application.

![Name the project](images/02.png)


## Create a Home Page
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

11. Change the <b>Variable Value Type</b> of <b>Invoicescan</b> to <b>Local Systemfile path</b>.

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

18. 
![bind menu](images/18.png)


## Summary

Now that you have ...
Continue to - [Exercise 1 - Exercise 1 Description](../ex1/README.md)

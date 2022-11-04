## Table of Contents
 - [Overview](#overview)
 - [Modify the Automation](#modifyAutomation)
 - [Map Automation parameters to Process parameters](#mapParameters)
 - [Summary](#summary)

### Overview <a name="overview"></a>

In this exercise you will learn:

- How to modify and add an automation as a dependency.

The pre-built automation extracts the data from the Invoice document using AI.

## Modify the Automation <a name="modifyAutomation"></a>

1. Once the dependency is completed, choose **Extract Invoice Data**, select three dots, and then **Open Editor**.

    ![05](./images/010a.png)

2. In **Automation Details**, go to **Input/Output** to modify the parameters.

- Rename **FilePath** to **fileName**.
- Select **Add new input parameter** and name it **folderName**.

    ![05](./images/016a.png)

    After the changes the parameters should look like this:

    ![05](./images/017.png)

3. Now go **Tools**, select **Automations** and drag and drop the **Download document** automation into the canvas, just before **Extract Data** activity.

    ![05](./images/018.png)

4. Select **Download document** automation.

5. You will now map the **Input Parameters**. Select **Edit Expression** next to **uploadedFileName** field.

    ![05](./images/019.png)

6. Map with variable **fileName** and select **Save Expression**.

    ![05](./images/098.png)

7. Select **Edit Expression** next to **folderFileName** field.

    ![05](./images/097.png)

8. Map with variable **folderName** and select **Save Expression**.

    ![05](./images/099.png)

9. The **outputPath** needs to be hard-coded:
    <pre> "C:\\Users\\Public\\" + Step0.fileName </pre>

    > To do so please do not copy and paste the code directly in the **outputPath** field but open the expression editor where you can edit the expression.

10. Open the expression editor and copy the code.

11. Choose **Save Expression**

    ![05](./images/096bis.png)


    ![05](./images/096.png)

12. Click on the **Canvas** in the background.

    ![05](./images/021.png)

13. Under **Tools** search for the activity **Delete File**, drag and drop it into the canvas, just below **Log Message** activity.

    ![05](./images/022.png)

14. Select the activity **Delete File**.

    ![05](./images/095.png)

15. Under **Delete File**, edit the **Input Parameters** as follows:
- Map **fileName** with **fileName**
- under **remotePath** type: C:\Users\Public\

    ![05](./images/023a.png)

16. Go to the process tab **Get Invoice Details**.

    ![05](./images/094.png)

## Map Automation parameters to Process parameters <a name="mapParameters"></a>

1. Select **Extract Invoice Data** and map the following inputs:

- Map **fileName** with **fileName**.
- Map **folderName** with **folderName**.

    ![05](./images/024.png)

2. **Save** your work.

## Summary <a name="summary"></a>

You have now modified the project.

Continue to - [Exercise 6 - Release and Deploy Process](../6_ReleaseDeployProcess/Readme.md)

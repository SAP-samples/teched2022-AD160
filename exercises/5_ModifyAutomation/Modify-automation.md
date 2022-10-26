## Table of Contents
 - [Overview](#overview)
 - [Modify the Automation](#modifyAutomation)
 - [Map Automation parameters to Process parameters](#mapParameters)
 - [Summary](#summary)

### Overview <a name="overview"></a>

In this exercise you will learn:
- How to modify and add an automation as a dependency.


The pre-built automation extracts the data from the Invoice document using AI.

## 1. Modify the Automation <a name="modifyAutomation"></a>


1. Once the dependency is completed, go to **Extract Invoice Data**, select three dots, and choose **Open Editor**

  ![05](./images/010b.png)

2. Modify parameters in **Input/Output**.
- Rename **FilePath** to **fileName**
- Select **Add new input parameter** and name it **folderName**

  ![05](./images/016a.png)

    After changes the parameters should look like this:

  ![05](./images/017.png)

3. Go to the **Tools**, select **Automations** and drag and drop **Download document**.

  ![05](./images/018.png)

4. Select Download Document automation and Map Input Parameters.

5. Select **Edit Expression** next to **uploadedFileName** field.

  ![05](./images/019.png)

6. Map with Variable **fileName** and select **Save Expression**.

  ![05](./images/098.png)

7. Select **Edit Expression** next to **folderFileName** field.

    ![05](./images/097.png)

8. Map with Variable **folderName** and select **Save Expression**.

    ![05](./images/099.png)

9. The **outputPath** needs to hard-coded: "C:\\Users\\Public\\" + Step0.FileName

    ![05](./images/096.png)

10. Click on the **Canvas** in the background.

  ![05](./images/021.png)

11. Under **Tools** search for the Activity **Delete File**, drag and drop it.

  ![05](./images/022.png)

12. Select the Activity **Delete File**.

  ![05](./images/095.png)

13. Under **Delete File** Step edit Input Parameters:
- Map **fileName** with **fileName**
- under **remotePath** type: C:\Users\Public\

  ![05](./images/023a.png)

14. Go to the process Tab **Get Invoice Details**.

  ![05](./images/094.png)

## 3. Map API parameters to Process parameters <a name="mapParameters"></a>

 Select **Extract Invoice Data** and map Inputs:

- Map **fileName** with **fileName**.
- Map **folderName** with **folderName**.

  ![05](./images/024a.png)


## Summary <a name="summary"></a>

You've now modified the project.

Continue to - [Exercise 6 - Release and Deploy Process](../6_ReleaseDeployProcess/run-release-deploy.md)

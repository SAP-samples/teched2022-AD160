# Add an automation to the process

In this exercise you will learn:
- How to modify and add an automation

## 1. Modify the Project


10. Once the dependency is completed, go to **Extract Invoice Data**, select three dots, and choose **Open Editor**

  ![05](./images/010a.png)

11. Modify parameters in **Input/Output**.
- Rename **FilePath** to **fileName**
- Select **Add new input parameter** and name it **folderName**

  ![05](./images/016.png)

    After changes the parameters should look like this:
  ![05](./images/017.png)

12. Go to the **Tools**, select **Automations** and drag and drop **Download document**.

  ![05](./images/018.png)

13. Map Input Parameters.
- Select **Edit Expression**
  ![05](./images/019.png)
- Under **Variables** map accordingly and select **Save Expression**:
|  **Name**    | **Type**
|  :------------- | :-------------
|  `uploadedFileName`       | `fileName`
|  `folderName`     | `folderName`

  ![05](./images/020.png)
- outputPath needs to hard-coded: "C:\\Users\\Public\\" + Step0.FileName

14. Click on the **Canvas** in the background.

  ![05](./images/021.png)

15. Under **Tools** search for the Activity **Delete File**, drag and drop it.

  ![05](./images/022.png)

16. Under **Delete File** Step edit Input Parameters:
- map fileName with fileName
- under remotePath type: C:\Users\Public\

  ![05](./images/023.png)

17. Map Inputs under Extract **Invoice Data**.

    |  **Name**    | **Type**
    |  :------------- | :-------------
    |  `fileName`       | `fileName`
    |  `folderName`     | `folderName`

  ![05](./images/024.png)

19. Map Inputs under Under **Invoice Approval form**.

  ![05](./images/025.png)

17. **Save** changes.

  ![05](./images/026a.png)

## Summary

You've now modified the project.

Continue to - [06](../ex3/run-release-deploy.md)

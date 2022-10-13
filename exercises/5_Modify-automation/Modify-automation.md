# Add an automation to the process

In this exercise you will learn:
- How to modify and add an automation

## 1. Modify the Project

1. Open your project. Choose process **Get Invoice Details**

  ![05](./images//005.png)

2. From the **Editable** version of the go to the **Invoice Request Form**, choose 3 dots and choose **Remove** to delete the form.

    <br>![](/exercises/Modify-automation/images/006.png)

3. Click on the **Canvas** in the background.

    <br>![](/exercises/Modify-automation/images/007.png)

4. Choose **Configure Inputs** in **Inputs** to configure inputs.

    <br>![](/exercises/Modify-automation/images/008.png)

5. Configure three inputs. Enter the names and choose types.

    |  **Name**    | **Type**
    |  :------------- | :-------------
    |  `fileName`       | string
    |  `folderName`     | string
    |  `employeeName`   | string

    **Apply** changes.

    <br>![](/exercises/Modify-automation/images/009.png)


6. Select Project Properties.

    <br>![](/exercises/Modify-automation/images/011a.png)

7. Choose **Configure Agent Version** and select Agent 2.0.22 or higher and **Save**.

    <br>![](/exercises/Modify-automation/images/012.png)

8. Choose **Dependencies** and select **Add Dependency** button.

    <br>![](/exercises/Modify-automation/images/013.png)

9. Under **Package** select **Document Management Repository**.

    <br>![](/exercises/Modify-automation/images/014.png)

    Select **Add** button and close the Project Properties window. Close the window.

    <br>![](/exercises/Modify-automation/images/015.png)

10. Once the dependency is completed, go to **Extract Invoice Data**, select three dots, and choose **Open Editor**

    <br>![](/exercises/Modify-automation/images/010a.png)

11. Modify parameters in **Input/Output**.
- Rename **FilePath** to **fileName**
- Select **Add new input parameter** and name it **folderName**

    <br>![](/exercises/Modify-automation/images/016.png)

    After changes the parameters should look like this:
    <br>![](/exercises/Modify-automation/images/017.png)

12. Go to the **Tools**, select **Automations** and drag and drop **Download document**.

    <br>![](/exercises/Modify-automation/images/018.png)

13. Map Input Parameters.
- Select **Edit Expression**
    <br>![](/exercises/Modify-automation/images/019.png)
- Under **Variables** map accordingly and select **Save Expression**:
|  **Name**    | **Type**
|  :------------- | :-------------
|  `uploadedFileName`       | `fileName`
|  `folderName`     | `folderName`

    <br>![](/exercises/Modify-automation/images/020.png)
- outputPath needs to hard-coded: "C:\\Users\\Public\\" + Step0.FileName

14. Click on the **Canvas** in the background.

    <br>![](/exercises/Modify-automation/images/021.png)

15. Under **Tools** search for the Activity **Delete File**, drag and drop it.

    <br>![](/exercises/Modify-automation/images/022.png)

16. Under **Delete File** Step edit Input Parameters:
- map fileName with fileName
- under remotePath type: C:\Users\Public\

    <br>![](/exercises/Modify-automation/images/023.png)

17. Map Inputs under Extract **Invoice Data**.

    |  **Name**    | **Type**
    |  :------------- | :-------------
    |  `fileName`       | `fileName`
    |  `folderName`     | `folderName`

    <br>![](/exercises/Modify-automation/images/024.png)

19. Map Inputs under Under **Invoice Approval form**.

    <br>![](/exercises/Modify-automation/images/025.png)

17. **Save** changes.

    <br>![](/exercises/Modify-automation/images/026a.png)

## Summary

You've now ...

Continue to - [Exercise 3 - Excercise 3 ](../ex3/README.md)

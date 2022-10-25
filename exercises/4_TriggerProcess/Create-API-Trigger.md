## Table of Contents
 - [Overview](#overview)
 - [Modify the Project](#modifyProject)
 - [Create an API Trigger for Process](#configureInputs)
 - [Summary](#summary)

### Overview <a name="overview"></a>

In this exercise you will learn:

- Configure the API Call to Trigger Process
- Modify the Process to map the other artifacts

## 1. Modify the Project <a name="modifyProject"></a>

1. Open your project Invoice Approval Process AD160-XXX. Choose process **Get Invoice Details**.

 ![04](./images//005.png)

2. From the **Editable** version of the go to the **Invoice Request Form**, choose 3 dots and choose **Remove** to delete the form.

 ![04](./images//006.png)

## 2. Create an API Trigger for Process <a name="configureInputs"></a>

1. Click on the **Canvas** in the background.

 ![04](./images/007a.png)

2. Choose **Configure Inputs** in **Inputs** to configure inputs.

 ![04](./images/008a.png)

3. Configure three inputs. Enter the names and choose types.

    |  **Name**    | **Type**
    |  :------------- | :-------------
    |  `fileName`       | string
    |  `folderName`     | string
    |  `employeeName`   | string

    **Apply** changes.

 ![04](./images/009a.png)

4. Select Project Properties.

 ![04](./images/011a.png)

5. Choose **Configure Agent Version** and select Agent 3.7.XX and **Save**.

 ![04](./images/012a.png)

6. Choose **Dependencies** and select **Add Dependency** button.

 ![04](./images/013.png)

7. Under **Package** select **Document Management Repository**.

 ![04](./images/014.png)

8. Select **Add** button.

 ![04](./images/015a.png)

8. **Close** the Project Properties window.

 ![04](./images/015b.png)

> With this package you can automate some operations on your Document Management Service repository.

## Summary <a name="summary"></a>

You've now created API Triggers for the Business Process.

Continue to - [Exercise 5 - Modify the Automation](../5_Modify-automation/Modify-automation.md)

## Table of Contents
 - [Overview](#overview)
 - [Modify the Project](#modifyProject)
 - [Create an API Trigger for Process](#configureInputs)
 - [Map API parameters to Process parameters](#mapParameters)
 - [Summary](#summary)

### Overview <a name="overview"></a>

In this exercise you will learn:

- Configure the API Call to Trigger Process
- Modify the Process to map the other artifacts
- Map Automation and Process parameters.

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
    |  `employeeMail`   | string

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

## 3. Map API parameters to Process parameters <a name="mapParameters"></a>

1. Select **Invoice Approval form** and map:
- under General: map **employeeMail** with Users

  ![05](./images/025.png)

- under Inputs: map **Employee Name** with **employeeName**.

  ![05](./images/025a.png)

2. Select **Invoice Approval Notification Form** under General: map **employeeMail** with Users.

  ![05](./images/027.png)

3. Select **Invoice Reject Notification Form** under General: map **employeeMail** with Users.

  ![05](./images/028.png)

4. **Save** changes.

  ![05](./images/026.png)

## Summary <a name="summary"></a>

You've now created API Triggers for the Business Process.

Continue to - [Exercise 5 - Modify the Automation](../5_ModifyAutomation/Modify-automation.md)

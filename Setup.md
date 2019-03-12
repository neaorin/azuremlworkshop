# Setup Azure Machine Learning Service

Use the Azure portal to create an Azure Machine Learning workspace. This workspace is the foundational block in the cloud that you use to experiment, train, and deploy machine learning models with Machine Learning. This quickstart uses cloud resources and requires no installation.  
 
In this quickstart, you take the following actions:

* Create a workspace in your Azure subscription.
* Try it out with Python in a Jupyter notebook and log values across multiple iterations.
* View the logged values in your workspace.

The following Azure resources are added automatically to your workspace when they're regionally available:

  - [Azure Container Registry](https://azure.microsoft.com/services/container-registry/)
  - [Azure Storage](https://azure.microsoft.com/services/storage/)
  - [Azure Application Insights](https://azure.microsoft.com/services/application-insights/) 
  - [Azure Key Vault](https://azure.microsoft.com/services/key-vault/)

The resources you create can be used as prerequisites to other Machine Learning service tutorials and how-to articles. As with other Azure services, there are limits on certain resources associated with Machine Learning. An example is compute cluster size. Learn more about the [default limits and how to increase your quota](how-to-manage-quotas.md).

If you don’t have an Azure subscription, create a free account before you begin. Try the [free or paid version of Azure Machine Learning service](http://aka.ms/AMLFree) today.


## Create a workspace 

1. Sign in to the [Azure portal](https://portal.azure.com/) by using the credentials for the Azure subscription you use. 

   ![Azure portal](https://raw.githubusercontent.com/MicrosoftDocs/azure-docs/master/includes//media/aml-create-in-portal/portal-dashboard.png)

1. In the upper-left corner of the portal, select **Create a resource**.

   ![Create a resource in Azure portal](https://raw.githubusercontent.com/MicrosoftDocs/azure-docs/master/includes//media/aml-create-in-portal/portal-create-a-resource.png)

1. In the search bar, enter **Machine Learning**. Select the **Machine Learning service workspace** search result.

   ![Search for a workspace](https://raw.githubusercontent.com/MicrosoftDocs/azure-docs/master/includes/media/aml-create-in-portal/allservices-search.PNG)

1. In the **ML service workspace** pane, scroll to the bottom and select **Create** to begin.

   ![Create](https://raw.githubusercontent.com/MicrosoftDocs/azure-docs/master/includes/media/aml-create-in-portal/portal-create-button.png)

1. In the **ML service workspace** pane, configure your workspace.

   Field|Description
   ---|---
   Workspace name | **mlworkshopXX**
   Subscription | **Azure Pass - Sponsorship**
   Resource group | **mlworkshopXX**
   Location | **West Europe**

   ![Create workspace](https://raw.githubusercontent.com/MicrosoftDocs/azure-docs/master/includes/media/aml-create-in-portal/workspace-create.png)

1. To start the creation process, select **Create**. It can take a few moments to create the workspace.

1. To check on the status of the deployment, select the Notifications icon, **bell**, on the toolbar.

1. When the process is finished, a deployment success message appears. It's also present in the notifications section. To view the new workspace, select **Go to resource**.

   ![Workspace creation status](https://raw.githubusercontent.com/MicrosoftDocs/azure-docs/master/includes/media/aml-create-in-portal/notifications.png)


## Use the workspace

A workspace helps you manage your machine learning scripts. In this section, you take the following steps:

* Open a notebook in Azure Notebooks.
* Run code that creates some logged values.
* View the logged values in your workspace.

This example shows how the workspace can help you keep track of information generated in a script. 

### Open a notebook 

[Azure Notebooks](https://notebooks.azure.com) provides a free cloud platform for Jupyter notebooks that is preconfigured with everything you need to run Machine Learning. From your workspace you can launch this platform to get started using your Azure Machine Learning service workspace.

1. On the workspace page, select **Explore your Azure Machine Learning service Workspace**.

 ![Explore the workspace](https://docs.microsoft.com/en-us/azure/machine-learning/service/media/quickstart-get-started/explore_aml.png)

1. Select **Open Azure Notebooks** to try your first experiment in Azure Notebooks.  Azure Notebooks is a separate service that lets you run Jupyter notebooks for free in the cloud.  When you use this link to the service, information about how to connect to your workspace will be added to the library you create in Azure Notebooks.

 ![Open Azure Notebooks](https://docs.microsoft.com/en-us/azure/machine-learning/service/media/quickstart-get-started/explore_ws.png)

1. Sign into Azure Notebooks.  Make sure you sign in with the same account you used to sign into the Azure portal. Your organization might require [administrator consent](https://notebooks.azure.com/help/signing-up/work-or-school-account/admin-consent) before you can sign in.

1. After you sign in, a new tab opens and a `Clone Library` prompt appears. Cloning this library will load a set of notebooks and other files into your Azure Notebooks account.  These files help you explore the capabilities of Azure Machine Learning.

1. Uncheck **Public** so that you don't share your workspace information with others.

1. Select **Clone**.

 ![Clone a library](https://docs.microsoft.com/en-us/azure/machine-learning/service/media/quickstart-get-started/clone.png)

1. If you see that the project status is stopped, click on **Run on Free Computer** to use the free notebook server.

    ![Run a project on free compute](https://docs.microsoft.com/en-us/azure/machine-learning/service/media/quickstart-get-started/run-project.png)

### Run the notebook

In the list of files for this project, you see a `config.json` file. This config file contains information about the workspace you created in the Azure portal.  This file allows your code to connect to and add information into your workspace.

1. Select **01.run-experiment.ipynb** to open the notebook.

1. The status area tells you to wait until the kernel has started.  The message disappears once the kernel is ready.

    ![Wait for kernel to start](https://docs.microsoft.com/en-us/azure/machine-learning/service/media/quickstart-get-started/wait-for-kernel.png)

1. After the kernel has started, run the cells one at a time using **Shift+Enter**. Or select **Cells** > **Run All** to run the entire notebook. When you see an asterisk, __*__, next to a cell, the cell is still running. After the code for that cell finishes, a number appears. 

1. Follow instructions in the notebook to authenticate your Azure subscription.

After you've finished running all of the cells in the notebook, you can view the logged values in your workspace.

## View logged values

1. The output from the `run` cell contains a link back to the Azure portal to view the experiment results in your workspace. 

    ![View experiments](https://docs.microsoft.com/en-us/azure/machine-learning/service/media/quickstart-get-started/view_exp.png)

1. Click the **Link to Azure Portal** to view information about the run in your workspace.  This link opens your workspace in the Azure portal.

1. The plots of logged values you see were automatically created in the workspace. Whenever you log multiple values with the same name parameter, a plot is automatically generated for you.

   ![View history](https://docs.microsoft.com/en-us/azure/machine-learning/service/media/quickstart-get-started/web-results.png)

Because the code to approximate pi uses random values, your plots will show different values.  

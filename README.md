# Azure Machine Learning Service - Hands-on Workshop

Azure Machine Learning service is a cloud service that you use to train, deploy, automate, and manage machine learning models, all at the broad scale that the cloud provides.

## What is machine learning?

Machine learning is a data science technique that allows computers to use existing data to forecast future behaviors, outcomes, and trends. By using machine learning, computers learn without being explicitly programmed.

Forecasts or predictions from machine learning can make apps and devices smarter. For example, when you shop online, machine learning helps recommend other products you might want based on what you've bought. Or when your credit card is swiped, machine learning compares the transaction to a database of transactions and helps detect fraud. And when your robot vacuum cleaner vacuums a room, machine learning helps it decide whether the job is done.

## What is Azure Machine Learning service?

Azure Machine Learning service provides a cloud-based environment you can use to prep data, train, test, deploy, manage, and track machine learning models.

![Azure Machine Learning service workflow](https://raw.githubusercontent.com/MicrosoftDocs/azure-docs/master/articles/machine-learning/service/media/overview-what-is-azure-ml/aml.png)

## How the service works: Architecture and concepts

This article describes the architecture and concepts for Azure Machine Learning service. The major components of the service and the general workflow for using the service are shown in the following diagram:

![Azure Machine Learning service architecture and workflow](https://raw.githubusercontent.com/MicrosoftDocs/azure-docs/master/articles/machine-learning/service/media/concept-azure-machine-learning-architecture/workflow.png)

The workflow generally follows this sequence:

1. Develop machine learning training scripts in **Python**.
1. Create and configure a **compute target**.
1. **Submit the scripts** to the configured compute target to run in that environment. During training, the scripts can read from or write to **datastore**. And the records of execution are saved as **runs** in the **workspace** and grouped under **experiments**.
1. **Query the experiment** for logged metrics from the current and past runs. If the metrics don't indicate a desired outcome, loop back to step 1 and iterate on your scripts.
1. After a satisfactory run is found, register the persisted model in the **model registry**.
1. Develop a scoring script.
1. **Create an image** and register it in the **image registry**.
1. **Deploy the image** as a **web service** in Azure.

Azure Machine Learning service fully supports open-source technologies. So you can use tens of thousands of open-source Python packages with machine learning components. Examples are PyTorch, TensorFlow, and scikit-learn.
Support for rich tools makes it easy to interactively explore and prepare data and then develop and test models. Examples are [Jupyter notebooks](http://jupyter.org) or the [Azure Machine Learning for Visual Studio Code](https://marketplace.visualstudio.com/items?itemName=ms-toolsai.vscode-ai#overview) extension.
Azure Machine Learning service also includes features that [automate model generation and tuning](https://docs.microsoft.com/en-us/azure/machine-learning/service/tutorial-auto-train-models) to help you create models with ease, efficiency, and accuracy.

By using Azure Machine Learning service, you can start training on your local machine and then scale out to the cloud. With many available [compute targets](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-set-up-training-targets), like Azure Machine Learning Compute and [Azure Databricks](https://docs.microsoft.com/en-us/azure/machine-learning/service/azure/azure-databricks/what-is-azure-databricks), and with [advanced hyperparameter tuning services](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-tune-hyperparameters), you can build better models faster by using the power of the cloud.

When you have the right model, you can easily deploy it in a container such as Docker. So it's simple to deploy to Azure Container Instances or Azure Kubernetes Service. Or you can use the container in your own deployments, either on-premises or in the cloud. For more information, see the article on [how to deploy and where](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-deploy-and-where).

You can manage the deployed models and track multiple runs as you experiment to find the best solution.
After it's deployed, your model can return predictions in [real time](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-consume-web-service) or [asynchronously](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-run-batch-predictions) on large quantities of data.

And with advanced [machine learning pipelines](https://docs.microsoft.com/en-us/azure/machine-learning/service/concept-ml-pipelines), you can collaborate on all the steps of data preparation, model training and evaluation, and deployment.

## What can I do with Azure Machine Learning service?

Using the <a href="https://aka.ms/aml-sdk" target="_blank">main Python SDK</a> and the <a href="https://aka.ms/data-prep-sdk" target="_blank">Data Prep SDK</a> for Azure Machine Learning as well as open-source Python packages, you can build and train highly accurate machine learning and deep-learning models yourself in an Azure Machine Learning service Workspace.
You can choose from many machine learning components available in open-source Python packages, such as the following examples:

- <a href="https://scikit-learn.org/stable/" target="_blank">Scikit-learn</a>
- <a href="https://www.tensorflow.org" target="_blank">Tensorflow</a>
- <a href="https://pytorch.org" target="_blank">PyTorch</a>
- <a href="https://www.microsoft.com/en-us/cognitive-toolkit/" target="_blank">CNTK</a>
- <a href="http://mxnet.io" target="_blank">MXNet</a>

Azure Machine Learning service can also autotrain a model and autotune it for you.
For an example, see [Train a regression model with automated machine learning](https://docs.microsoft.com/en-us/azure/machine-learning/service/tutorial-auto-train-models).

After you have a model, you use it to create a container, such as Docker, that can be deployed locally for testing. After testing is done, you can deploy the model as a production web service in either Azure Container Instances or Azure Kubernetes Service. For more information, see the article on [how to deploy and where](https://docs.microsoft.com/en-us/azure/machine-learning/service/how-to-deploy-and-where).

Then you can manage your deployed models by using the [Azure Machine Learning SDK for Python](https://aka.ms/aml-sdk) or the [Azure portal](https://portal.azure.com/).
You can evaluate model metrics, retrain, and redeploy new versions of the model, all while tracking the model's experiments.

To get started using Azure Machine Learning service, see [Next steps](#next-steps).

## How is Azure Machine Learning service different from Machine Learning Studio?

[Azure Machine Learning Studio](https://studio.azureml.net/) is a collaborative, drag-and-drop visual workspace where you can build, test, and deploy machine learning solutions without needing to write code. It uses prebuilt and preconfigured machine learning algorithms and data-handling modules.

Use Machine Learning Studio when you want to experiment with machine learning models quickly and easily, and the built-in machine learning algorithms are sufficient for your solutions.

Use Machine Learning service if you work in a Python environment, you want more control over your machine learning algorithms, or you want to use open-source machine learning libraries.

> [!NOTE]
> Models created in Azure Machine Learning Studio can't be deployed or managed by Azure Machine Learning service.

## Free trial

If you don’t have an Azure subscription, create a free account before you begin. Try the [free or paid version of Azure Machine Learning service](http://aka.ms/AMLFree) today.

You get credits to spend on Azure services. After they're used up, you can keep the account and use [free Azure services](https://azure.microsoft.com/free/). Your credit card is never charged unless you explicitly change your settings and ask to be charged. Or [activate MSDN subscriber benefits](https://azure.microsoft.com/pricing/member-offers/msdn-benefits-details/?WT.mc_id=A261C142F), which give you credits every month that you can use for paid Azure services.


## Hands-on Labs

1. [Setup Azure ML Service](Setup.md)
1. [Train a model with Azure ML service](Train.md)
1. [Deploy a model in Azure Container Instances](Deploy.md)
1. [Use Automated Machine Learning](Automl.md)
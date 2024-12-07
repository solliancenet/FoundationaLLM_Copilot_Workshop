## Lab4 - Embedding and Vectorization Pipelines

In this lab, we will explore the process of creating a new `datasource` with access to multiple documents and then using the `embedding` and  `vectorization` process and pipeline to create indexes in `Azure AI Search`. 

### Task 1: Create a new Datasource

By January 31st 2025, the Management portal in FoundationaLLM will have the capability to create a new datasource and upload multiple documents to the storage account using the user interface.
For now, we use a POSTMAN Collection to create a new datasource and upload documents to the storage account.

### Starting the process using the API

1. 3 documents have been provided to you in the `data` folder. These documents are `customer_service_data.pdf`, `customer_service_data_2.pdf` and `customer_service_data_3.pdf`. These documents contain the content that we will use to create the datasource and the vectorization profile.

> [!NOTE]
> As you have no access to the Azure Resource Group during the workshop, we added the documents to the storage account for you. You will use the POSTMAN collection to create the datasource and the vectorization profile.

2. **Open POSTMAN**: Open the POSTMAN application and import the collection `New York Workshop Demo.postman_collection.json` that was provided to you in the `data` folder.
3. This collection will allow you to create the datasource, the Vectroization profile and the invoke the Vectorization pipeline to create the indexes in Azure AI Search.

![POSTMAN Collection](/media/Lab4-1.jpg)


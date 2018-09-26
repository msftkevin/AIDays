# Knowledge Mining hands-on labs

## Cognitive search ##
Cognitive search adds data extraction, natural language processing (NLP), and image processing to an Azure Search indexing pipeline, making unsearchable or unstructured content more searchable. Information created by a skill, such as entity recognition or image analysis, gets added to an index in Azure Search.

Let’s try the enrichment pipeline in the Azure portal before writing a single line of code:
•	Begin with sample data in Azure Blob storage
•	Configure the Import Wizard for indexing and enrichment
•	Run the wizard (an entity skill detects people, location, and organizations)
•	Use Search Explorer to query the enriched data.

## Prerequisites ##
Azure services are used exclusively in this scenario. Creating the services you need is part of the preparation.
•	Azure Blob storage provides the source data.
•	Azure Search handles data ingestion and indexing, cognitive search enrichment, and full text search queries.

## Set up Azure Search ##
First, sign up for the Azure Search service.
1.	Go to the Azure portal and sign in by using your Azure account.
2.	Click Create a resource, search for Azure Search, and click Create. See Create an Azure Search service in the portal if you are setting up a search service for the first time and you need more help. 
3.	For Resource group, create a resource group to contain all the resources you create in this tutorial. 
4.	For Location, choose either South Central US or West Europe. Currently, the preview is available only in these regions.
5.	For Pricing tier, you can create a Free service to complete this lab. For deeper investigation using your own data, create a paid service such as Basic or Standard.
A Free service is limited to 3 indexes, 16 MB maximum blob size, and 2 minutes of indexing, which is insufficient for exercising the full capabilities of cognitive search. To review limits for different tiers, see Service Limits.
6.	Pin the service to the dashboard for fast access to service information.
 
## Set up Azure Blob service and load sample data ##
The enrichment pipeline pulls from Azure data sources supported by Azure Search indexers. For this exercise, we use blob storage to showcase multiple content types.
1.	Download sample data consisting of a small file set of different types.
2.	Sign up for Azure Blob storage, create a storage account, sign in to Storage Explorer, and create a container. See Azure Storage Explorer Quickstart for instructions on all the steps.
3.	Using the Azure Storage Explorer, in the container you created, click Upload to upload the sample files.

# Purpose of the document
- Objective:
  This document serves as a proposal for implementation of a data analytics solution on a cloud infrastructure.
- Scope:
  Within the purview of this document lies a high-level architectural proposal, accompanied by a proposal for a robust code framework.
- Out of scope:
  This document does not contain the development of a fully functional Proof of Concept (POC) from start to finish.
- Agreement:
  Upon acceptance of this proposal, all involded stakeholders agree to engage in a development process. This task will be undertaken by a dedicated delivery team that will utilize the code framework presented within this document.
  

# Requirements and needs

# Architecture proposal
Analyzing the needs of the stakeholders,the budget, the existing resurces, the infracture and the data, we recommend a solution that uses Platfor-as-a-Service (PaaS). Hving in mind that the desired outut of the data aims to be used for analyzes from the BI teams and the sales managers, our recommendation is to use Microsoft Azure cloud enabling the Azure Synapse Analytics service.
## Infrastructure: 
Azure as Platform-as-a-Service.
- Required Services: the below listed services must be set up for a fully operational enviroment
  - Azure Subscription and Resource Group: to be created and organise logically to macth the company`s related services.
  - Azure App Service (Web Apps, APIs): create to host your web applications, APIs, and mobile backends.
  - Azure SQL Database: will be your relational database.
  - Azure Storage: to host  files, tables and queques. The storage will be used for Inbound and Outbound data files.
  - Azure Key Vault: to host keys, secrets, and certificates used by your applications.
  - Azure Active Directory (Azure AD):wil be used to manage user identities and access control and integrate Azure AD with your applications for authentication and authorization.
  - Azure Functions: to create serverless functions that respond to events as well as configure triggers, bindings, and deployment options.
  - Azure Logic Apps: to build workflows to automate business processes and integrate services.
  - Synapse Analytics workspace: to be created for ETL purposes

## ETL process proposal
![image](https://github.com/ivarozelin/CloudDataProject/assets/134283235/65285f74-7d96-4884-a5bd-25fb288e111f)

- Web Ui is client based interface that will be connected to Azure Blob Storage throughout Azure Logic Apps.
- Azure Blob storage to be organized in containers as follows:
  - data - generic conatiner that includes the rest of the containers
  - primarydata - will host the original files obtained from the Web Ui
  - inbound - will host the validated files
  - outbound - will host the transformed files
  - errorlog - will host the error files as a result of the primary data validation


  






  
    

# Azure Cloud Resume Challenge
Welcome to my Cloud Resume Challenge for Azure project! ☁️

## [My Web - Click Here!](https://azureresumeyahav.z6.web.core.windows.net/)

![Diagram](https://github.com/DorAvissar/ResumeChallenge-/blob/main/diagram.png?raw=true)

I began by mastering the basics and earned my AZ-900 Azure Fundamentals certification. After completing the certification, I dedicated myself to the Cloud Resume Challenge for Azure.

Over the course of two intensive weekends, totaling around 30-40 hours, I devoted significant effort to this project. Whether you're an experienced professional or new to Azure, I hope my project inspires and assists you on your own cloud computing journey. Let's dive in together!

## Challenge Overview
This challenge is composed of 8 main parts:
1. Configure a Static Website via Azure Storage with a custom domain and HTTP
2. Write your resume in HTML and format it with CSS
3. Setup Azure Storage account and enable Static Website
4. Infrastructure as Code by using Terraform
5. Enable CDN for HTTPS access to your website and custom domain
6. Use Azure Functions App to interact with CosmosDB API to update a visitor counter
7. Write JavaScript to capture the result of the visitor counter function and display it on the site
8. Configure GitHub Actions for CI/CD with Azure Storage

## Prerequisites
- Azure account
- GitHub account
- Azure CLI
- Azure Functions Core Tools
- Visual Studio Code
- Visual Studio Code Extensions
- Azure Functions Extension
- C# Extension
- Azure Storage Extension
- A cheap domain provider 

## Front-end

### Phase 1: Building the Resume Website
I started by building a static resume website using HTML and CSS. I used a template from the internet and customized it to my needs. Here's the result:

![Static Resume Page](https://github.com/yahav123456/Resume_Challenge/assets/166650066/329d5b2d-e262-40d0-8e32-82a75c81e5d0)

### Phase 2: Hosting the Website on Azure
I deployed the static site to Azure Blob Storage, which has an option to host static websites. I uploaded the website files through the CLI. Here's a screenshot of the uploaded files:

![Uploaded Files](https://github.com/yahav123456/Resume_Challenge/assets/166650066/af683086-6349-4ba9-bd4a-65be74d619bc)

## Back-end

### Phase 3: Domain and CDN
I bought a domain on GoDaddy and pointed it to the Azure CDN endpoint. This ensures users from different locations can access the site quickly.

![Domain and CDN](https://github.com/yahav123456/Resume_Challenge/assets/166650066/0b5f3f1c-f105-4941-bb90-f83e7ccac955)

### Phase 4: JavaScript Web App
I created a counter to keep track of page visits using JavaScript. The `main.js` function sends an HTTP request to the Azure Function to get the count and display it.

### Phase 5: Azure Functions
I created an Azure Function with an HTTP trigger to update the visitor count each time the page is loaded. The function fetches the count from Azure Cosmos DB, increments it, and returns the updated count.

![Azure Functions](https://github.com/yahav123456/Resume_Challenge/assets/166650066/afab9a1d-8cbe-4862-8d6c-eac6afa3e2b1)

### Phase 6: Azure Cosmos DB
I created a Cosmos DB to store the visitor count. I used the Table API to manage the data. This documentation helped me understand how it works.

![Cosmos DB](https://github.com/yahav123456/Resume_Challenge/assets/166650066/16eb1741-c60f-488a-8771-493e3853e63f)

### Phase 7: Terraform
To automate resource provisioning, I used Terraform. I imported existing resources to a state file and configured variables, storing sensitive information as environment variables.

### CI/CD
I set up a CI/CD pipeline using GitHub Actions to deploy updates to the Azure Storage container. This workflow also purges the CDN cache to reflect updates immediately.

- Followed [Microsoft's docs on using GitHub Actions to deploy a static website](https://learn.microsoft.com/en-us/azure/storage/blobs/storage-blobs-static-site-github-actions?tabs=userlevel).

![CI/CD Pipeline](https://github.com/yahav123456/Resume_Challenge/assets/166650066/2bc8f90b-3fbb-4408-be02-178aee09404d)
![CI/CD Pipeline](https://github.com/yahav123456/Resume_Challenge/assets/166650066/ca2f1c30-765a-45c7-b743-5294765909c3)

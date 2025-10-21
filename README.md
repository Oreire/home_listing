# home_listing
Employed Github Actions to Deploy Web Application using Azure Static Web Apps

# Azure-Web-Automation
Automation of Static Web Application Deployment on Azure Static Web App with GitHub Actions 

✅ Deployment Validation: Azure Static Web Apps + GitHub Actions

📦 Project Overview

Title: CI/CD Deployment of Home Listing Web App via Azure Static Web Apps
Source Repository: techbleat/home_listing
Deployment Target: Azure Static Web Apps (West Europe region)
Branch: main
App Location: / (root directory)

🛠️ Step 1: Provisioning the Static Web App
Using Azure CLI, the following command provisions the web app:
az staticwebapp create \
  --name home-listing-app \
  --resource-group techbleat-app \
  --location "West Europe" \
  --source GitHub \
  --branch main \
  --app-location "/"


✅ Validation:
- Resource group HomeListingRG scoped for audit and cost tracking
- Region West Europe aligns with GDPR and UK data residency
- GitHub integration ensures traceable source control

🔁 Step 2: GitHub Actions Workflow Configuration

🔐 Step 3: Secrets Management

In GitHub repository settings:
- Add AZURE_STATIC_WEB_APPS_API_TOKEN under Settings → Secrets → Actions
- This token is generated from Azure and scoped to the Static Web App

✅ Validation:
- Secrets are encrypted and not exposed in logs
- Token-based authentication aligns with DevSecOps principles
- GitHub’s built-in GITHUB_TOKEN handles repo access securely

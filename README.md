# Cloud Services & Web App Deployment - Task 3

## Project Overview
This repository documents the deployment of a live web application using Microsoft Azure Static Web Apps. The project demonstrates Platform as a Service (PaaS) hosting, automated CI/CD via GitHub Actions, global networking, and secure secrets management.

## Step 1: Application Development
I created a responsive single-page application using HTML, CSS, and JavaScript. The code is hosted in a separate source code repository (linked below).

*Source Code Repository:* [INSERT LINK TO YOUR `azure-static-web-app` REPO HERE]

## Step 2: Azure Static Web App Deployment
To host the application, I provisioned an Azure Static Web App on the Free tier. 
- **Resource Group:** Task3-RG
- **Plan:** Free
- **Source:** GitHub

By connecting Azure directly to my GitHub account, Azure automatically provisioned the necessary compute and global networking (CDN) to host the site.

*[INSERT SCREENSHOT 1 HERE - The Azure Static Web App summary screen showing Free tier]*

## Step 3: CI/CD Automation
Azure automatically generated a GitHub Actions workflow (`.github/workflows`) in my source code repository. This pipeline automatically builds and deploys the website to the live Azure URL every time I push a change to the `main` branch.

*[INSERT SCREENSHOT 2 HERE - The GitHub Actions tab or the .github folder]*

## Step 4: Secrets & Environment Management
To secure the deployment, I managed environment variables and secrets directly within GitHub. I created an `APP_ENVIRONMENT` secret to represent the production environment, and Azure securely injected its deployment token. This ensures no sensitive credentials are hardcoded in the application code.

*[INSERT SCREENSHOT 3 HERE - The GitHub Secrets page showing APP_ENVIRONMENT and the AZURE token]*

## Step 5: Live Testing & Verification
The deployment was successful, and the static web app is now live on the internet, served securely over HTTPS via Azure's global edge network.

*Live Website:* [INSERT YOUR LIVE AZURE URL HERE]

*[INSERT SCREENSHOT 4 HERE - The live website in the browser]*

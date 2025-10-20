# CI/CD Assignment 1 – HelloApp Pipeline

## Overview
This assignment was to create a simple application and automate the process of building and pushing its Docker image to Docker Hub using GitHub Actions.  
The goal was to make sure the entire process happened automatically on each code push without running any Docker commands manually.

## Project Setup
- **Application:** A basic Python Flask app that returns a simple “Hello World” message.  
- **Dockerfile:** Created to containerise the Flask app and define how it should run.  
- **Docker Hub:** A personal repository was used to store the built Docker image.  

## Workflow Configuration
- The workflow file was created under `.github/workflows/` to automate the process.  
- The pipeline is triggered on every code push to the main branch.  
- The workflow builds the Docker image using the Dockerfile and tags it.  
- It logs in to Docker Hub using credentials stored securely in GitHub Secrets.  
- Once built, the workflow automatically pushes the image to Docker Hub.  

## Secrets and Variables
- **DOCKERHUB_USERNAME** and **DOCKERHUB_TOKEN** were stored in GitHub Secrets.  
- These were used inside the workflow for secure authentication when pushing images.  

## Validation
- Checked that the workflow completed successfully under the GitHub **Actions** tab.  
- Verified the image appeared on Docker Hub with the correct tag.  
- Pulled the image locally using:  
  \`\`\`bash
  docker pull username/repository:tag
  docker run -d -p 5000:5000 username/repository:tag
  \`\`\`  
- Accessed the app on \`http://localhost:5000\` to confirm it was running correctly.

## Summary
This assignment helped me understand how CI/CD automates Docker builds and image delivery.  
By using GitHub Actions, I was able to completely automate building, tagging, and pushing the Docker image to Docker Hub without any manual steps.






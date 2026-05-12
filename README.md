# KinlayGyeltshen_02240347_DSO101_A2

## DSO101 Assignment 2: CI/CD with Jenkins

This repository contains a simple Node.js to-do list app configured for Jenkins CI/CD.

## GitHub Repository Link

https://github.com/kinlay123/KinlayGyeltshen_02240347_DSO101_A2.git

## Pipeline Configuration

The `Jenkinsfile` in the project root defines the pipeline with the following stages:

1. **Checkout**: Pull code from GitHub (`checkout scm`)
2. **Install**: Install dependencies (`npm install`)
3. **Build**: Build project (`npm run build`)
4. **Test**: Run Jest tests and publish `junit.xml` to Jenkins test reports
5. **Deploy**: Build and push Docker image to Docker Hub

## Required Jenkins Setup

1. Install plugins:
   - NodeJS
   - Pipeline
   - GitHub Integration
   - Docker Pipeline (for deployment stage)
2. Configure NodeJS tool in Jenkins as `NodeJS`.
3. Add credentials:
   - GitHub PAT for repository access
   - Docker Hub credentials with ID `docker-hub-creds`

## Challenges Faced

- The initial repository did not contain Assignment 1 app files, so a minimal Node.js to-do app was created from scratch.
- Jenkins test reporting requires JUnit XML format, so `jest-junit` was added and configured to generate `junit.xml`.
- Docker deployment requires Jenkins Docker plugin and valid registry credentials.

## How to Run Locally

```bash
npm install
npm run build
npm test
npm start
```

## Deliverables Checklist

- [ ] Screenshot of successful Jenkins pipeline run
- [ ] Screenshot of Jenkins test results
- [ ] Docker Hub image link
- [ ] GitHub repository link containing `Jenkinsfile`
- [ ] Short report (this README): pipeline setup + challenges
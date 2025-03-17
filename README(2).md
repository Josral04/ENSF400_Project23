# ENSF 400 - Winter 2025 - Course Project

## Project Overview

In this project, you will work based on a software project by incorporating/extending a complete CI/CD (Continuous Integration/Continuous Deployment) pipeline. This is based on an open-source sample application: https://github.com/7ep/demo

This project can also be any application that requires the project of build, test, and deployment.
You will leverage GitHub for source control, Docker for containerizing your application, and a CI/CD tool (Jenkins) to automate the build, testing, and verification process. The goal is to validate every code change automatically through container builds, unit tests, code quality checks, and end-to-end functional tests.


## Project Requirements

By the end of this project, your group must deliver the following:

1.	Manage your project on GitHub and follow proper Git workflows (branching, pull requests, code reviews). Document the process of how you use Git workflows to collaborate with your team members.

1.	Containerize your application for builds and deployments. Upload and download your container images to a public or private image repository (e.g., Docker Hub or GitHub Container Registry). Ensure a container image is built with unique build tag(s) matching the triggering commit from any branch.

1.	Set up an automated CI/CD with Jenkins in a Codespace environment. Configure the pipeline to trigger upon pull requests merging changes into the main branch.

1.	Document the CI/CD process and provide clear instructions on replicating your environment. Submit a video demo at the end of the project.

### Existing Pipelines
You will also demonstrate the delivery of the following process and artifacts that come with the project.

1.	Run static analysis quality-gating using SonarQube
1.	Performance testing with Jmeter
1.	Security analysis with OWASP's "DependencyCheck"
1.	Build Javadocs


## Evaluation Criteria

Your project will be assessed on the following criteria:

### GitHub Repository & Git Workflow (15%)
1.	Project on GitHub in a public repository with all team members participating in the development and maintenance of the project (5%).
1.	Demonstrate the process practicing Git workflows (branching, pull requests, code reviews) (10%).

### Containerization (20%)
1.	Dockerfile to containerize the project (5%).
1.	Use of container image repository to upload and download images (5%).
1.	Effective tagging mechanism for each building matching the commits/branches/pull requests (10%).

### CI/CD Pipeline Automation (40%)
1.	Jenkins integration with GitHub in Codespace (10%).
1.	Triggering automated checks upon pull request to the main branch (10%).
1.	Deployment process to automatically deploy the application in the Codespace environment upon a build (10%).
1.	Be able to run items 5-8 in **Existing Pipelines** (10%).

### Testing & Code Quality (10%)
1.	Generate test coverage reports upon each automated build (5%).
1.	Generate code quality report using SonarQube reports upon each automated build (5%).

### Documentation & Demo (15%)
1.	Clarity and completeness of README and other documentation. The documentation must demonstrate the team’s collaboration process (5%).
1.	Demonstration video with a length not exceeding 10 minutes, showing a clear understanding of the pipeline and its benefits. The documentation must demonstrate the team’s collaboration process (10%).

_______________________________________________________________________________________________________________________________________________________________________________________________________________

# Organization of our ENSF 400 CI/CD Project  

## Team Members  
- Josral Frederick UCID: 30195360
- Muhammad Aun Raza My UCID: 30172183
- Natnael Tekli UCID: 30171167
- Jaden Chow UCID: 30173676


## Project Description  
The main objective in this project is to create software that incorporates/extends a complete CI/CD 
(Continuous Integration/Continuous Deployment) pipeline. 

## Git Workflow  
Our team follows a structured Git workflow to manage our project efficiently on GitHub.

We begin by cloning the repository using git clone <repository_url>. Before making changes, we create a new feature branch with git checkout -b feature/feature-name to keep our work organized.

Once changes are made, we stage and commit them using git add . and git commit -m "Description of changes", ensuring clear commit messages.

To keep our branch up-to-date, we sync it with the main branch by switching to main, pulling the latest changes (git pull origin main), and merging them into our feature branch (git merge main). If merge conflicts arise, we resolve them before proceeding.

After finalizing our changes, we push our branch to the remote repository using git push origin feature/feature-name. We then open a Pull Request (PR) on GitHub, providing a description of our modifications.

Team members participate in a code review process, leaving feedback and suggesting necessary improvements. Once approved, the PR is merged into main, typically by a team lead or someone with write access.

After merging, we delete the feature branch both locally (git branch -d feature/feature-name) and remotely (git push origin --delete feature/feature-name). To stay updated, we sync our local repository with the latest changes using git pull origin main.

We follow GitFlow best practices, using descriptive branch names (e.g., feature/login-page, bugfix/error-handling) and ensuring every change is reviewed via a PR before merging into main.
External contributors fork the repository, create a new branch, make their changes, and open a PR to contribute to the project.

This workflow ensures a structured and collaborative development process, keeping our codebase clean and organized.

## Containerization  
- **Dockerfile**:
  A Dockerfile is a set of instructions to automate the creation of a Docker Image. The Dockerfile helps containerize the application, ensuring it is built, tested and deployed.
  This is done by packaging the application into a container, works with Kubernetes and enables automation in the CI/CD pipeline.

- **Image Repository**: Instructions for pushing/pulling images and how tagging works.  
Container images will be pushed to **Docker Hub**. To push an image, use the following command:  
  ```bash
  docker push <your-dockerhub-NatnaelTekli>/task-manager-app:<tag>   



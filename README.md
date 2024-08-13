# End-to-End-CICD-Implementation

Implemented an end-to-end CI/CD pipeline for java-based application using Jenkins
declarative pipeline which include various stages such as Build, Unit testing, Static code
analysis, SAST, DAST, Creation of Docker Images, Deployment on Kubernetes platform using
Argo CD.

Pipeline Workflow

Source Code Management:

The source code is managed in a Git repository.
A webhook triggers the CI/CD pipeline when changes are pushed to the repository.
Jenkins:
Jenkins is the orchestrator of the pipeline.
It starts the process by pulling the latest changes from the Git repository.
Maven:
Jenkins triggers a Maven build to compile the code and manage dependencies.
If the build is successful, the process moves on to code quality analysis.
SonarQube:
The code is analyzed using SonarQube to ensure it meets quality standards.
If the code passes the quality checks, it proceeds to testing.
Automated Testing:
The code undergoes automated testing to validate functionality.
If all tests pass, the pipeline continues to the next step.
Docker:
The application is packaged into a Docker image.
The new Docker image is pushed to DockerHub.
Image Updater:
The Image Updater updates the application with the new Docker image.
Argo CD:
Argo CD manages the deployment of the application to the Kubernetes cluster.
The Manifests Repo is updated with the new image, and Argo CD deploys it to Kubernetes.
Reporting:
Jenkins generates reports based on the results of the pipeline.
Notifications are sent to the development team via Slack and email.

Components
Jenkins: CI/CD tool used for orchestrating the pipeline.
Maven: Build automation tool used for compiling the code.
SonarQube: Static code analysis tool for ensuring code quality.
Docker: Containerization platform used to package the application.
Argo CD: GitOps continuous delivery tool for Kubernetes.

Prerequisites
Jenkins installed and configured.
Maven installed.
SonarQube server running and configured.
Docker installed and a DockerHub account.
Argo CD installed and configured with Kubernetes.

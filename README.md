# # ioromero

This repository contains a simple `deployment.yaml` file for deploying an application. It is being monitored by ArgoCD from another repository, [inception-of-things](https://github.com/iker-gonzalez/inception-of-things). Any change made to the Docker image version in `ioromero` will automatically trigger an update to the exposed application in `inception-of-things` through ArgoCD.

## Deployment

The deployment is managed through Kubernetes manifests defined in the `deployment.yaml` file. This includes specifications for pods, services, and any other necessary resources for running the application.

## Monitoring with ArgoCD

ArgoCD is configured to watch for changes in this repository. When a change is detected, ArgoCD automatically syncs the application state with the defined manifests, ensuring that the application is always up to date with the latest configurations.

## Usage

To use this repository effectively, follow these steps:

1. Make changes to the Docker image version in the `deployment.yaml` file as needed.
2. Commit and push the changes to the `ioromero` repository.
3. ArgoCD, configured in the `inception-of-things` repository, will detect the changes and automatically update the exposed application to the newly updated Docker image version.

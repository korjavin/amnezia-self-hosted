# Amnezia VPN GitOps Repository

This repository contains the configuration for deploying a self-hosted Amnezia VPN server using a GitOps workflow with Portainer.

## Features

-   **Protocol:** Utilizes the "over-cloak" protocol for obfuscation.
-   **Containerization:** Includes a `docker-compose.yaml` file for easy deployment with Portainer.
-   **Reverse Proxy:** Contains labels for Traefik to enable SSL and manage routing.
-   **CI/CD:** Implements a GitHub Action to trigger the build and deployment process. For more details, see the `../deployment_prompt.md` file.

## Prerequisites

-   A server with Docker and Portainer installed.
-   Traefik set up as a reverse proxy.
-   A domain name for the VPN server.

## Usage

1.  Fork this repository.
2.  Configure the `docker-compose.yaml` with your specific settings (e.g., domain name).
3.  Set up the repository in Portainer as a GitOps stack.
4.  Pushing changes to the `main` branch will trigger the GitHub Action to automatically update the deployment.
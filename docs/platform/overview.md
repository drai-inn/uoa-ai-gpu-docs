# Platform Architecture

The UoA Research AI GPU Platform is designed to provide a scalable and secure environment for AI research.

## Overview

The platform is built as a Kubernetes (K8s) environment, integrating various components to manage user access, security, and resource allocation.

### Key Components

-   **Kubernetes Cluster**: The core orchestration layer for managing containerized AI workloads.
-   **Keycloak**: Handles user authentication and role-based access control (RBAC).
-   **Policies**: Defines usage policies and resource limits for different user roles.

## Repository

For detailed configuration files, including K8s manifests, Keycloak setup, and policy definitions, please refer to the source repository:

[**drai-inn/ai-gpu-platform**](https://github.com/drai-inn/ai-gpu-platform)

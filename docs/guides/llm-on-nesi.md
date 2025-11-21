# Running LLMs on NeSI

This guide provides an overview of how to deploy and run Large Language Models (LLMs) on the NeSI HPC platform using the UoA AI GPU resources.

## Prerequisites

Before you begin, ensure you have:

-   **Docker Engine**: Installed locally (e.g., [Docker Desktop](https://docs.docker.com/engine/install/ubuntu/#install-using-the-repository)).
-   **SSH Access**: Configured SSH keys for accessing the VM (`GatewayPorts yes` required in `sshd_config`).
-   **DuckDNS**: A domain and API key for external access.
-   **API Keys**: OpenAI, LiteLLM, etc., as needed for your specific model.

## Quick Start

1.  **Configuration**: Create a `.env` file with your secrets (API keys, passwords).
2.  **Launch**: Run `sudo docker compose up -d` to start the services.
3.  **HPC Job Submission**: Use the provided Slurm scripts to submit your model inference job to the HPC nodes.

## Repository

For the full tutorial, example `.env` files, and Slurm submission scripts, please refer to the source repository:

[**drai-inn/llm-nesi-example**](https://github.com/drai-inn/llm-nesi-example)

# Contributing to UoA Research AI GPU Platform Docs

Thank you for your interest in contributing! This guide will help you get started.

## Development Setup

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/drai-inn/uoa-ai-gpu-docs.git
    cd uoa-ai-gpu-docs
    ```

2.  **Create and activate a virtual environment:**
    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the local server:**
    ```bash
    mkdocs serve
    ```
    The site will be available at `http://127.0.0.1:8000`.

## Workflow

1.  **Create a branch:** Always work on a new branch for your changes.
    ```bash
    git checkout -b my-new-feature
    ```

2.  **Make changes:** Edit the documentation in the `docs/` directory.

3.  **Verify locally:** Ensure `mkdocs serve` is running and check your changes in the browser.

4.  **Commit:** Use granular, descriptive commit messages.
    ```bash
    git commit -m "docs: add section on GPU scheduling"
    ```

5.  **Push and PR:** Push your branch and open a Pull Request against `main`.

## Deployment

Deployment is **automated**.
- When a PR is merged into `main`, a GitHub Action automatically builds the site and deploys it to the `gh-pages` branch.
- **Do not** run `mkdocs gh-deploy` manually unless you are fixing a deployment emergency.

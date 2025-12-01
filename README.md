# UoA Research AI GPU Platform Docs

[![Deploy docs](https://github.com/drai-inn/uoa-ai-gpu-docs/actions/workflows/docs.yml/badge.svg)](https://github.com/drai-inn/uoa-ai-gpu-docs/actions/workflows/docs.yml)


Welcome to the official documentation repository for the University of Auckland Research AI GPU Platform. This site provides comprehensive guides, reference materials, and tutorials for researchers using our GPU resources.

**[🚀 View the Live Documentation](https://drai-inn.github.io/uoa-ai-gpu-docs/)**

## Community & Contributing

This documentation is built by the community, for the community.

*   **✏️ Edit this page**: Click the pencil icon on any page to fix typos or suggest changes.
*   **🤝 Contributing Guide**: Read our [Contribution Guidelines](CONTRIBUTING.md) for more details.
*   **📜 Code of Conduct**: We are committed to a welcoming environment. Please read our [Code of Conduct](CODE_OF_CONDUCT.md).

We welcome contributions from everyone—researchers, students, and engineers!

## Development Setup

To set up the development environment locally:

1.  **Create a virtual environment:**
    ```bash
    python3 -m venv .venv
    ```

2.  **Activate the virtual environment:**
    ```bash
    source .venv/bin/activate
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```

4.  **Run the development server:**
    ```bash
    zensical serve
    ```

The site will be available at `http://127.0.0.1:8000`.

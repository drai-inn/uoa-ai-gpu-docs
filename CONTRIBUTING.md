# Contributing to UoA Research AI GPU Platform Docs

👋 **Welcome!** We are thrilled that you're interested in contributing.

This documentation is a community effort. Whether you're a researcher, student, or engineer, your insights help make this platform better for everyone. You don't need to be an expert programmer to contribute!

## Ways to Contribute

There are many ways to help:

*   **📝 Edit a Page**: Spot a typo or unclear explanation? Click the **pencil icon** (✏️) at the top of any page to edit it directly on GitHub.
*   **🐛 Report an Issue**: Found a bug or missing information? [Open an issue](https://github.com/drai-inn/uoa-ai-gpu-docs/issues) to let us know.
*   **💡 Suggest a Guide**: Have a workflow that works well for you? We'd love to host your guide or tutorial.
*   **💬 Join the Discussion**: Have questions or ideas? Check out our [GitHub Discussions](https://github.com/drai-inn/uoa-ai-gpu-docs/discussions) (if enabled) or contact the team.

## Style Guide

To keep our docs consistent and friendly:

*   **Tone**: Professional but accessible. Write as if you're explaining to a colleague.
*   **Formatting**: We use standard Markdown.
    *   Use `code blocks` for commands and file paths.
    *   Use **bold** for UI elements or key terms.
*   **Images**: Keep screenshots focused and relevant.
*   **Icons**: We use Lucide icons (e.g., `lucide/server`).

## Development Setup

If you want to preview changes locally or make significant updates, here's how to set up your environment:

1.  **Clone the repository:**
    ```bash
    git clone https://github.com/drai-inn/uoa-ai-gpu-docs.git
    cd uoa-ai-gpu-docs
    ```

2.  **Create a virtual environment:**
    ```bash
    python3 -m venv .venv
    source .venv/bin/activate
    ```

3.  **Install dependencies:**
    ```bash
    pip install -r requirements.txt
    ```
    *Note: This installs `zensical`.*

4.  **Run the local server:**
    ```bash
    zensical serve
    ```
    The site will be available at `http://127.0.0.1:8000`. Changes will auto-reload.

## Submitting Changes

1.  **Create a Branch**: `git checkout -b my-new-guide`
2.  **Commit**: `git commit -m "docs: add guide on pytorch"`
3.  **Push**: `git push origin my-new-guide`
4.  **Open a Pull Request**: Go to GitHub and open a PR against `main`.
5.  **Review Preview**: A comment will be automatically posted on your PR with a link to a live preview of your changes (e.g., `https://drai-inn.github.io/uoa-ai-gpu-docs/previews/pr-123/`). Use this to verify your changes look correct. Note that this preview is temporary and will be deleted when the PR is closed.

## Community Standards

We are committed to providing a friendly, safe, and welcoming environment for all. Please read and uphold our [Code of Conduct](CODE_OF_CONDUCT.md).

---

**Questions?** Reach out via [Issues](https://github.com/drai-inn/uoa-ai-gpu-docs/issues).

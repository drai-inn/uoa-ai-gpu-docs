---
trigger: always_on
---

## Workflow
- **Updates**: When updating documentation, ensure the local server (`mkdocs serve`) is verified.
- **Commits**: Maintain a granular, frequent commit workflow. Commit small, logical units of work with clear, descriptive messages. Avoid large, monolithic commits.
- **Deployment**: Deployment is automated via GitHub Actions on push to `main`. Do not manually deploy.
- **Contribution**: Follow the guidelines in `CONTRIBUTING.md`.

---
trigger: always_on
---

## Workflow
- **Dependency Management**: When managing versions and releases always check the source repository for current releases and ensure you're not bound by your own training data and things that have happened since.
- **Updates**: When updating documentation, ensure the local server (`mkdocs serve`) is verified.
- **Commits**: Maintain a granular, frequent commit workflow. Commit small, logical units of work with clear, descriptive messages. Avoid large, monolithic commits.
- **Deployment**: Deployment is automated via GitHub Actions on push to `main`. Do not manually deploy.
- **Contribution**: Follow the guidelines in `CONTRIBUTING.md`.
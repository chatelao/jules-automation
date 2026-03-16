# Jules Automation

This repository contains automation scripts and workflows to streamline the development process with Google Jules.

## Automation Rules (from GEMINI.md)

1. **Issue Labeling:** Every new issue is automatically labeled with "jules".
2. **Project Management:** Every issue with the "jules" label is added to the [project board](https://github.com/users/chatelao/projects/14).
3. **Roadmap Management:**
   - A `ROADMAP.md` file is maintained with checkboxes for tasks.
   - New tasks (from issues) are inserted at the **top** of the list.
   - Agents should execute tasks from **bottom to top**.
   - A timestamp of completion is added to the end of each task when it's done (issue is closed).

## Setup

To enable the project management automation, you need to add a Personal Access Token (PAT) with `repo` and `project` scopes to your repository secrets:

1. Create a PAT at [github.com/settings/tokens](https://github.com/settings/tokens).
2. Go to your repository settings > Secrets and variables > Actions.
3. Add a new repository secret named `ADD_TO_PROJECT_PAT` with your PAT as the value.

## Files

- `scripts/roadmap_manager.py`: Python script to manage `ROADMAP.md`.
- `.github/workflows/jules-automation.yml`: GitHub Action workflow for issue automation.
- `ROADMAP.md`: The automated roadmap of tasks.
- `AGENTS.md`: Instructions for AI agents working on this repo.

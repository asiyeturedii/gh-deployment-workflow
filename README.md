# gh-deployment-workflow

A simple static website automatically deployed to GitHub Pages using GitHub Actions.

🌐 **Live site:** `https://<username>.github.io/gh-deployment-workflow/`

## What it does

Every push to the `main` branch that modifies `index.html` triggers a GitHub Actions workflow that automatically deploys the site to GitHub Pages.

## Project structure

```
├── index.html              # Static website
├── README.md               # This file
└── .github/
    └── workflows/
        └── deploy.yml      # GitHub Actions deployment workflow
```

## How it works

1. A change is pushed to `main` that includes `index.html`
2. The `deploy.yml` workflow is triggered
3. GitHub Actions checks out the repo, packages the files, and deploys to GitHub Pages
4. The live site is updated automatically

## Workflow trigger

The workflow only runs when `index.html` is changed — other file changes (like edits to this README) do **not** trigger a deployment.

## Concepts covered

- GitHub Actions
- GitHub Pages
- Continuous Integration / Continuous Deployment (CI/CD)
- Workflow triggers with path filters

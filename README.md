# 🚀 CI/CD Templates: New Feature Branch Workflow

[![Maintained by Gitdigital](https://img.shields.io/badge/Maintained%20by-Gitdigital-blueviolet?style=for-the-badge)](https://github.com/Gitdigital-products)
[![GitHub Workflow Status](https://img.shields.io/github/actions/workflow/status/Gitdigital-products/ci-cd-templates--New-Feature-Branch/feature-validation.yml?branch=main&style=for-the-badge&logo=github)](https://github.com/Gitdigital-products/ci-cd-templates--New-Feature-Branch/actions)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)
[![PRs Welcome](https://img.shields.io/badge/PRs-welcome-brightgreen.svg?style=for-the-badge)](http://makeapullrequest.com)
[![GitHub last commit](https://img.shields.io/github/last-commit/Gitdigital-products/ci-cd-templates--New-Feature-Branch?style=for-the-badge)](https://github.com/Gitdigital-products/ci-cd-templates--New-Feature-Branch/commits/main)

---

## 📖 Overview
This repository provides standardized **CI/CD templates** specifically designed for a **Feature Branch Workflow**. It ensures that every new feature is validated, linted, and tested automatically before it ever reaches the main codebase.

### Key Benefits:
* **Automated Quality Gates**: Prevents broken code from merging.
* **Standardized PRs**: Consistent communication across the team.
* **Security First**: Pre-configured `.gitignore` to prevent secret leakage.

---

## 🛠️ Included Components

| Component | Purpose | Location |
| :--- | :--- | :--- |
| **Validation Workflow** | Runs tests/linting on every `feature/*` push. | `.github/workflows/` |
| **PR Template** | Standardizes the review process and checklist. | `.github/pull_request_template.md` |
| **Safe Config** | Universal `.gitignore` for Node/Python/DevOps. | `/.gitignore` |

---

## 🚀 How to Use These Templates

### 1. Integration
Copy the `.github` folder and `.gitignore` file into your project's root directory:
```bash
cp -r .github /path/to/your/project/
cp .gitignore /path/to/your/project/


# ci-cd-templates
ci-cd-templates Reusable GitHub Actions and GitLab pipeline templates.
# CI/CD Templates

Reusable GitHub Actions workflows for the **Gitdigital Products** ecosystem.  
Keep your pipelines consistent, clean, and fast.

## 🚀 Included Workflows
- `rust-ci.yml` → Build + test Rust projects
- `docker-ci.yml` → Build + push Docker images
- `node-ci.yml` → Test Node.js apps

## 🛠️ Usage
In any repo, reference these templates in your `.github/workflows` directory.

Example:
```yaml
name: Reuse Rust CI
on: [push]

jobs:
  call-template:
    uses: Gitdigital-products/ci-cd-templates/.github/workflows/rust-ci.yml@main

# 🛠️ Kubernetes Helm Chart Template

Welcome to the Kubernetes Helm Chart Template repository! This repository provides a template for deploying Kubernetes applications using Helm charts, Docker, and GitHub Actions for CI/CD. It integrates with ArgoCD for GitOps-style deployments, allowing automated application updates and synchronization with the cluster.

## 📁 Repository Structure
```text
.
├── charts/                        # Helm charts for Kubernetes resources
│   └── my-app/                    # Example Helm chart for the application
│       ├── Chart.yaml             # Helm chart metadata
│       ├── values.yaml            # Default values for the chart (image, replicas, etc.)
│       ├── charts/                # Subcharts (if any dependencies are used)
│       ├── templates/             # Kubernetes resource templates (Deployment, Service, etc.)
│       │   ├── deployment.yaml    # Application deployment template
│       │   ├── service.yaml       # Service for exposing the app
│       │   └── ingress.yaml       # Optional ingress resource
│       └── README.md              # Documentation for using the Helm chart
├── .github/                       # GitHub-specific configurations
│   └── workflows/                 # GitHub Actions workflows for CI/CD
├── Dockerfile                     # Dockerfile for building the app container
├── README.md                      # Project documentation
```

## ⚙️ Semantic Commit Messages
This project uses [Semantic Commit Messages](https://www.conventionalcommits.org/) to ensure meaningful and consistent commit history. The format is as follows:

```php
<type>(<scope>): <subject>
```

### Types

- `feat`: A new feature (e.g., `feat: add login functionality`).
- `fix`: A bug fix (e.g., `fix: resolve login button issue`).
- `docs`: Documentation changes (e.g., `docs: update API documentation`).
- `style`: Code style changes (formatting, missing semi-colons, etc.) without changing logic (e.g., `style: fix indentation`).
- `refactor`: Code changes that neither fix a bug nor add a feature (e.g., `refactor: update user controller structure`).
- `test`: Adding or updating tests (e.g., `test: add unit tests for login service`).
- `chore`: Changes to build process, auxiliary tools, or libraries (e.g., `chore: update dependencies`).

### Scope

Optional: The part of the codebase affected by the change (e.g., `feat(auth): add OAuth support`)

### Subject

A brief description of the change, using the imperative mood (e.g., `fix: resolve issue with user authentication`).

## 🚀 Semantic Release

This project is configured with [Semantic Release](https://semantic-release.gitbook.io/semantic-release) to automate the release process based on your commit messages.

### How It Works

1. Analyze commits: Semantic Release inspects commit messages to determine the type of changes in the codebase.
2. Generate release version: Based on the commit type, it will automatically bump the version following semantic versioning:
- fix → Patch release (e.g., 1.0.1)
- feat → Minor release (e.g., 1.1.0)
- BREAKING CHANGE → Major release (e.g., 2.0.0)
3. Create release notes: It generates a changelog from the commit messages and includes it in the release.
4. Publish: It automatically publishes the new version to the repository (and any other configured registries, e.g., npm).

## 🤝 Contributing

If you find any issues or have suggestions for improving this template repository, please feel free to open an issue or submit a pull request. Contributions are always welcome!

## 📜 License

This repository is licensed under the MIT License. See the [LICENSE](LICENSE) file for more information.

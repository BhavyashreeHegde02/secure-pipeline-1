# Secure Git Operations and Gitflow Branching Strategy

A hands-on DevOps project demonstrating secure Git practices, Gitflow branching, automated testing, CI workflows, and application security checks using GitHub Actions.

## Project Overview

This project demonstrates how a structured Git workflow can improve collaboration, code quality, and security in software development.

It implements a Gitflow branching strategy with feature development, release management, and hotfix handling. GitHub Actions automates testing and security checks whenever code changes are pushed or pull requests are created.

## Objectives

- Implement a structured Gitflow branching strategy.
- Practice feature, release, and hotfix workflows.
- Manage code integration using Pull Requests.
- Automate application testing using Pytest.
- Integrate security checks into a GitHub Actions workflow.
- Manage releases using Git tags.

## Technologies Used

| Technology | Purpose |
|---|---|
| Git | Version control |
| GitHub | Repository and collaboration |
| GitHub Actions | CI automation |
| Python | Application development |
| Pytest | Automated testing |
| Bandit | Python security analysis |
| pip-audit | Dependency vulnerability auditing |
| Secret scanning | Detect potential exposed secrets |

## Gitflow Branching Strategy

The project follows a Gitflow-inspired branching model.

- `main` – Contains the stable release.
- `develop` – Integration branch for development.
- `feature/*` – Used to develop new functionality.
- `release/*` – Used to prepare a release.
- `hotfix/*` – Used to fix critical issues in the released application.

### Workflow

1. Create feature branches from `develop`.
2. Implement and test new functionality.
3. Open Pull Requests to merge changes.
4. Create release branches to prepare versions.
5. Merge releases into `main` and back into `develop`.
6. Create hotfix branches from `main` for critical bug fixes.
7. Merge hotfixes into both `main` and `develop`.

## Implemented Features

### 1. Order Total Calculation

Implemented an order calculation function with input validation and tax calculation.

### 2. Automated Testing

Used Pytest to validate application functionality, including:

- Order total calculation.
- Input validation.
- Tax calculation.
- Zero-quantity regression testing.

### 3. CI and Security Checks

Configured a GitHub Actions workflow named `security-checks` to automate:

- Pytest execution.
- Secret scanning.
- Bandit security analysis.
- Dependency vulnerability auditing using pip-audit.

## Release Management

| Version | Description |
|---|---|
| v1.0.0 | Initial secure Gitflow release with tax calculation |
| v1.0.1 | Hotfix to reject zero-quantity order calculations |

## Testing Results

The final application test suite completed successfully:

- `main` branch: 5 tests passed.
- `develop` branch: 5 tests passed.
- GitHub Actions security workflow: Successful.

## Project Structure

```text
secure-pipeline-1/
│
├── .github/
│   └── workflows/
│       └── ci.yml
│
├── .githooks/
├── scripts/
│   └── secret_scan.py
│
├── app.py
├── test_app.py
├── requirements.txt
├── VERSION
├── CHANGELOG.md
└── README.md
```

## Run the Project Locally

Clone the repository:

```bash
git clone https://github.com/BhavyashreeHegde02/secure-pipeline-1.git
cd secure-pipeline-1
```

Create a virtual environment:

```bash
python -m venv .venv
```

Activate it on Windows:

```powershell
.\.venv\Scripts\Activate.ps1
```

Install dependencies:

```bash
pip install -r requirements.txt
```

Run automated tests:

```bash
python -m pytest -q
```

## Key Learnings

Through this hands-on implementation, I explored:

- Secure Git operations and branching strategies.
- Pull Request-based collaboration.
- CI automation using GitHub Actions.
- Automated testing and regression testing.
- Application security and dependency auditing.
- Release management and hotfix workflows.

## Repository

GitHub: https://github.com/BhavyashreeHegde02/secure-pipeline-1

---

**Learning by building, testing, and improving.**

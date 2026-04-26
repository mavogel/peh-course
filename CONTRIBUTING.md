# Contributing to Building an AI-Powered IDP from Scratch

Thank you for your interest in contributing to this course repository! This project accompanies the Packt course *Building an AI-Powered Internal Developer Platform from Scratch* and the books *The Platform Engineer's Handbook* (Packt) and *Effective Platform Engineering* (Manning).

Contributions that improve the code, fix bugs, clarify documentation, or add useful examples are welcome and appreciated.

## How to Contribute

### 1. Fork the Repository

Navigate to [github.com/achankra/peh-course](https://github.com/achankra/peh-course) and click **Fork** in the top-right corner. This creates your own copy of the repository under your GitHub account.

### 2. Clone Your Fork

```bash
git clone https://github.com/<your-username>/peh-course.git
cd peh-course
```

### 3. Create a Feature Branch

Always work on a dedicated branch, never directly on `main`.

```bash
git checkout -b feat/your-descriptive-branch-name
```

Use a clear prefix that signals the type of change:

| Prefix | Use when |
|--------|----------|
| `feat/` | Adding a new feature, demo, or exercise |
| `fix/` | Fixing a bug in scripts or configurations |
| `docs/` | Improving documentation, README, or comments |
| `chore/` | Updating dependencies, tooling, or dev setup |
| `refactor/` | Restructuring code without changing behavior |

### 4. Make Your Changes

The repository is organized by session (Session1 through Session9). Each session folder contains the relevant code, YAML configurations, and Python scripts for that part of the course.

A few guidelines:

- **Test locally.** Every script in this repo is designed to run on a local Kind cluster with no cloud dependencies. Verify your changes work end to end before submitting.
- **Follow existing patterns.** Match the coding style, naming conventions, and file structure already in use. Python scripts use standard library where possible; YAML files follow Kubernetes conventions.
- **Keep changes focused.** One PR should address one concern. A PR that fixes a bug in Session 3 and adds a new feature to Session 7 should be two separate PRs.
- **Update documentation.** If your change affects how a demo or exercise works, update the relevant README or inline comments.
- **Use the devcontainer.** The repo includes a devcontainer configuration for a consistent development environment. Using it ensures your setup matches what other contributors and learners use.

### 5. Commit Your Changes

Write clear, descriptive commit messages. Use [Conventional Commits](https://www.conventionalcommits.org/) format:

```bash
git add <specific-files>
git commit -m "feat: add network policy example to Session 3"
```

Examples of good commit messages:

- `fix: correct OTel collector port in Session 6 config`
- `docs: clarify Velero backup restore steps in Session 7 README`
- `feat: add devcontainer setup`
- `chore: update Python dependencies for chaos runner`

### 6. Push and Open a Pull Request

```bash
git push origin feat/your-descriptive-branch-name
```

Then go to your fork on GitHub and click **Compare & pull request**. In your PR description:

- **Summarize what changed and why.** A reviewer should understand the motivation without reading every line of diff.
- **Reference the session number** (e.g., "This fixes the alert correlator in Session 6").
- **Include testing steps.** Describe how you verified the change works (e.g., "Ran `chaos-runner.py` against a Kind cluster with 3 pods and confirmed latency injection").
- **Add screenshots or terminal output** if the change is visual or produces notable output.

### 7. Respond to Review Feedback

A maintainer will review your PR. Be open to suggestions and iterate. Once approved, your PR will be merged into `main`.

## What to Contribute

Here are some ideas for valuable contributions:

- **Bug fixes** in Python scripts or YAML configurations
- **Improved error handling** in demo scripts (e.g., better messages when a dependency is missing)
- **Additional examples** that extend a session's concepts (e.g., a new chaos experiment, an alternative golden path)
- **Documentation improvements** such as clearer setup instructions, troubleshooting tips, or annotated code comments
- **DevEx improvements** like devcontainer enhancements, Makefile targets, or pre-commit hooks
- **Compatibility fixes** for different operating systems or Kubernetes versions

## Code of Conduct

Be respectful, constructive, and collaborative. This is a learning-focused repository. Contributions from all experience levels are welcome. If you are new to platform engineering or open source, don't hesitate to open an issue or a draft PR to ask questions.

## Reporting Issues

If you find a bug or have a suggestion but don't want to submit a PR, open a [GitHub Issue](https://github.com/achankra/peh-course/issues) with:

- Which session and file is affected
- What you expected vs. what happened
- Steps to reproduce (if it's a bug)
- Your environment (OS, Python version, Kind version)

---

## Contributors

Thank you to everyone who has contributed to making this course better. Every fix, improvement, and idea matters.

| Contributor | Contribution |
|-------------|-------------|
| **Manuel Vogel** ([@mavogel](https://github.com/mavogel)) | Added devcontainer setup ([PR #1](https://github.com/achankra/peh-course/pull/1)) -- enabling a consistent, reproducible development environment so learners can run `pip install` and session demos without local dependency conflicts. Tested through Session 2. |

*Want to see your name here? Submit a PR!*

---

## License

By contributing, you agree that your contributions will be made available under the same terms as the rest of the repository.

## Questions?

Reach out to [Ajay Chankramath](https://github.com/achankra) via GitHub Issues or at [platformetrics.com](https://platformetrics.com).

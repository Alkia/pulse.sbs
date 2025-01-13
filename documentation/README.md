# Docunentation


## Directory structure

```
├── README.md
├── api
├── backend_admin
├── db
├── documentation
│   └── directory_structure.md
├── files
│   ├── logs
│   └── transcripts
├── frontend
├── iot
└── survey
```

## Git strategy with external project

To effectively manage a project based on the existing GitHub repository https://github.com/surveyjs/surveyjs-php.git while allowing for ongoing changes and evolution of both your modifications and the original project, consider the following best practices for using Git:
1. Forking the Repository
Fork the Repository: Create a personal copy of the original repository on GitHub. This allows you to make changes without affecting the main project.
Clone Your Fork: Clone your forked repository to your local machine using:
bash
git clone https://github.com/yourusername/surveyjs-php.git
2. Setting Up Remote Tracking
Add Upstream Remote: Set the original repository as an upstream remote to keep track of changes made in the original project.
bash
git remote add upstream https://github.com/surveyjs/surveyjs-php.git
3. Branching Strategy
Create Feature Branches: For each new feature or change, create a new branch from the main (or master) branch. This keeps your changes organized and isolated.
bash
git checkout -b feature/pulse-survey-feature
4. Regularly Syncing with Upstream
Fetch Changes from Upstream: Regularly pull changes from the original repository to keep your fork up to date.
bash
git fetch upstream
git checkout main
git merge upstream/main
Rebase Your Feature Branch: Before merging your changes back to main, rebase your feature branch onto the latest main to resolve any conflicts early.
bash
git checkout feature/pulse-survey-feature
git rebase main
5. Committing Changes
Commit Often with Clear Messages: Make small, logical commits with descriptive messages that explain what each change does.
bash
git commit -m "Add new styling options for survey forms"
6. Pushing Changes and Pull Requests
Push Changes to Your Fork: After committing your changes, push them to your GitHub fork.
bash
git push origin feature/my-new-feature
Create Pull Requests: If you want to contribute back to the original repository, create a pull request from your feature branch to the original repository's main branch.
7. Documentation and Version Control
Document Changes: Maintain a CHANGELOG file in your repository to document what has changed with each version.
Version Control: Consider using semantic versioning (e.g., v1.0.0) for releases of your modified project.
Summary of Best Practices:
Fork and Clone: Start by forking and cloning the repository.
Set Up Remotes: Keep track of both your fork and the original repo.
Branching Strategy: Use branches for features or fixes.
Sync Regularly: Keep your fork updated with upstream changes.
Commit Wisely: Make clear, frequent commits.
Push and Pull Request: Share your contributions via pull requests.
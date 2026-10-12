# Git Repository Collaboration Lab

A small sample website for demonstrating Git branching, commits, pushes, pull requests, review, and merging.

## Requirements
- Git installed
- A GitHub account
- A web browser
- Optional: VS Code

## 1. Run the website
Open `index.html` in your browser. It is a static website, so no server is required.

## 2. Create a Git repository
Open a terminal in this folder and run:

```bash
git init
git branch -M main
git add .
git commit -m "Initial project setup"
```

Create an empty repository on GitHub named `git-collaboration-lab`. Then connect it (replace USERNAME):

```bash
git remote add origin https://github.com/USERNAME/git-collaboration-lab.git
git push -u origin main
```

If Git asks you to configure your identity, use your own details:

```bash
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
```

## 3. Demonstrate a feature branch
Create a branch for the introduction feature:

```bash
git switch -c feature/introduction
```

Edit `src/content.js` and change the introduction text. Then run:

```bash
git status
git add .
git commit -m "Update project introduction"
git push -u origin feature/introduction
```

## 4. Open a pull request
1. Open your GitHub repository in the browser.
2. Choose **Compare & pull request** for `feature/introduction` (or open **Pull requests > New pull request**).
3. Set the base branch to `main` and compare branch to `feature/introduction`.
4. Add a title and description, then create the pull request.
5. Review the **Files changed** tab. If working alone, explain that a teammate would normally review it.
6. Click **Merge pull request**, then confirm the merge.

## 5. Update the local main branch
```bash
git switch main
git pull origin main
```

## Expected result
- `main` contains the initial project.
- `feature/introduction` contains the proposed introduction change.
- GitHub shows a pull request with the changed file.
- After merging, the updated introduction is present in `main`.

## Important
A pull request is created on GitHub; Git commands alone do not create one. Do not claim a pull request was created or merged until you have performed those steps in your own GitHub repository.

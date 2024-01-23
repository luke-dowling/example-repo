# GitHub Team Collaboration Guide

This guide will walk you through the process of working in a team where one person owns the repository, and all contributors create feature branches before pushing changes to the main branch. Additionally, we'll cover how to handle conflicts that may arise during the development process.

## Table of Contents

1. [Clone the Repository](#1-clone-the-repository)
2. [Create a Feature Branch](#2-create-a-feature-branch)
3. [Make Changes and Commit](#3-make-changes-and-commit)
4. [Push Changes to GitHub](#4-push-changes-to-github)
5. [Create a Pull Request](#5-create-a-pull-request)
6. [Review and Merge](#6-review-and-merge)
7. [Handling Conflicts](#7-handling-conflicts)

---

### 1. Clone the Repository

First, clone the repository to your local machine:

```bash
git clone https://github.com/username/repository.git
```

Replace `username/repository` with the actual username and repository name.

### 2. Create a Feature Branch

Before making changes, create a new branch for your feature:

```bash
git switch -c feature-branch
```

Replace `feature-branch` with a descriptive name for your feature.

### 3. Make Changes and Commit

Make your changes to the code, add and commit them:

```bash
git add .
git commit -m "Description of changes"
```

### 4. Push Changes to GitHub

Push your feature branch to GitHub:

```bash
git push origin feature-branch
```

### 5. Create a Pull Request

On the GitHub repository page, create a pull request from your feature branch to the main branch. Provide details about the changes made.

### 6. Review and Merge

The repository owner or a designated reviewer will review your pull request. If approved, they will merge it into the main branch.

### 7. Handling Conflicts

#### 7.1 Pull Latest Changes

Before creating a pull request or merging, ensure your local main branch is up-to-date:

```bash
git switch main
git pull origin main
```

#### 7.2 Merge Conflicts

If there are conflicts during the merge, Git will mark them in your files. Open the conflicted files, resolve the conflicts, and then add and commit the changes.

#### 7.3 Push Changes

Push the resolved changes to GitHub:

```bash
git push origin main
```

## 8. Handling Conflicts on GitHub

Handling conflicts on GitHub involves resolving conflicting changes between branches, typically during the process of merging a pull request. Here's a more detailed explanation of handling conflicts directly on GitHub:

### 1. **Create a Pull Request**

After pushing your feature branch, create a pull request on the GitHub repository.

### 2. **Review Changes**

Allow time for others to review your changes and address any feedback.

### 3. **Conflict Detection**

If there are conflicting changes between your branch and the main branch, GitHub will notify you. This happens when someone else has made changes to the same files you modified.

### 4. **Resolve Conflicts**

- **Locate Conflicted Files:**
  GitHub will mark the conflicted files in your pull request. Navigate to the "Files changed" tab to see the conflicting changes.
- **Initiate Conflict Resolution:**
  Click the "Resolve conflicts" button. This will take you to a file editor where you can manually resolve conflicts.
- **Resolve Conflicts:**
  Manually edit the conflicting sections in the affected files. Remove the conflict markers (`<<<<<<<`, `=======`, `>>>>>>>`) and keep the desired changes.
- **Mark as Resolved:**
  Once conflicts are resolved, mark the files as resolved.
- **Commit Changes:**
  Commit the changes directly on the branch. There's no need to create a new commit for conflict resolution.

### 5. **Complete Pull Request**

- **Rebase if Necessary:**
  If there were conflicts, you might need to rebase your branch on the latest main branch to ensure a clean history.
- **Merge Pull Request:**
  Complete the pull request. If you resolved conflicts locally and pushed the changes, GitHub will recognize the resolution.

### 6. **Continuous Integration (Optional)**

If the repository has continuous integration (CI) checks, wait for the checks to pass. CI systems often run tests to ensure the changes didn't introduce errors.

### 7. **Delete Feature Branch (Optional)**

After merging, you can choose to delete the feature branch on GitHub.

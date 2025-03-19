---
title: Using source control tool in vscode 
sidebar_label: Using source control tool in vscode 
description: A brief description of what the post covers
---

# Using Source Control in VS Code

Visual Studio Code (VS Code) provides built-in support for Git, making it easy to manage source control directly from the editor. Whether you’re working on a solo project or collaborating with a team, VS Code streamlines Git workflows with an intuitive UI and powerful features.

### Setting Up Git in VS Code

#### 1. Install Git

Before using Git in VS Code, ensure that Git is installed on your system:

Download and install Git from the official site: Git Downloads

Verify installation by running:

```git --version```

#### 2. Configure Git in VS Code

After installing Git, set up your identity:

```
git config --global user.name "Your Name"
git config --global user.email "your.email@example.com"
```

### Using Git in VS Code

![VScode](/img/1-7cfd2283.png)

#### 1. Open a Git Repository

Open VS Code and navigate to your project folder.

If your project is already under Git, VS Code will automatically detect the repository.

If not, initialize a new repository by clicking Source Control (left sidebar) and selecting Initialize Repository.

#### 2. Cloning a Repository

To clone a remote repository:

Open VS Code.

Press `Ctrl + Shift + P` and search for `Git: Clone.`

Enter the repository URL and select a local folder.

Open the cloned project in VS Code.

#### 3. Checking Git Status

You can check the current status of your repository:

Open the Source Control panel to see modified, staged, and untracked files.

Run the following command in the terminal:

`git status`

#### 4. Staging and Committing Changes

![VScode](/img/2-7cfd2283.png)

Click the + icon next to a file in the Source Control panel to stage changes.

To commit, enter a message in the text box and press Ctrl + Enter.

Alternatively, use the terminal:

```
git add .
git commit -m "Your commit message"
```

#### 5. Pushing Changes to a Remote Repository

After committing, push changes to a remote repository:

`git push origin main`

If no remote is set up:

```
git remote add origin <repository-url>
git push -u origin main
```

or you can do 
![commitandpush](/img/3-7cfd2283.png)

#### 6. Pulling Changes

To fetch the latest updates from a remote repository:

Click the Sync Changes button in the Source Control panel.

Use the terminal:

```git pull origin main```

#### 7. Branching in VS Code

To create and switch branches:

Click the branch icon in the lower-left corner.

Select Create New Branch, enter a name, and switch to it.

Or, use the terminal:

```
git branch new-branch
git checkout new-branch
```
#### 8. Merging Branches

To merge changes from another branch:

Switch to the target branch (main or develop).

Click the Source Control panel and choose Merge Branch.

Use the terminal:

```
git merge branch-name
```

## Conclusion

VS Code makes Git workflows *simple* with an ***intuitive UI and robust integration.*** Whether you're working solo or in a team, leveraging VS Code’s Git features will *streamline* your version control process and *improve collaboration.*
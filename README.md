# learn-git
Learn git


# Git Flow

## Creating a GitHub repository

1. Start by creating a Git repository:
  - you can do this on GitHub by clicking the [+ button](https://github.com/new) at the top right
  - Select `Initialise this repository with a README`
  - Click `Add .gitignore` and select your coding environment (Node is good if you use npm)
  - Optional: Choose a license
- Copy the URL of the repository

## Command Line
1. cd into a directory such as `git`
  ```bash
  mkdir git && cd $_
  ```

- git clone from the git URL
  ```bash
  git clone https://github.com/macintoshhelper/learn-git
  # https://github.com/username/repository-name
  ```
  You have now downloaded the git repository
  You are in the master branch, which should only contain stable, deployable code.

- Create and checkout to a new branch
  ```bash
  # Create and checkout to new branch
  git checkout -b branch-name # where branch-name may be your feature name

  # Create new branch
  git branch branch-name

  # Checkout to existing branch
  git checkout branch-name
  ```

- Write some code and add + commit it
  ```bash
  # Check what files have changed and need to be staged
  git status
  
  # Add a file(s) to be committed
  git add fileName.js fileName2.js <...>
  
  # Commit / create a snapshot of the code that you can revert to
  git commit -m 'Description of the code you are committing'
  ```
  
- Merge with master to update any changes since you wrote the code
  ```bash
  git checkout master
  git pull origin master
  git checkout branch-name
  git merge master
  ```
  
- Push code up to git server
  ```bash
  git push origin branch-name
  ```

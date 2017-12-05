# Contributor's Guide

GDG Kolachi is built in the open using the [hoverboard project](https://github.com/gdg-x/hoverboard), and the GDG Kolachi team eagerly encourages any and all forms of community contribution. Follow the instructions below to install and run the Project locally in less than 15 minutes. please follow these guidelines:

1. Find an issue that needs assistance by looking in the [issues](https://github.com/GDGKolachi/gdgkolachi.com/issues) directory of this repo.

1. Let us know you are working on it by posting a comment on the issue.

1. Follow the below mentioned Guidelines to start working on the issue.

____________________________________________________________________

## Guidelines

- [Prerequisites](#prerequisites)
- [Forking the Project](#forking-the-project)
- [Create A Branch](#create-a-branch)
- [Running the App](#running-the-app)
- [Make Changes](#make-changes)
- [Pull Request](#pull-request)
- [Any Questions](#any-questions)

## Prerequisites

1.  Install [Node.js](https://nodejs.org/) (`node`) version 4 or above.
    Node.js includes Node Package Manager (`npm`) by default. The Hoverboard
    uses `npm` for Polymer CLI.

1.  Verify that you're running `node` version 4 or above and `npm`
    version 2.15 or above.

        node -v
        v4.4.7

        npm -v
        2.15.8
  
  1. Make sure you have [Git](https://git-scm.com/) Installed in your system

## Forking the Project

### Fork this Repo

1.  [Fork](https://github.com/GDGKolachi/gdgkolachi.com/fork) this repository


### Clone it locally

1.  Open a Terminal / Command Line / Bash Shell and navigate to a project directory where you want to copy this project.
        
        cd yourProjectDirectory

1.  Run below command in your terminal.

        git clone https://github.com/yourUsername/gdgkolachi.com.git
    (make sure to replace `yourUsername` with your GitHub Username), This will download the entire GDG Kolachi repo to your projects directory.

### Install Dependencies

1. `cd` into the base directory of your GDG Kolachi project.

1.  Install the application dependencies.

        npm install

### Setup Your Upstream

1. Add a remote to the official GDG Kolachi repo:

        git remote add upstream https://github.com/GDGKolachi/gdgkolachi.com.git
    
    Congratulations, you now have a local copy of the GDG Kolachi repo!

### Maintaining Your Fork

Now that you have a copy of your fork, there is work you will need to do to keep it current.

#### Rebasing from Upstream

Do this prior to every time you create a branch for a PR:

Make sure you are on the `hoverboard-v2` branch

        git status
        On branch hoverboard-v2
        Your branch is up-to-date with 'origin/hoverboard-v2'.

If your aren't on `hoverboard-v2`, resolve outstanding files / commits and checkout the `hoverboard-v2` branch

        git checkout hoverboard-v2

Do a pull with rebase against upstream

        git pull --rebase upstream hoverboard-v2

This will pull down all of the changes to the official `hoverboard-v2` branch, without making an additional commit in your local repo.

(Optional) Force push your updated `hoverboard-v2` branch to your GitHub fork

        git push origin hoverboard-v2 --force

This will overwrite the `hoverboard-v2` branch of your fork.


## Create A Branch

Everytime before you start working, you will need to create a separate branch specific to the issue / feature you're working on. You will push your work to this branch.

### Naming Your Branch

Name the branch something like `fix/xxx` or `feature/xxx` where `xxx` is a short description of the changes or feature you are attempting to add. For example `fix/event-image` would be a branch where you fix something specific to images on events page or card.

### Adding Your Branch

To create a branch on your local machine (and switch to this branch):

      git checkout -b [name_of_your_new_branch]

and to push to GitHub:

      git push origin [name_of_your_new_branch]

  If you need more help with branching, take a look at [this](https://github.com/Kunena/Kunena-Forum/wiki/Create-a-new-branch-with-git-and-manage-branches).

## Running the App

### Start the development server
  
This command serves the app at http://localhost:3000 and provides basic URL routing for the app:

        npm run serve

## Make Changes

This bit is up to you!

## Pull Request

### Creating a Pull Request

1. Add your edited files: `git add path/to/filename.ext` You can also do: `git add .` to add all unstaged files. Take care, though, because you can accidentally add files you don't want added. Review your `git status` first.

1. Commit your edits.

        git commit -m "Type you commit message here"

1. If you would want to add/remove changes to previous commit simply add the files as in Step 1 earlier, and use `git commit --amend` or `git commit --amend --no-edit` (for keeping the same commit message).

1. Push your commits to your GitHub Fork: `git push -u origin branch/name-here`

1. Once the edits have been committed, you will be prompted to create a pull request on your fork's GitHub Page.

1. By default, all pull requests should be against the GDG Kolachi's main repo, `hoverboard-v2` branch.

1. Submit a pull request from your branch to GDG Kolachi's `hoverboard-v2` branch.

1. The title (also called the subject) of your PR should be descriptive of your changes and succinctly indicates what is being fixed. `i.e Correct typo in home page`

1. In the body of your PR include a more detailed summary of the changes you made and why.
    - If the PR is meant to fix an existing bug/issue then, at the end of
        your PR's description, append the keyword `closes` and #xxxx (where xxxx
        is the issue number). Example: `closes #13`. This tells GitHub to
        close the existing issue, if the PR is merged.

Read more on submitting a PR [here](https://help.github.com/articles/creating-a-pull-request/)

#### If your PR is accepted

Once your PR is accepted, you may delete the branch you created to submit it.
This keeps your working fork clean.

You can do this with a press of a button on the GitHub PR interface. You can
delete the local copy of the branch with: `git branch -D branch/to-delete-name`

#### If your PR is rejected

Don't despair! You should receive solid feedback from us as to
why it was rejected and what changes are needed.

Many Pull Requests, especially first Pull Requests, require correction or
updating. If you have used the GitHub interface to create your PR, you will need
to close your PR, create a new branch, and re-submit.

If you have a local copy of the repo, you can make the requested changes and
amend your commit with: `git commit --amend` This will update your existing
commit. When you push it to your fork you will need to do a force push to
overwrite your old commit: `git push --force`

Be sure to post in the PR conversation that you have made the requested changes.

## Any Questions?

Feel free to ask any questions by commenting on the issue.
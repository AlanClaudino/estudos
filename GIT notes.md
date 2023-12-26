# Introductiont to Git

## Definition

Git is a type of version control system (VCS). A version control system enables you to record changes to file over time.

Some of the tasks you can perform with git are to take snapshots of files over time, restore earlier versions of files from snapshots you have made and work on multiples versions of a file in parallel.

## Git commit graph

Git tracks changes to files over time. It does this by enabling you to take snapshots of files at any time. These snapshots are called commits and we can represent the commit history with a basic graph.

![Git commit graph example](./img/git%20commit%20%20graph.png)

## Git conceptual areas

In Git, we have 3 logical areas in which we work with our files: working tree, staging area and git history.

The working tree is what we see in our file system. When we add, delete and edit files, we do so in the working tree.

The git history is equivalent to the commit graph. The history is kept in a hidden directory called `.git`. This directory holds an object database and metadata that makes up our repository.

Git gives us full control of which changes in our working tree should be included in our next commit. The way we have this control is through the staging area. Only changes added to the staging area are included in the commit.

## Basic Git Commands

- `git init` initialize a new repo in a directory

- `git config --global user.name "name"`

- `git config --global user.email "email"` The flag **--local** option as well

- `git status` see the state of files in working tree, staging area vs latest commit in git history

- `git add` move file(s) to the staging area

- `git log` view the git history / git commit graph

- `git diff` diff of working tree and staging area

- `git diff --cached` diff of staging area and latest commit

- `git rm` remove a file from the working tree and the staging area

- `git checkout -- filename` retrieve a file from the staging area into the working tree

- `git reset HEAD filename` retrieve a file from the latest commit into the staging area

- `git checkout (commit hash) filename` retrieve a file from a previous commit

## .gitignore

We list on this file all files or directories in our repo we do not want git to track.

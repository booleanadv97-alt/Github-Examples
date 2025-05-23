## Git Hidden Folder

There is a hidden folder called `.git` which tells you that our project is a git repo.

If we wanted to create a git repo in a new project we create the folder and then initialize that repo using `git init`

```
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init
touch Readme.md
code Readme.md
git status
git add .
# makes changes to readme.md
git commit /a /m "add readme file"
```

## Cloning

We can clone three ways: HTTPS, SSH, GitHub CLI

Since we are using GitHub Codespaces we'll create a temporary directory in our workspace

```sh
mkdir /workspace/temp
cd /workspace/temp
```


### HTTPS
```sh
git clone https://github.com/booleanadv97-alt/Github-Examples.git
cd GitHub-Examples
```
> You'll need to generate a Personal Access Token (PAT)

You will use the PAT as your password when you login

- Give it access to Contects for Commits

### SSH

```ssh
git@github.com:booleanadv97-alt/Github-Examples.git
cd Github-Examples
```
## Commits 

When we want to commit code we can write `git commit` which will open up the commit edit message in the editor of choice.
```sh
git commit
```
Normally you will have to set a default editor:
```
git config --global core.editor emacs
```
Make a commit and commit message without opening an editor
```sh
git commit -m "commit mesasge"
``` 
## Branches

List of branches 

```
git branch
```

Create a new branch
```
git branch branch-name
```

Checkout the branch
```
git checkout dev
```

## Remotes
We can add remote but often you wil just add remote via upstream when adding a branch

```sh
git remode add ...
git branch -u origin new-feature
```
## Stashing
```
git stash list
git stash
git stash my-name
git stash apply
git stash pop
```
## Merging
```
git checkout dev
git merge main
```
## Add

When we want to stage changes that will be included in the commit we can use the . to add all possible files.

## Reset

Reset allows you to move Staged changes to be unstaged.
This is useful when you want to revert all files not to be commited.

```
git add .
git reset
```

> git reset will revert a git add.

## Status

Git status shows you what files will or not will be commited.

```
git status
```

## Gitconfig file

The gitconfig file is what stores your global configurations for git such as email, name, editor and more.

Showing the contents of our .gitconfig file

```
git config --list
```

When you first install Git on a machine you are suppose to set up your name and email

```sh
git config --global user.name "John Doe"
git config --global user.email johndoe@example.com
```

## Log

`git log` will show recent git commits to the git tree

## Push

When we want to push a repo to our remote origin

```
git push
```
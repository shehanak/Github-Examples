## Git Hidden Folder

There is a hidden folder called `.git` which tells you that our project is a git repo.

If we wanted to create a git repo in a new project we create the folder and initialize that repo using `git init`

```
mkdir /workspaces/tmp/new-project
cd /workspaces/tmp/new-project
git init
touch Readme.md
code Readme.md
git status
git add Readme.md

# make changes to readme.md
git commit -a -m "add readme file"
```


## Cloning

We can clone three ways: HTTPS, SSH, Github CLI

Since we are using Github codespaces we'll create a temporary derectory in our workspace

``` sh
mkdir /workspace/tmp
cd /workspace/tmp
```

## HTTPS

``` sh
git clone https://github.com/ShehanCodes/Github-Examples.git
cd Github-Examples
```

> You'll need to generate a Personal Access Token
https://github.com/settings/personal-access-tokens

You will use the PAT as your password when you login

- Give it access to Contents for Commits

### SSH

```sh
git clone git@github.com:ShehanCodes/Github-Examples.git
```

We will need to create our own SSH rsa key pair

## Commits

When we want to commit code we can write git commit which will open up the commit edit message in the editor of choice.

``` sh
git commit
```

Set the global editor
```
git config --global core.editor emacs
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

Check out the branch

```
git checkout dev
```

## Remotes

## Stashing

## Merging

## Add

When we want to stage changes that will be included in the commit
We can use the . to add all possible files.

```
git add Readme.md
```

## Reset

Reset allows you to move Staged changes to be unstaged.
This is useful when you want to revert all files not to be commited.

```
git add .
git reset
```

> git reset will revert a git add .

## Status

Git status shows you what files will or will not be commited.

```
git status
```

## Gitconfig

The gitconfig file is what stores your global configurations for git such as email, name, editor and more. 

Showing the contents of our .gitconfig file
```
git config --list
```

When you first install Git on a machine you are suppose to set up your name and email.

```
git config --global user.name "John Doe"
git config --global user.email "johndoe@example.com"
```

---
id: 2-basic-github
title: Basic Github
sidebar_label: Basic Github
---

## GIT first-time setup

After installing GIT, first thing to do is to set user name and email address. Every Git commit uses this information.

```shell
git config --global user.name "John Doe"
git config --global user.email "johndoe@example.com"
```

By default Git will create a branch called master when you create a new repository with git init. From Git version 2.28 onwards, you can set a different name for the initial branch.

To set main as the default branch name do:

```shell
git config --global init.defaultBranch main
```

## A new repo from scratch

Say you’ve just got some data from a collaborator and are about to start exploring it.

1. Create a directory to contain the project.
2. Go into the new directory.
3. Type git init.
4. Write some code.
5. Type git add to add the files (see the typical use page).
6. Type git commit.
7. The first file to create (and add and commit) is probably a ReadMe file, either as plain text or with Markdown, describing the project.

Markdown allows you to add a bit of text markup, like hyperlinks, bold/italics, or to indicate code with a monospace font. Markdown is easily converted to html for viewing in a web browser, and GitHub will do this for you automatically.

## A new repo from an existing project

Say you’ve got an existing project that you want to start tracking with git.

1. Go into the directory containing the project.
2. Type git init.
3. Type git add to add all of the relevant files.
4. You’ll probably want to create a .gitignore file right away, to indicate all of the files you don’t want to track. Use git add .gitignore, too.
5. Type git commit.

## Connect it to github

You’ve now got a local git repository. You can use git locally, like that, if you want. But if you want the thing to have a home on github, do the following.

1. Go to github.
2. Log in to your account.
3. Click the new repository button in the top-right. You’ll have an option there to initialize the repository with a README file, but I don’t.
4. Click the “Create repository” button.
5. Now, follow the second set of instructions, “Push an existing repository…”

```shell
git remote add origin git@github.com:username/new_repo
git push -u origin master
```

Actually, the first line of the instructions will say

```shell
git remote add origin https://github.com/username/new_repo
```

But I use `git@github.com:username/new_repo` rather than `https://github.com/username/new_repo`, as the former is for use with ssh (if you set up ssh as I mentioned in “Your first time”, then you won’t have to type your password every time you push things to github). If you use the latter construction, you’ll have to type your github password every time you push to github.

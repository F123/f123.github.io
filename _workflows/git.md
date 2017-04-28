---
layout: page
title: Git Version Control Workflow
permalink: /workflows/git/
---

## Git Version Control Workflow in F123

This is a very basic `workflow` explanation. It assumes you are
working from the command-line and not using a GUI `git` client
program.

## Cloning a Repository

First to clone a git repository to your local machine:

git clone https://github.com/f123/f123pi.git

Which will clone the f123pi repository into the directory `f123pi`
relative to where you are working currently.

## Edit Files

Now you can edit files to your heart's content and there is no danger
of breaking anything or over-writing earlier work in a way which makes
it impossible to recover it if things go wrong or if experiments don't
work.

## Add and Commit

The next stage when you are happy with your changes are to `add` a
changed file. This is called `staging` in `git` language.

To `stage` (add) a file called `index.md`:

git add index.md

Assuming the file is in your current working directory.

At any time you can see the status of all of the files which make up
the repository by typing:

git status

I like to redirect the output from `git status` to a file and review
the file in an editor. This is very useful if there are many files and
there have been many chnges:

git status > res
nano res

To `commit` changes, you can either enter a commit message on the
command-line, like this:

git commit -m "Fixed a typographical error in index.md"

Or you can just enter:

git commit

And your default editor will open for you to type the commit message.
If you do this,remember that all lines with a hash symbol at the
beginning are ignore, and an empty file, including a file with all
lines commented-out, will abort a commit.

In committing large changes I also like to redirect the output of `git
status`, edit the file and then use the file for my commit message
with the `-F` switch:

git status > res
nano res
git commit -F res

## Checkout

If you decide that changes you have made are incorrect, before
`staging` you can get back to the previous version like this:

git checkout index.md

Which will over-write index.md with the saved version.

## Push

After you have committed changes, you will need to `push` them to make
them visible to everybody else.

To push, type this at the command-line:

git push origin master

## Commit often, pull regularly

It is a good idea before making changes to anything, to `pull` so that
you can see the correct and current status:

git pull

If somebody else makes changes to a file you are changing, then
changes will need to be merged. The merge can be complex for a complex
source file, but is less of a problem for documentation or blog posts.

## Branching

You can create a local `branch` if you want to make wholescale changes
or additions to many files.

Give your branch a meaningful name:

git checkout -b fix_menu_bug

Will create the branch `fix_menu_bug and switch to it.

At any time you can see which branch you are on currently with:

git branch

Which gives something like:

master
*fix_menu_bug

The asterisk indicates you are currently on the `fix_menu_bug` branch.

To switch back to the `master` branch:

git checkout master

Now:

git branch

Will give:

*master
fix_menu_bug

To indicate you are back on the `master` branch.

## Merging a Branch Back into Master

Let's say you have fixed the menu bug and you now want to merge the
fixed code back into the `master` branch. First make sure you are on
the `master` branch and then:

git merge fix_menu_bug

If there are no conflicats with other people's work to overcome, all
changes which have been committed on the `fix_menu_bug` branch will be
merged into `master`.

You can now delete the `fix_menu_bug` branch.

git branch -d fix_menu_bug

## Remote Tracking

Branches you create are *not* available remotely to other people
unless they are `remotely tracked`. It is not very easy to understand
in my experience so will not be discussed here.

## Workflow in Brief

1. Clone.
2. Edit, edit, edit.
3. Checkout if you want to abandon changes.
4. Stage (add).
5. Commit.
6. Push.
7. Pull (regularly before making edits).

## Git Configuration

You maye need to make a couple of configurations to your command-line
`git` before you start work, and especially before you can push:

git config --global user.name "Bilbow Baggins"
git config --global user.email "bilbo@middle.earth.com"
git config --global core.editor emacs


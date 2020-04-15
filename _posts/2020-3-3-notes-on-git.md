---
layout: post
title: Notes on Git
categories: [projects, courses]
tags: [git, vcs, coursera]
---

Note (mostly) to self about how to use basics of git and follow best practices

on setting new [email and privacy](https://help.github.com/articles/keeping-your-email-address-private/)

`git init`
`git clone URL`

`git init` creates .git/ (git directory) in the current directory, the "working tree" is the current/parent directory that contains .git/

The git directory contains all the changes and their history and the working tree contains the current versions of the files.

The git directory acts as a database for all the changes tracked in Git and the working tree acts as a sandbox where we can edit the current versions of the files.

`git add filename`
adds to the staging area (a file) - an index of what will go to the next commit

`git status` current info
`git log` histor of commits

`git commit -m 'Commit message'`
multiline are ususally ok  -first as topic

`git commit -a -m`
commit previously added skipping staging

and after a blank one more detailed description
could follow in up to 72 chars ususally
because `git log` commend will not do any line wrapping.

tracking lifecycle
new files start as untracked

git add new_file
puts new_file in the staging area (skips modified for new files)

tracked: modified > staged > committed

`git diff filename` for diff-like compare

without git there's still:

`create diff file`

`diff -u old_file new_ file > change.diff`
and
`patch old_file < change.diff` to merge diff with original file


Command	Explanation & Link
git commit -a	Stages files automatically
git log -p	Produces patch text
git show	Shows various objects
git diff	Is similar to the Linux `diff` command, and can show the differences in various commits
git diff --staged	An alias to --cached, this will show all staged files compared to the named commit
git add -p	Allows a user to interactively review patches to add to the current commit
git mv	Similar to the Linux `mv` command, this moves a file
git rm	Similar to the Linux `rm` command, this deletes, or removes a file
There are many useful git cheatsheets online as well. Please take some time to research and study a few, such as [this one](https://github.github.com/training-kit/downloads/github-git-cheat-sheet.pdf).

.gitignore files
.gitignore files are used to tell the git tool to intentionally ignore some files in a given Git repository. For example, this can be useful for configuration files or metadata files that a user may not want to check into the master branch. Check out more at: https://git-scm.com/docs/gitignore.

A few common examples of file patterns to exclude can be found [here](https://gist.github.com/octocat/9257657).

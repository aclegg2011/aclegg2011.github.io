---
layout: post
title: "Useful Git Commands"
date: 2018-12-18
---

# change current branch name
git branch -m
 
git show commitID > file.txt
or >> to append to the end of an existing file
 
git diff-tree --no-commit-id --name-only -r commit (shows only files changed)
 
$ git clone will give you the whole repository.
$ git tag -l and then checkout a specific tag:
$ git checkout tags/<tag_name>
or
$ git checkout tags/<tag_name> -b <branch_name>
 
then git reflog
find the last good head
and then git reset --hard {whatever head}
 
git cherry-pick -m 1 parent_commit
 
#add new commit to gerrit
add new commit
make changes
git add -A && git commit -s
add comment ctrl+x
git review
 
#append to current commit
make change
git add .
git commit -s --amend
git review
 
// Store github username and password
git config --global credential.helper store
git config --global credential.helper 'cache --timeout 7200'
 
warning: inexact rename detection was skipped due to too many files.
warning: you may want to set your merge.renamelimit variable to at least 3745 and retry the command.
git config merge.renameLimit 999999
//Revert
git config --unset merge.renameLimit
 
// Remove remote branch from repo
git push <remote name> --delete <branch>
 
 ! [remote rejected] p9.0 -> p9.0 (shallow update not allowed)
error: failed to push some refs to 'prebuilts_build-tools.git'
git fetch --unshallow <original_remote>

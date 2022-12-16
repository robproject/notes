---
id: 8jlp33vk61u8j5wabgfaanm
title: Git
desc: ''
updated: 1669520693972
created: 1637553970482
---
## Update
### Windows
git update-git-for-windows


## Operations
### Stash Pull Apply
git add .
git stash
git pull upstream version-13 # or origin
git stash apply

### Remove from staging
git restore --staged [-r] [file1] [file2] [dir [need -r]]
### Remove all from staging
git reset HEAD

### See all branches
git branch -a

### Log
git log --oneline

### Status
git status


## Files
### .git/config
```
[core]  
	repositoryformatversion = 0  
	filemode = false  
	bare = true   =====>  means no working copy, can be cloned from  
	logallrefupdates = true  
	symlinks = false  
	ignorecase = true  
[remote "origin"]  
	url = C:\\Users\\%USER%\\dendron\\.git  
	fetch = +refs/heads/*:refs/remotes/origin/*  
[branch "master"]  
	remote = origin  
	merge = refs/heads/master  
```

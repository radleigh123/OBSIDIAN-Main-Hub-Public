---
cssclass:
title: Git
creation-date: 2023-08-17
aliases:
tags:
- Git
- 
---
**[[MAIN-CODE]]**

---
# Git

**Editing texts**
```bash
# Replaces the texts in the file
echo "add texts" > file.txt

# Appends the file with the given string, newline
echo "add newline texts" >> file.txt
printf "add newline texts\n" >> file.txt

# Appends multiple newlines (NOT WORKING)
cat << EOF >> file.txt
> Hello World
> Earth-616
> EOF
```

**Switching to another branch/commit**
```bash
# Go to existing branch
git checkout <existing_branch>

# Go to and create branch, -b (means, run git branch before git checkout)
git checkout -b <new_branch>

# Go to specific commit
git checkout <commit_hash>

# Go to previous commit
git checkout HEAD^

# Go back to two commits
git checkout HEAD~2
```

**Checking commit history**
```bash
# Show default logs
git log

# Show logs in one line
git log --oneline

# Show logs with references (branches, tags, etc)
git log --decorate

# Show logs in the form of graph
git log --graph

# Include all the branches of the repo
git log --all
```

**Editing branchs**
```bash
# Creating a branch
git branch <branch_name>

# Deleting a branch
git branch -D <branch_name>
```

<br>

# 
---
- **Adding new lines** - [How to Append to File in Bash (phoenixnap.com)](https://phoenixnap.com/kb/bash-append-to-file#:~:text=One%20of%20the%20ways%20to,end%20of%20the%20specified%20file.)
- **Git checkout** - [Git Checkout | Atlassian Git Tutorial](https://www.atlassian.com/git/tutorials/using-branches/git-checkout)
- **Commit history** - [Git - git-log Documentation (git-scm.com)](https://git-scm.com/docs/git-log)
	- [Git log --oneline - Scaler Topics](https://www.scaler.com/topics/git/git-log-one-line/)
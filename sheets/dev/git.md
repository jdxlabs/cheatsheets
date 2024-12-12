# Git

## Manage repositories

### Create a new one
```bash
mkdir repository_name
cd repository_name
git init
```

### Clone an existing one
```bash
git clone git://<repo>
git clone https://user@bitbucket.org/user/repo_name.git
git clone https://github.com/user/repo_name.git
```

## Repository status

### Compare Versions
```bash
git diff #changes made since last commit
git diff <commit1> <commit2>
git diff <commit> <path> #changes between a particular commit and the current file
```

### See what has not been validated
```bash
git-status
```

### List of commits made
```bash
git-log
```

### Delete a branch locally
```bash
git branch -d <branchname>
```

### Create a branch and switch to it
```bash
git checkout -b <branchname>
```

## File Management

### Add files to commit
```bash
git add . #add all uncommitted files
git add <file1> <file2> #add specified files
```


### Delete file
```bash
git rm <filename> #delete locally and also on repository
```

### Move a file
```bash
git mv <file_name> <new_destination>
```


## Commit Management

### Update your local repository
```bash
git pull

# or
git pull --rebase
```

### Commit
```bash
git commit <file1> <file2> #commit the filled in files (which need to be staged)
git commit -a #committe modified files, even if not in staged state
git commit -m "<description>" #commit staged files, with description message
```

### Add commit to repository
```bash
git push origin master #push into master branch
git push
```


## Undo Commands

### Undo changes to a specific file
```bash
git checkout HEAD <file>
git checkout <file>
```

### Undo changes made since last commit
```bash
git reset --hard HEAD
```

### Delete last commit
```bash
git reset --hard HEAD^
```

### Delete one (or more) unpushed commit
```bash
git reset --hard <last-id>
```

### Delete an already pushed commit
```bash
(from the branch to revert)
git log --> get last correct hash
 
# to revert the local repository
git reset --hard <commit_id>
 
# to revert the remote repository
git push -f origin <commit_id>:develop
 
git status
` Your branch is up to date with 'origin/develop'.
` nothing to validate, the working copy is clean
```

### Purge a file from Git history
```bash
git filter-branch --force --index-filter \
  "git rm --cached --ignore-unmatch config/apiKeys.json" \
  --prune-empty --tag-name-filter cat -- --all
# Purges `config/apiKeys.json` from history

git push origin --force --all
```


## Tagging

### Create a new tag
```bash
git tag 1.0.1
git push --tags
```

### Delete a tag (may be useful in some contexts)
```bash
git tag -d 1.0.1 && git push origin :refs/tags/1.0.1
```


## Others

### View the commit history of a file
```bash
git log -p filename
```


## Git Config

### Enable Color
```bash
git config color.ui true
```

### Dealing with word wrap issues on Windows
```bash
git config --global core.autocrlf true
```

### ~/.gitconfig file
```bash
[user]
     name = ...
     e-mail = ...

[color]
     ui=true
```

### Debug: detect the gitignore rule that is applied on a file
```bash
git check-ignore -v < any_file >
```

### Bonus: A little utily to see last changes directly in the console
```bash
apt install tig

# You can call it in your repository
tig

# To navigate :
# Up/down to explore commits
# Ctrl U/D to browse the changed files in the current commit
# and Q to quit !
```


## Useful links
* [Learn git branching](https://learngitbranching.js.org)
* [Learn git concepts, not commands](https://dev.to/unseenwizzard/learn-git-concepts-not-commands-4gjc)
* [Code Review Developer Guide](https://google.github.io/eng-practices/review)
* [Git Submodule Cheatsheet](https://medium.com/faun/git-submodule-cheatsheet-29a3bfe443c3)

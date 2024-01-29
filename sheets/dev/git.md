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


## Git Setup

### Enable Color
```bashgit config color.ui true```

### Dealing with word wrap issues on Windows
```bashgit config --global core.autocrlf true```

### Installation of the Eclipse plugin: Egit
[[http://www.eclipse.org/egit/download/|Get the plugin here]] and install it via: Help >> Install New Software.


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

## To go further
   * [[https://learngitbranching.js.org/|Learn git branching]]
   * [[https://dev.to/unseenwizzard/learn-git-concepts-not-commands-4gjc|Learn git concepts, not commands]]
   * [[https://google.github.io/eng-practices/review/|Code Review Developer Guide]]
   * [[https://medium.com/faun/git-submodule-cheatsheet-29a3bfe443c3|Git Submodule Cheatsheet]]
   * [[git-subtrees|Git SubTrees - An alternative to SubModules]]
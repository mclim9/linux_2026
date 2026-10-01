# GIT Command Cheat sheet
---------------------------------------------------------------------------------------
## Basic Commands

| Function        | Command                                                           |
| --------------- | ----------------------------------------------------------------- |
| Clone Repo      | `git clone <web address>`                                         |
| Pull            | `git pull`                                                        |
| Show Unstgd Chg | `git diff`                                                        |
| Status          | `git status`                                                      |
| Push to Server  | `git.exe push -v --progress "origin" master:master`               |
| Mystery         | `git rev-list --objects --all  #See what files are being tracked` |

---------------------------------------------------------------------------------------
## Start

### Initial Setup - name
```GIT
git config --global user.name "Your Name"
git config --global user.email "you@example.com"
git config --list               # Verify
```

### Define Repo

```GIT
git remote add <repo> <url>
git remote              # list repos
git push --set-upstream <repo> master
```

### Commit Files to Repo

```GIT
git add *.*
git commit -m "<message>"
git push
git status
```

## Merge Branch w/ origin

```GIT
git checkout master
git pull origin master
git merge <test>
git push origin master
```

---------------------------------------------------------------------------------------
## Remove

### Delete local Files to match Repo

```GIT
git fetch --all
git reset --hard origin/master
git pull
```

### Reduce git size

```GIT
git rev-list --objects --all   #See what files are being tracked
git filter-branch --index-filter 'git rm --cached --ignore-unmatch file_to_remove' --prune-empty -- --all
git prune
git reflog expire --all --expire=now
git gc --prune=now --aggressive
git gc --aggressive
```

## Remove deleted files

[Source](https://git-scm.com/book/en/v2/Git-Internals-Maintenance-and-Data-Recovery)

```GIT
git rev-list --objects --all   #See what files are being tracked
git filter-branch --index-filter 'git rm --cached --ignore-unmatch *.mov' -- --all
rm -Rf .git/refs/original
rm -Rf .git/logs/
git gc --aggressive --prune=now
git count-objects -v
```

---------------------------------------------------------------------------------------
## Links

[Source](https://github.com/mclim9/linux_2026)

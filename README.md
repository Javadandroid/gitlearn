# Git Cheat Sheet

**git init :** initial git in the current directory

**rm -rf .git :** remove git fro current directory (located in git directory for linux)

**Remove-Item -Recurse -Force .git** remove git fro current directory (located in git directory for windows shell)

**git status :** show status of git

**.gitignore file:** untracked files can be set in this file

**git add `<filename>`:** add file for stage level for adding all files use "." 

**git restore --staged `<filename>`:** remove file from stage level for removing all files use "." 

**git commit:** make a snapshot for all staged files
>for better message we can use :

| Prefix | Full Name | Emoji | Description |
| :--- | :--- | :---: | :--- |
| **feat** | Feature | ✨ | Introduces a new feature to the codebase. |
| **fix** | Bug Fix | 🐛 | Patches a bug in your codebase. |
| **docs** | Documentation | 📝 | Documentation only changes (like README or Wiki). |
| **style** | Styles | 💎 | Changes that do not affect the meaning of the code (white-space, formatting, etc). |
| **refactor** | Refactoring | ♻️ | A code change that neither fixes a bug nor adds a feature (code cleanup). |
| **perf** | Performance | 🚀 | A code change that improves performance. |
| **test** | Tests | 🧪 | Adding missing tests or correcting existing tests. |
| **build** | Builds | 📦 | Changes that affect the build system or external dependencies (e.g., npm, pip). |
| **ci** | CI | 👷 | Changes to CI configuration files and scripts (e.g., GitHub Actions). |
| **chore** | Chores | 🔧 | Other changes that don't modify src or test files (maintenance tasks). |
| **revert** | Revert | ⏪ | Reverts a previous commit. |
---

**git log :** show all commits
>- for show all commits use `--all`
>- for show graph and line use `--graph`
>- for summerize the each commit in one line use `--oneline`

**git checkout `<commitHash>`:** for reverting and go to a specific commit
>you can use partial of HASH
---
 
**git checkout `<branchName>` :** for switching between branches and last commit of that branch

**git switch `<branchName>`:** for switching between branches safer than checkout and newer


**git switch --detach `<commitHash>` :** for back to specific commit 

**git switch -c `<branchName>` :** for create new branch
>we can delete this branch

**git merge `<branchName>` :** merge a commit from diffrent branch to current bfanch

**git branch -d `<branchName>` :** delete branch with name 

**git remote add origin `<URL>`** connect to git repo remotely
>- **remote:** connect remotely
>- **add:** add new connection
>- **origin:** is an Alias for our url

**git remote -v:** show remote url with aliases and permissions

**git push `<Alias or URL>` `<branch name>`:**
>**-u** flag short for **--set-upstream** this make our push permanent and no need for next times to enter ***alias*** and ***branch name***

>example: git push -u origin master ***next Time:*** git push

**git reset `<head~><number of commits from end> or <commit hash>`:** delete commits to head number or hash
>example: git reset head~1

>- **--soft** this flag delete commit message and files go in staged level.
>- **--mixed** this flag delete commit message and files go in unstaged level.
>- **--hard** delete commit and changes, in default without flag use git use this.

Reset Mode | Command Example | Commit History | Staging Area (Index) | Working Directory (Files) | Use Case |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Soft** 🟢 | `git reset --soft HEAD~1` | **Removed** ❌<br>(Moves HEAD back) | **Staged** 🟢<br>(Files remain added) | **Preserved** ✅<br>(Changes are safe) | When you want to fix the commit message or combine commits. |
| **Mixed** 🟠 | `git reset --mixed HEAD~1`<br>*(Default)* | **Removed** ❌<br>(Moves HEAD back) | **Unstaged** 🔴<br>(Files are modified) | **Preserved** ✅<br>(Changes are safe) | When you want to keep your work but unstage the files. |
| **Hard** 🔴 | `git reset --hard HEAD~1` | **Removed** ❌<br>(Moves HEAD back) | **Cleared** 💨<br>(Reset to match HEAD) | **Discarded** ❌<br>(All changes are **LOST**) | When the last commit was a total mistake and you want to destroy it. |


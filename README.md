# Git Cheat Sheet

**git init :** initial git in the current directory

**rm -rf .git :** remove git fro current directory (located in git directory for linux)

**Remove-Item -Recurse -Force .git** remove git fro current directory (located in git directory for windows shell)

**git status :** show status of git

**.gitignore file:** untracked files can be set in this file

**git add `<filename>`:** add file for stage level for adding all file use "." 

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

**git checkout `<commitHash>`:** for reverting and go to a specific commit
>you can use partial of HASH
---
 
**git checkout `<branchName>`:** 


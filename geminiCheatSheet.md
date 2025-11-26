# Git Cheat Sheet 🚀

یک راهنمای سریع و کامل برای دستورات گیت، از ساخت و حذف تا مدیریت برنچ‌ها و ریموت.

---

## 1. Setup & Config (تنظیمات اولیه)
قبل از شروع، باید هویت خود را مشخص کنید.

| Command | English Description | Example |
| :--- | :--- | :--- |
| `git config --global user.name` | Sets the name you want attached to your commit transactions | `git config --global user.name "Ali Karimi"` |
| `git config --global user.email` | Sets the email you want attached to your commit transactions | `git config --global user.email "ali@example.com"` |
| `git config --list` | List all the settings of your git configuration | `git config --list` |

---

## 2. Create & Delete Repositories (ساخت و حذف مخزن)
شروع کار با ایجاد یک پروژه جدید یا کپی کردن یک پروژه موجود.

| Command | English Description | Example |
| :--- | :--- | :--- |
| `git init` | Create a new local repository (adds .git folder) | `git init` |
| `git clone <url>` | Downloads a project and its entire history from the internet | `git clone https://github.com/user/repo.git` |
| `rm -rf .git` | **Delete** the repository (Un-track project by removing .git folder - Linux/Mac) | `rm -rf .git` |
| `rd /s /q .git` | **Delete** the repository (Windows CMD) | `rd /s /q .git` |

---

## 3. File Operations: Add, Remove, Move (مدیریت فایل‌ها)
اضافه کردن فایل‌ها به استیج یا حذف آن‌ها.



| Command | English Description | Example |
| :--- | :--- | :--- |
| `git status` | List all new or modified files to be committed | `git status` |
| `git add <file>` | Snapshots the file in preparation for versioning | `git add index.html` |
| `git add .` | Stages all changes in the current directory | `git add .` |
| `git rm <file>` | **Deletes** the file from the working directory and stages the deletion | `git rm script.js` |
| `git rm --cached <file>` | Removes the file from version control but preserves the file locally | `git rm --cached secret.json` |
| `git mv <old> <new>` | Renames a file and stages the change | `git mv file.txt newfile.txt` |

---

## 4. Snapshotting (ذخیره تغییرات)
ثبت نهایی تغییرات در تاریخچه گیت.

| Command | English Description | Example |
| :--- | :--- | :--- |
| `git commit -m "<msg>"` | Records file snapshots permanently in version history | `git commit -m "Fix login bug"` |
| `git commit --amend` | Replaces the most recent commit with the staged changes | `git commit --amend -m "New message"` |

---

## 5. Branching & Merging (شاخه‌ها و ادغام)
ساخت شاخه‌های جدید و حذف آن‌ها.



[Image of Git branching model]


| Command | English Description | Example |
| :--- | :--- | :--- |
| `git branch` | Lists all local branches in the current repository | `git branch` |
| `git branch <branch>` | Creates a new branch | `git branch feature-login` |
| `git checkout <branch>` | Switches to the specified branch | `git checkout main` |
| `git checkout -b <branch>` | Creates a branch and switches to it immediately | `git checkout -b develop` |
| `git branch -d <branch>` | **Deletes** the specified branch | `git branch -d feature-login` |
| `git merge <branch>` | Merges the specified branch’s history into the current one | `git merge develop` |

---

## 6. Sharing & Updating (اشتراک‌گذاری و ریموت)
ارتباط با سرورهایی مثل GitHub یا GitLab.

| Command | English Description | Example |
| :--- | :--- | :--- |
| `git remote add <name> <url>` | Connects a local repo to a remote server | `git remote add origin https://github.com/...` |
| `git remote -v` | Verifies the new remote URL | `git remote -v` |
| `git fetch` | Downloads all history from the remote tracking branches | `git fetch origin` |
| `git pull` | Updates your current local working branch with all new commits from the remote | `git pull origin main` |
| `git push` | Uploads all local branch commits to the remote | `git push origin main` |

---

## 7. Inspection & Comparison (بازرسی و مقایسه)
بررسی تاریخچه و تفاوت‌ها.

| Command | English Description | Example |
| :--- | :--- | :--- |
| `git log` | Lists version history for the current branch | `git log` |
| `git log --oneline` | Lists version history in a compact format | `git log --oneline` |
| `git diff` | Shows file differences not yet staged | `git diff` |
| `git diff --staged` | Shows file differences between staging and the last version | `git diff --staged` |

---

## 8. Undo & Reset (بازگشت و اصلاح)
برگرداندن تغییرات اشتباه.

| Command | English Description | Example |
| :--- | :--- | :--- |
| `git restore <file>` | Discards changes in working directory (undo edit) | `git restore style.css` |
| `git restore --staged <file>` | Unstages the file (undo git add) | `git restore --staged style.css` |
| `git reset --hard HEAD` | Discards all local changes in working directory | `git reset --hard HEAD` |
| `git reset <commit>` | Resets index but keeps changes in working directory | `git reset a1b2c3d` |

---

## 9. Stashing (ذخیره موقت)
ذخیره تغییرات بدون کامیت کردن برای استفاده در آینده.

| Command | English Description | Example |
| :--- | :--- | :--- |
| `git stash` | Temporarily stores all modified tracked files | `git stash` |
| `git stash list` | Lists all stashed changesets | `git stash list` |
| `git stash pop` | Restores the most recently stashed files | `git stash pop` |
| `git stash drop` | **Deletes** the most recently stashed changeset | `git stash drop` |
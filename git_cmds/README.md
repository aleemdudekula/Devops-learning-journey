# Git Tutorial

## What is origin in Git?

origin is just a default remote name created when you clone a repository.

When you run:

git clone https://github.com/username/repo.git

Git automatically creates:

origin → https://github.com/username/repo.git

Check it:

git remote -v

⚠️ Important:
origin is not special. It’s just a nickname. You can rename it.

## 2️⃣ Difference Between git pull and git push

Command	Direction	What It Does

git pull	Remote → Local	Downloads and merges changes

git push	Local → Remote	Uploads your commits

git pull

git pull origin main

Equivalent to:

git fetch origin

git merge origin/main

git push

git push origin main

Sends your local commits to remote.

⚠️ Reality check:

pull can create unwanted merge commits.

Professionals often use:

git pull --rebase

## 3️⃣ What is git add?

It stages changes for the next commit.

Add single file:

git add file.py

Add multiple files:

git add file1.py file2.py file3.py

Add all files:

git add .

Then:

git commit -m "Added programs"

git push origin main

### ⚠️ Important:

You don’t “add to GitHub”.

You add locally → commit → then push.

## 4️⃣ What is Master and Feature Branch?

Modern default branch name is usually main, not master.

🔹 main (or master)

Stable production-ready code

Should not break

🔹 feature branch

Used to develop new features

Created from main (or develop)

### Example:

git checkout -b feature-login

## 5️⃣ How to Push Code from Feature to Main

Correct professional flow:

# Create feature branch

git checkout -b feature-prime

# Make changes

git add .

git commit -m "Add prime program"

# Push feature branch

git push origin feature-prime

Now:

# Switch to main

git checkout main

git pull origin main

# Merge feature

git merge feature-prime

# Push main

git push origin main

⚠️ In real teams:

You DO NOT merge locally.

You create a Pull Request.

🔥 Real GitHub Flow (Professional Way)

🖥️ GitHub Interface Example

4 Steps:

Push feature branch

Go to GitHub

Click "Compare & Pull Request"

Review changes

Merge PR

Delete branch

## 6️⃣ How to Handle Branching Strategy in GitHub?

Common Strategy: Git Flow

4 Typical Structure:

main → production

develop → integration

feature/*

release/*

hotfix/*

⚠️ But here's reality:

For small teams:

Just use main + feature branches.

Git Flow is often overkill.

Don’t complicate if your team is 3–5 devs.

## 7️⃣ How to Revoke Changes Done in GitHub?

Depends on situation.

## ✅ Safe Way (Already Pushed)
git revert <commit-hash>

Creates new commit that undoes change.

Best for shared branches.

⚠️ Dangerous Way (Rewrite History)

git reset --hard <commit-hash>

git push --force

This rewrites history.

Never do this on:

main

Shared branches

Unless your team agrees.

⚡ Bonus: Recover Deleted Branch

git checkout -b feature origin/feature

Or use:

git reflog

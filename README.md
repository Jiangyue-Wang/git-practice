# Git and GitHub Practice Tutorial

Welcome to the Git and GitHub practice repository under Prugh Lab! Follow this tutorial to practice Git commands and GitHub workflows.

---------------------------------------------

## **1. Clone the Repository**
Start by cloning this repository. This will copy all its contents to your local machine.
```bash
git clone https://github.com/<your-username>/<repo-name>.git
cd <repo-name>
```
## **2. Create and Switch to a Branch
To avoid working directly on the main branch, create your own branch:
```bash
git checkout -b my-branch
```

## **3. Make Changes and Commit
Edit file1.txt and file2.txt as per the assigned issue. Save the file, then stage and commit the changes:
```bash
git add file1.txt
git commit -m "Edit file1 and file2 as per Issue #1"
```

## **4. Push the changes
Push your branch to GitHub:
```bash
git push
```

## **5. Open a Pull Request
Go to the repository on GitHub.

Click Compare & Pull Request for your branch.

Add a meaningful description of the changes and submit the pull request.

## **6. Fetch and Merge Changes

After your pull request is merged, update your local repository with the latest changes:
```bash
git checkout main
git pull origin main
```
**If there's a conflict:**
Open the conflicting files in your editor.

Fix the conflict markers (e.g., <<<<<< and >>>>>>).

Stage and commit the resolved file:
```bash
git add <conflicting-file>
git commit -m "Resolve merge conflict"
```

## **7. Rebase a branch to another
If the main branch has been updated and you want to apply those updates to your branch, you can use git rebase. This helps keep your commit history clean.

Switch to your branch:
```bash
git checkout my-branch
```
Rebase onto the latest main branch:
```bash
git fetch origin
git rebase origin/main
```
If there are conflicts:

Resolve the conflicts in the files (as described in Step 6).

Continue the rebase process:
```bash
git rebase --continue
Force-push the updated branch to GitHub:
git push --force-with-lease
```
Note: Use git rebase with caution if you’re collaborating closely with others on the same branch. Discuss with your team first. If it's your own branch, that's fine.

## A final resolution if you mess up everything
Copy paste your code files to a safe place (e.g. Desktop) and delete the whole repo folder. Clone them again from remote, and copy paste back the files, stage, commit, and push.

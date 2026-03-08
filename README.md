# Git Version Control – Lab 2
---

1. Create Local Repository

Create a new project directory and initialize it as a Git repository:
```bash
mkdir Lab2
cd Lab2
git init
```
Create a README file and commit it:
```bash
echo "# Lab2 Git Practice" >> README.md
git add .
git commit -m "initial commit"
```
Connect the repository to the remote and push:
```bash
git remote add origin https://github.com/OmarHesham249/lab-2.git
git branch -M main
git push -u origin main
```
2. Create Branches
Create dev branch:
```bash
git checkout -b dev
echo "this is dev branch" >> dev.txt
git add .
git commit -m "add dev file"
git push origin dev
```
Create test branch:
```bash
git checkout main
git checkout -b test
echo "this is test branch" >> test.txt
git add .
git commit -m "add test file"
git push origin test
```
3. Merge Branches into Main

Merge both branches into main:
```bash
git checkout main
git merge dev
git merge test
git push origin main
```
4. Delete Branches
Local Branch Deletion:
```bash
git branch -d dev   # Removes local dev branch
git branch -d test  # Removes local test branch
```
Remote Branch Deletion:
```bash
git push origin --delete dev
git push origin --delete test
```
5. Switching Without Committing

Temporarily save uncommitted changes:
```bash
git stash         # Save changes
git checkout dev  # Switch branch
git stash pop     # Restore saved changes
```
6. Working with Tags
Create and Push Tag:
```bash
git tag -a v1.7 -m "version 1.7 release"
git push origin v1.7
```
List Tags:
git tag
Delete Tag:

Locally:
```bash
git tag -d v1.7
```
Remotely:
```bash
git push origin --delete v1.7
```
7. Adding Image to README
   
![Image](https://github.com/OmarHesham249/lab-2/blob/main/Image/627fa25ae195ca005f2e20c3-1733279978117.jpeg)

Example:

![Git Logo](https://git-scm.com/images/logos/downloads/Git-Logo-2Color.png)

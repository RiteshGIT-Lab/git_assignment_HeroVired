
# Git LFS Setup and Usage Guide

This document outlines the steps to install and use **Git Large File Storage (LFS)** for handling large files (like PDFs) in a Git repository.

---

## Prerequisites

- Git installed on your system  
- Git LFS installed (`git lfs`)  

---

## Steps

### 1. Initialize Git LFS

```bash
git lfs install
````

This command sets up Git LFS in your local repository, allowing you to track large files.

---

### 2. Track Large Files

```bash
git lfs track "*.pdf"
```

This tells Git LFS to manage all `.pdf` files using LFS.
A `.gitattributes` file will be created or updated automatically.

---

### 3. Add and Commit Changes

```bash
git add .
git commit -m "Large file has been added to GitHub"
```

This stages and commits your changes, including the new `.gitattributes` file.

---

### 4. Push to Remote Repository

```bash
git push
```
- <img width="452" height="176" alt="image" src="https://github.com/user-attachments/assets/38a1da7a-85cd-424b-b3a5-faa46715cc35" />

This uploads your changes to the remote repository.
If you want to push all LFS files explicitly, you can use:

```bash
git lfs push --all origin main
```

---

### 5. Pull Updates from Remote

```bash
git pull
```

This fetches and merges the latest changes from the remote repository.

---

### 6. Verify LFS Installation and Tracking

```bash
git lfs
git status
```

Use these commands to verify that LFS is correctly configured and track the status of your files.

---

## Example Commit Workflow

```bash
git add .
git commit -m "Code is ok"
git push
```

---

## Notes

* Ensure `.gitattributes` is committed and pushed so that collaborators automatically use LFS for the same file types.
* You can check which files are tracked by running:

```bash
git lfs track
```

---

**Author:** *Ritesh Sharma*
**Date:** *10th October 2025*


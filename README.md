# ML Project - Git and GitHub Workflow
## Stage 1: Basic Setup (Foundation)
### Terminal Commands (Starting from Home Directory)

```bash
mkdir ml-project
cd ml-project
git init
touch train.py predict.py utils.py README.md
git status
```

### Explanation

1. `mkdir ml-project`
   Creates a new project directory.

2. `cd ml-project`
   Navigates into the project directory.

3. `git init`
   Initializes a new Git repository.

4. `touch train.py predict.py utils.py README.md`
   Creates empty project files.

5. `git status`
   Checks repository status and tracked/untracked files.

---

## Stage 2: Version Control Workflow (Application)

### Commands and Explanation

1. Stage only required files:

```bash
git add train.py utils.py
```

Stages only the training script and utilities file.

---

2. Commit changes:

```bash
git commit -m "Add training script and utilities"
```

Creates a snapshot of staged changes.

---

3. Create repository on GitHub

Create a repository named **ml-project** on GitHub using the website interface.

---

4. Link local repository to GitHub:

```bash
git remote add origin https://github.com/yourusername/ml-project.git
```

Connects the local repository with the remote GitHub repository.

---

5. Push commits:

```bash
git branch -M main
git push -u origin main
```

Uploads commits to GitHub and sets upstream tracking.

---

## Stage 3: Mini-Project - Collaborative Workflow (Synthesis)

### Scenario

* Remote repository has updates to `predict.py` and `README.md`.
* Local repository has modified `utils.py` and a new file `config.py`.

---

### Step 1: Retrieve teammate's changes

```bash
git status
git stash
git pull origin main
git stash pop
```

**Reasoning:**

* `git status` checks working directory.
* `git stash` temporarily saves uncommitted work.
* `git pull` retrieves teammate updates.
* `git stash pop` restores local changes.

---

### Step 2: Stage and Commit Local Changes

```bash
git add utils.py config.py
git commit -m "Update utilities and add config file"
```

**Reasoning:**

Stages modified and new files before committing them to version history.

---

### Step 3: Push Changes to GitHub

```bash
git push origin main
```

Uploads local commits to the remote repository.

---

### Potential Issues and Handling

1. **Uncommitted Changes Blocking Pull**

Git may prevent pulling changes.

Solution:

```bash
git stash
```

Temporarily saves work.

---

2. **Remote Repository Ahead**

Pull latest changes before pushing.

```bash
git pull origin main
```

---

3. **Authentication Issues**

Login using browser authentication or GitHub credential manager.

---

### Best Practices

* Pull latest updates before starting work.
* Commit frequently with clear messages.
* Stage only required files.
* Check repository status regularly using `git status`.

---

## Repository Link

https://github.com/madesh-codes/ml-project

# Basic-Installation
It will help to check how to install required softwares,library and commands for them
## 1-Git Bash 
#### A.Check Git installation on Windows:
Open command promt and check **git --version**
#### B.Download exe file and install git for windows and then 
Open command promt and check **git --version**
#### C.How to make git bash default terminal in vscode
When terminal is opened, in top right corner user should click on down-arrow button and then an option menu will appear. Then you should select Select Default Profile and you can choose your default terminal from there.
![Img1](https://github.com/programres1/Basic-Installation/blob/main/1.png)
## 2-Python
#### A.Check Python installation on Windows:
Open git bash and check **python --version**
#### B.Download exe file and install python for windows and then 
Open command promt and check **python --version**
## 3-Install uv and commands
#### A.Check uv installation on Windows:
Open git bash and check **uv --version**
#### B.Install uv (pip install uv) for windows and then 
Open command promt and check **uv --version**
#### C. Upgrade uv
**pip install --upgrade uv**

#### D.Core Project & Dependency Management 
**uv init**: Creates a new Python project, including pyproject.toml and a .venv

**uv add -r requirements.txt**:Install all dependencies mentioned in requirements.txt. Also adds the dependencies to pyproject.toml and creates a uv.lock file.

**uv add < package-name >**: Adds dependencies and updates pyproject.toml and uv.lock.

**uv pip install flask ruff** :To install multiple packages, e.g., Flask and Ruff

**uv pip install 'ruff>=0.2.0'**:To install a package with a constraint, e.g., Ruff v0.2.0 or newer

**uv pip install 'ruff==0.3.0'**:To install a package at a specific version, e.g., Ruff v0.3.0

**uv remove < package-name >**: Removes dependencies.

**uv pip install -r pyproject.toml**:Install from a pyproject.toml file

**uv run your_script_name.py** :Run the script using the uv run command

**uv sync**: Updates the virtual environment to match the uv.lock file.

**uv pip compile requirements.txt**: Compiles requirements in project to requirements.txt.

**uv pip sync requirements.txt**: Syncs virtual environment with a requirements.txt.

**uv lock**: Generates or updates the lockfile without installing packages.

**uv tree**: Visualizes the project dependency tree. 

**uv export**: Exports the lockfile to an alternative format (e.g., requirements.txt). 

#### E.Manage virtual environment
**uv venv** : Creating virtual environment.

**source .venv/Scripts/activate**: For activating virtual environment.

**deactivate** :To exit a virtual environment.

**uv venv my-name** : A specific name or path can be specified, e.g., to create a virtual environment at my-name

**uv venv --python 3.11**: A Python version can be requested, e.g., to create a virtual environment with Python 3.11.this requires the requested Python version to be available on the system. However, if unavailable, uv will download Python for you.

**uv python install** :Install the latest stable version

**uv python install <version_identifier>**:Install a specific version 

**uv python list** :List installed Python versions

**uv python uninstall <version_identifier>** :Uninstall the desired version

## 4-Git
#### A.Set up git(Open Git Bash)
👉It  is used to set the default branch name for all future, newly initialized Git repositories on your system. The placeholder <branch_name> should be replaced with your desired name, such as main or primary.

```
git config --global init.Defaultbranch <branch_name>
```
👉Set an usename address in Git
```
git config --global user.name <username>
```

👉Set an email address in Git
```
git config --global user.email <email>
```

👉Check git configuration
```
git config --list
```

👉*main* is default branch name of repo created by git. With *git init* this branch is automatically created.*Branch* is parallel version of our project

#### B.Other git commands
👉It transforms a standard directory into a Git repository, allowing you to track changes, create versions, and collaborate with others. 

```
git init
```
👉The git status command is used to display the current state of the working directory 

```
git status
```


**git add < filename >**:The git add command is used to move changes from your working directory to the staging area .Stage a single file by name.

**git add .**:Stage every file

**git restore < filename >**:To restore file from staging area.

**git restore .**: To restore all files from staging area.

**git rm -f --cached < filename >**: for removing a file from the staging area.

**git rm -f -r --cached .**: for removing all files from the staging area.

**git commit -m "your message"**:The git commit command acts as a save point for your project, recording a snapshot of your staged changes into the local repository's history. Unlike many other version control systems, a Git commit stays on your local machine and is not shared with others until you explicitly "push" it. 

**git log**:To view the commit history of a repository. 

**git restore --source=< commit-hash > .** :You restored your working directory files to that old commit.**But your HEAD (current branch) is still at the latest commit**.So nothing is “lost” — your latest commit is still there.

**git restore .**:This restores all files back to the latest commit (HEAD)

**git branch -m master main**:To rename the local branch, if not done earlier in git bash globally.


**git checkout -f main**:  ??

#### C.Github
👉It is a cloud platform(Other plateforms are gitlab,bitbucket ) to store git repository online and collaborate with others.

👉links a local repository to a remote repository. 'origin' is the default name for the remote, and the URL points to the GitHub repository.It only connects repo, does NOT push code

```
git remote add origin <git-url>
```

👉Push the renamed local branch to the remote repository (e.g., on GitHub or GitLab). Sends your local commits → remote repo .(-u) Stands for --set-upstream.It links your local branch with remote branch.After running once this command subsequently we can use **git push** only.
```
git push -u origin main
```

👉Check if local repository pushed successfully
```
git remote -v 
```

#### D.Branch

![Img4](https://github.com/programres1/Basic-Installation/blob/main/4.png)
##### 🚀 1. Create + Switch (Modern Way ✅)
###### 🔹 Create and switch in one command
```
git switch -c new-branch
```
👉 Creates branch feature/login and switches to it

##### 🔁 2. Switch between branches
🔹 Go back to main
```
git switch main
```
🔹 Switch again to feature
```
git switch  new-branch
```

##### 🔥 3. Advanced Branching (Pro Level)
###### 🔹 Create branch from specific commit
```
git switch -c  new-branch <commit-hash>
```
###### 🔹 Create branch from another branch
```
git switch -c  new-branch source-branch
```
###### 🔹 Push new branch to remote
```
git push -u origin  new-branch
```
###### 🔹 Track remote branch
git switch --track is used to create a new branch tracking a remote branch. If the branch already exists , we simply switch to it or set upstream manually.--track is used only when branch does NOT exist locally
```
git switch --track origin/new-branch
```
###### 🔹Set upstream manually (if not tracking)
```Bash
git branch --set-upstream-to=origin/atext-enhanced
```

![Img5](https://github.com/programres1/Basic-Installation/blob/main/5.png)

##### 🧠 4. See all branches
```
git branch        # local
git branch -r     # remote
git branch -a     # all
```
##### 🔥 5. Rename branch (advanced)
```
git branch -m old-name new-name
```
##### ⚠️ 6. Delete branch (careful)
Local:
```
git branch -d  new-branch
```
Force delete:
```
git branch -D feature/login
```
git branch -D feature/login

#### E.Pull

##### 🚀 What is git pull?

👉git pull fetches changes from a remote repository and merges them into the current branch. Internally, it is a combination of git fetch and git merge.

👉 It downloads changes from remote (GitHub) and updates your local branch. Simple Meaning is it Bring latest code from remote repo into my current branch.🔍 What actually happens internally

git pull =git fetch + git merge
🔹 Step 1: git fetch

👉 Downloads latest changes from remote
👉 Does NOT modify your code

🔹 Step 2: git merge

👉 Merges those changes into your current branch

📦 Example Flow

```
git pull origin main

git pull origin atext-enhanced
```
👉 Means:

Get latest code from origin/main
Merge into your current branch
🔄 Visual Understanding
GitHub (origin/main)
        ↓ fetch
Local (origin/main)
        ↓ merge
Local (main)
✅ Common Usage
🔹 Pull latest code
```
git pull
```
👉 Works only if upstream is set (-u used earlier)

🔹 Pull from specific branch
git pull origin main
⚠️ Important Scenarios
🔴 1. Merge conflict

👉 Happens when:

You and someone else changed same code

👉 Git will ask you to resolve manually

🟡 2. Local changes present

👉 You may get:

Please commit or stash your changes
Fix:
```
git stash
git pull
git stash pop
```

#### F.Stash 
👉 git stash temporarily saves uncommitted changes, git pull fetches and merges the latest code, and git stash pop reapplies the saved changes on top of the updated code.

🔹 1. git stash
git stash

👉 Temporarily saves your uncommitted changes
👉 Cleans your working directory

🧠 Think:

"Hide my changes safely for now"

🔹 2. git pull
git pull

👉 Now your working directory is clean
👉 Git can safely download + merge latest code

🔹 3. git stash pop
git stash pop

👉 Brings back your saved changes
👉 Applies them on top of latest code

🔄 Visual Flow
Before:
Your changes + Old code

git stash
↓
Clean state

git pull
↓
Latest code

git stash pop
↓
Your changes + Latest code
⚠️ Important Things
🔴 1. Conflict can happen

👉 If same lines changed:

You’ll get merge conflict after:

git stash pop
🟡 2. Difference: pop vs apply
Command	Behavior
git stash pop	apply + delete stash
git stash apply	apply but keep stash
🔹 Check stash list
git stash list
🔹 Apply specific stash
git stash apply stash@{0}


----

🧠 First: Check your stash list
git stash list

👉 Example:

stash@{0}: WIP on main
stash@{1}: WIP on feature
🗑️ 1. Delete a specific stash
git stash drop stash@{0}

👉 Deletes only that one stash

🧹 2. Delete latest stash (most common)
git stash drop

👉 Same as:

git stash drop stash@{0}
💥 3. Delete ALL stashes
git stash clear

⚠️ Warning:
👉 Removes everything permanently

🔥 Important Difference
Command	What it does
git stash pop	apply + delete stash
git stash apply	apply but keep stash
git stash drop	delete without applying



----
when work on my branch is finshed and tested i want to merge this work into main branch. Then i will open up a pull reuest. A pull request  will let me share with my teammates for review and feedback.Once approved and merged my changes will become part of main branch.I will keep code base stable and oragnized.

Use compare and pull request or pull request tab and new pull request and fill the form and create pull reuest. Boss will review and no conflict is there and every thing seems good, he will confirm the merge.Enter comments if required Press merge pull request button.Again press confirm merge button. If you want delete that branch.

For synnc with local repo switch to main branch in local repo and then use git pull command to sysnc.

---

![Img4](https://github.com/programres1/Basic-Installation/blob/main/4.png)

![Img6](https://github.com/programres1/Basic-Installation/blob/main/6.png)

**Typical WorkFlow**

1-Clone the repository

2-Create a new branch from the main or another branch

3-Make your changes

4-Push the branch to the remote repo

5-Open a Pull Request

6-Merge the changes

7-Pull the merged changes into your local main branch

8-Repeat from step 2

#### G.Merge Conflict
A merge conflict occurs when Git cannot automatically merge changes because the same part of a file was modified differently in two branches. It must be resolved manually by editing the file and committing the result.

👉 A merge conflict happens when Git cannot automatically combine changes from two sources.

💡 In simple words:

“Git doesn’t know which change is correct”

🚨 When does it happen?
🔥 Common scenario:
You and your teammate edit the same file
Even worse → same line


----
1- branch-b commit is approved
2- boss  will swich to main branch
3-boss will use git pull to sync the code.
4-boss  will switch to main branch-a
5-Run git merge main->main will merge into branch-a, although initial purpose/objective of branch-a user was to merge his branch to main branch.
6- Atually it will show error but both branch-a and branch-b code will come in brach-a.
```
<<<<<<< HEAD(Current Change)
Manoj
=======
anu
>>>>>>> main(Incoming change)
```
7- Now take help of Merge Editor in vs code and compare manullay and have the necessary changes from both the files and discard which is not required.
8-Use git commit -am "resolved conflict" and git puch from branch-a
9- Now approve pull request in github for branch-a
10- now everybody can switch to main branch and use git pull to sysnc code from git hub

------

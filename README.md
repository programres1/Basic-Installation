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

**git config --global init.Defaultbranch <branch_name>**:It  is used to set the default branch name for all future, newly initialized Git repositories on your system. The placeholder <branch_name> should be replaced with your desired name, such as main or primary.

**git config --global user.name <username>**:Set an usename address in Git

**git config --global user.email <email>**:Set an email address in Git

**git config --list**:Check git configuration

*main* is default branch name of repo created by git. With *git init* this branch is automatically created.*Branch* is parallel version of our project

#### B.Other git commands

**git init** :It transforms a standard directory into a Git repository, allowing you to track changes, create versions, and collaborate with others. 

**git status**: The git status command is used to display the current state of the working directory 

**git add <filename>**:The git add command is used to move changes from your working directory to the staging area .Stage a single file by name.

**git add .**:Stage every file

**git restore --staged <file>**:for removing a file from the staging area while keeping your local changes intact.

**git restore --staged**: Unstages everything in your current directory at once.

**git commit -m "your message"**:The git commit command acts as a save point for your project, recording a snapshot of your staged changes into the local repository's history. Unlike many other version control systems, a Git commit stays on your local machine and is not shared with others until you explicitly "push" it. 

**git branch -m master main**:To rename the local branch.

**git push -u origin main**:Push the renamed local branch to the remote repository (e.g., on GitHub or GitLab) and reset the upstream branch.


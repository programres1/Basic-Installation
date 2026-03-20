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
## 3-Install uv
#### A.Check uv installation on Windows:
Open git bash and check **uv --version**
#### B.Install uv (pip install uv) for windows and then 
Open command promt and check **uv --version**
#### C. Upgrade uv
**pip install --upgrade uv**
## 4-uv Commands
#### A.Core Project & Dependency Management 
**uv init**: Creates a new Python project, including pyproject.toml and a .venv

**uv add <package>**: Adds dependencies and updates pyproject.toml and uv.lock.

**uv remove <package>**: Removes dependencies.

**uv sync**: Updates the virtual environment to match the uv.lock file.

**uv pip compile**: Compiles requirements in project to requirements.txt.

**uv pip sync**: Syncs virtual environment with a requirements.txt.

**uv lock**: Generates or updates the lockfile without installing packages.

**uv tree**: Visualizes the project dependency tree. 

**uv export**: Exports the lockfile to an alternative format (e.g., requirements.txt). 

#### B.Manage virtual environment
**uv venv** : Creating virtual environment.

**uv venv my-name** : A specific name or path can be specified, e.g., to create a virtual environment at my-name

**uv venv --python 3.11**: A Python version can be requested, e.g., to create a virtual environment with Python 3.11.this requires the requested Python version to be available on the system. However, if unavailable, uv will download Python for you.

**source .venv/Scripts/activate**: For activating virtual environment.

**deactivate** :To exit a virtual environment.

**uv python install** :Install the latest stable version

**uv python install <version_identifier>**:Install a specific version 

**uv python list** :List installed Python versions

**uv python uninstall <version_identifier>** :Uninstall the desired version


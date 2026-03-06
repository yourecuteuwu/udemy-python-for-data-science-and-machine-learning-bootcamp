# Overview
- Download Python and Anaconda
- Download zip files of Notebooks
- Open Juypter and explore different notebooks

What is Anaconda?
- Anaconda is a distribution of Python.
- What does a "distribution of Python mean"?
- It means that Anaconda contains not only **Python**, but other **libaries** that are popular amongst data scientists and ML / AI Engineers as well as a **virtual environment system**.

When we download Anaconda, Juypter will come installed.
- What is Juypter?
- Jupyter is an **IDE** (integrated development environment).
- What is an IDE?
- An IDE is an application you use to write code along with other bells and whistles (like correcting your syntax and compiling your code for you).

Download Anaconda by going to `anaconda.com`

Can also just do `brew install --cask anaconda` which is what I did since I am on MacOS and didn't want to enter in my email.

I then checked to make sure Anaconda was installed by running `brew list` which contained `anaconda` in the casks section and ran `/opt/homebrew/anaconda3/bin/conda init $(basename $SHELL)` which printed anaconda.

I then went into Finder and opened up `Anaconda-Navigator`.

I ended up uninstalling `anaconda` and instead brew installed `miniforge` as I was told it was better for security as well as for licensing: `brew install --cask miniforge`.

---

## How to run Juypter when installed Miniforge via Homebrew:
1. Make sure conda is installed: `conda --version`
2. Then I ran `conda create -n notebook python=3.11` to create a separate environment for the jupyter notebook
3. After that I needed to run this command: `eval "$(/opt/homebrew/Caskroom/miniforge/base/bin/conda shell.zsh hook)"` to configure terminal so that when we run the next command, we don't get an error.
4. Run `conda activate notebook` to switch over to the notebook environment (can check for all Anaconda environments by running `conda info --envs`) - you should see something like this in your terminal: `(notebook) yourname@mac ~ %`.
5. Then run `conda install jupyterlab` to install Jupyter into the Anaconda environment: notebook.
6. Then after installation is complete run `jupyter lab` and in `http://localhost:8888`, Jupyter will start running.


Additional:
- Can make a directory and put all Jupyter project in there and then run `jupyter lab` to run Jupyter

## Information on Environments
An **Anaconda environment** is an isolated directory containing a specific Python interpreter, libraries, and dependencies, separate from other projects. It prevents version conflicts, allowing you to run different project requirements simultaneously on one machine. Environments ensure project reproducibility and manage diverse packages (Python, R, binaries) efficiently. 

Key aspects of **Anaconda environments**:
Isolation: Each environment is self-contained. Installing or updating a package in one environment does not affect others or your base system.
Version Management: You can have one environment with Python 3.8 and another with 3.12, each using different versions of libraries like NumPy or Pandas.

Base Environment: Upon installation, Anaconda creates a "base" environment, which should generally be kept clean to maintain stability.
Management Commands:
- Create: `conda create --name <env_name> <packages>`
- Activate: `conda activate <env_name>`
- List: `conda info --envs`

Portability: Environments can be exported to a .yaml file to share with others, ensuring they can recreate the exact same setup. 

Creating distinct environments for each project is considered best practice, as it prevents package conflicts and allows for testing new libraries without compromising existing work. 

---

Overview:
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

---

# Pre-Commit Demo for Python Source code

The file can be used as "gist" or to demonstrate the use of pre-commit hooks within development, prio to the github/gitlap pipelines application.

The gist is used by https://pre-commit.com/, and the installation instructions are:

# Installation

Before you can run hooks, you need to have the pre-commit package manager installed.

Using pip:

     $ pip install pre-commit

Non-administrative installation:

    to upgrade: run again, to uninstall: pass uninstall to python
    does not work on platforms without symlink support (windows)

    $ curl https://pre-commit.com/install-local.py | python -

In a python project, add the following to your requirements.txt (or requirements-dev.txt):

    $ pre-commit

On a Mac, make use of [homebrew](http://brew.sh)

    $ brew install pre-commit

If you use Windows, make use of Conda (via conda-forge):

    $ conda install -c conda-forge pre-commit

# Quick start

1. Install pre-commit

Simply follow the install instructions, and pre check the  **pre-commit --version**. You should show you what version you're using, always make use of the most recent

    $ pre-commit --version
    pre-commit 2.4.0

2. Add a pre-commit configuration ¶

Create a file named .pre-commit-config.yaml, and introduce pre-commit checks by adding the content of the demo file, within a new branch

    $ git checkout -b feature/pre-commit-check
    $ touch .pre-commit-config.yaml

4. Run against all the files, and checkout what might complain about.

It's usually a good idea to run the hooks against all of the files when adding new hooks (usually pre-commit will only run on the changed files during git hooks)

    $ pre-commit run --all-files

# Content of Pre-Commit Demo file

The Demo File constist of checks, and helps to improve your source code in the following way:

* trailing-whitespace - This hook trims trailing whitespace. 
* check format of yaml, json, and xml
* check-symlinks are correct
* check-case-conflict in declarations, and imports
* check-docstrings are not forgotten as a note of the developer for himself
* check-merge-conflict are resolved before Github/lab is bothered
* end-of-file-fixer required if work happens on Windows, Linux, Unix (BSD Mac OSX) operating systems
* trailing-whitespace
* fix the format of json and pretty-format-json
* check in develop, and master branches that the imports are "pyupgrade(d)"
* add-trailing-comma, when missing
* make imports nicer, and reorder-python-imports
* get your source code opinionated organised, and understandable (with black)

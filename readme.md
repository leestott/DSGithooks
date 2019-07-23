## Githooks

### Background

Git can run custom scripts when certain actions occur like commiting to a repository, merging, pushing code, etc. We set up a client-side pre-commit hook, which runs a custom script called pre-commit in the .githooks directory of this repository.

### pre-commit

The pre-commit script is executed every time one runs git commit before Git asks the developer for a commit message.

For every .ipynb file staged to be committed, pre-commit generates corresponding .py and .html files in the scripts and html directories respectively.

.py files makes code reviews easier, since the .py files only contain code (excludes markdown comments and json associated with jupyter notebooks)

.html files make sharing notebooks easier, since one can open .html files in a browser, rather than having to start the jupyter server to view the latest content in a notebook

### Configuring Git Hooks

Ensure you are running Git version 2.9 or greater
Run the Makefile at the root of this repository with make

### Creating Custom Git Hooks

In addition to the git pre-commit hook that we have provided, other git hooks can be added to the .githooks directory. For example, one could set up a post-receive hook to send an email  when code is pushed to the repository.

For more information about creating custom git commit hooks, please refer to this [guide](https://git-scm.com/book/en/v2/Customizing-Git-Git-Hooks)

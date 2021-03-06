# Git Bulk Toolkit (gbt)

[![Build Status](https://travis-ci.com/benp44/git-bulk-toolkit.svg?branch=master)](https://travis-ci.com/benp44/git-bulk-toolkit)

A simple tool for managing and viewing the status of multiple local git repositories. Pull requests welcome

Example user stories and features of gbt:

**As a git user I'd like to see the state of my locally cloned git repos, relative to their origins**
 * Fetch on all locally cloned repos, and view a summary of upstream or local changes

**As a git user I'd like to get up to date with the origin on all my locally cloned repos**
 * Pull on all locally cloned repos

**As a git user I'd like to see what changes my team has made over multiple repos, over a set time interval**
 * View a combined commit history on all locally cloned repos

**As a git user I'd like to see which branches are ahead or behind origin/master**
 * View a list of all branches that are either ahead or behind master, and by how much

### Screenshot

![Screenshot](/screenshot.png?raw=true)

### Installation

Clone the repo and alias to the script in .bashrc, .zshrc, etc. For example:

    alias gbs='~/Development/git-bulk-toolkit/gbt fetch status'
    alias gbp='~/Development/git-bulk-toolkit/gbt pull status'
    alias gbc='~/Development/git-bulk-toolkit/gbt checkout'
    alias gbl='~/Development/git-bulk-toolkit/gbt log'
    alias gbb='~/Development/git-bulk-toolkit/gbt pull branches'

If the git-bulk-toolkit repository is among those in the development directory, then the tool will let you know when it has an update.

### Usage

When first run, gbt will ask you to select a development directory. It then operates on all git directories directly under this, so can be run from anywhere.

#### Examples

Show status for all repositories under development directory:

    gbt status

Run 'git fetch' on all repositories under development directory, and show status:

    gbt fetch status

Run 'git pull' on all repositories under development directory:

    gbt pull

Run 'git checkout master' on all repositories under development directory:

    gbt checkout master

Run 'git log' on all repositories under development directory, limited to the last `n` days, and merge the results:

    gbt log n

Show a list of all branches that are ahead or behind origin/master, for all repositories under the development directory:

    gbt branches

### Todo

* Add user-friendly way to reset development dir
* Testing... way more testing for edge scenarios - did I mention PR's welcome!?

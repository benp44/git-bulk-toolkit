# Git Bulk Toolkit (gbt)

A simple tool for managing and viewing the status of multiple local git repositories. Pull requests welcome

### Screenshot

![Screenshot](/screenshot.png?raw=true)

### Installation

Clone the repo and alias to the script in .bashrc, .zshrc, etc. For example:
  
    alias gbp='~/Development/git-bulk-toolkit/gbt fetch status'
    alias gbs='~/Development/git-bulk-toolkit/gbt pull status'
    alias gbc='~/Development/git-bulk-toolkit/gbt checkout'
    alias gbl='~/Development/git-bulk-toolkit/gbt log'

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

### Todo

* Add user-friendly way to reset development dir
* Add support for nested repos/submodules
* Testing... way more testing for edge scenarios - did I mention PR's welcome!?

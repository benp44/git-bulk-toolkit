# Git Bulk Toolkit (gbt)

A simple tool for managing multiple local git repositories.

### Screenshot

![Screenshot](/screenshot.png?raw=true)

### Installation

Clone the repo and alias to the script. For example:

    gbsStatus() {
         ~/Development/git-bulk-toolkit/gbt fetch status
    }

    gbsPull() {
        ~/Development/git-bulk-toolkit/gbt pull status
    }

    gbsCheckout() {
        ~/Development/git-bulk-toolkit/gbt checkout $1
    }
    
    alias gbp=gbsPull
    alias gbs=gbsStatus
    alias gbc=gbsCheckout

### Usage

    gbt [fetch] [pull] [status] [checkout <branch_name>]

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


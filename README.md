# git-bulk-toolkit

A simple tool for managing multiple local git repositories.

### Screenshot

![Screenshot](/screenshot.png?raw=true)

### Usage

gbt [fetch] [pull] [status] [checkout <branch_name>]

#### Examples

	gbt status
	Show status for all repositories under development directory

	gbt fetch status
	Run 'git fetch' on all repositories under development directory, and show status

	gbt pull
	Run 'git pull' on all repositories under development directory

	gbt checkout master
	Run 'git checkout master' on all repositories under development directory

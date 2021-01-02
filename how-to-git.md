# Intro to Git CVS

This doc is intended to give just enough background to motivate and explain how to:

- use someone else's material on `github.com`
- put content on `github.com` for personal storage, backup, and use on multiple computers


## Importance of CVS in Programming

Version Control Systems (VCS) are an important programming tool.
Some benefits:

- distributed backups of content
- content sharing
    - between developers
    - with users
    - a way to refer to the same version of content
- record history of changes
- interact with automated tools, eg testing
- a way to conceptually group changes

There are several VCSs, including:  Git, Subversion (svn), Mercurial (hg), and CVS.

VCSs work with most fle types, but they are most useful with text files.


## Git

We'll use Git, which is the most popular, and currently the best, CVS.
Git comes with most linux OSs, and includes the `git` executable that you run on the command line.

There are several companies that host Git repos for free.
The biggest is `github.com`.
Another is `bitbucket.org`.


## Repository

In a VCS, a group of related content in a filesystem sub-tree is called a repository.
A group of people can `clone` a repository in order to work on it together.
When they do that, they need to coordinate how they write to the repo.

Cloning is more than just a copy.
It brings meta-information about how to share info with the original repo, and the history of the files in the repo.

It can also be useful for one user to clone the repository to multiple computers.


## Clone a Github repo

Cloning is how you get the original repo onto your computer.
On `github.com`, the web page for each repo provides a url to clone it.
The process looks like this:
```
$ mkdir app
$ cd app
$ git clone <url> [directory-name]
```


## The git Command

You can get a brief summary of `git` commands like so:
```
$ git --help
```
or just:
```
$ git
```

To get explanatory, in-depth documentation, type:
```
$ man git
```

There are many sub-commands, like `git clone ...` or `git fetch ...`.
You can get brief, summary instructions for them like so:
```
$ git clone --help
```
To get explanatory, in-depth documentation, type:
```
$ man git clone
```


## Setup to use Git

Git reads the configuration file `~/.gitconfig`.
Make yours similar to this:
```ini
[user]
    name = Tony Weber
    email = anthony.weber@nissint.com
[color]
    ui = auto
[push]
    default = upstream  # `upstream` replaces the deprecated `tracking`
[alias]
    lg = log --graph --decorate --oneline
    llog = log --stat
[diff]
    tool = meld
[difftool]
    prompt = false
[difftool "meld"]
    cmd = meld "$LOCAL" "$REMOTE"
[merge]
    tool = meld
[core]
    pager = less -r
```

## The Basic Commands

```
$ git clone
$ git pull
$ git status
$ git add
$ git commit
$ git push
```


# raspberry pi setup

## Disable Passwordless Part of Sudo

By default, raspberry pi OS gives passwordless sudo to pi user.  
Turn off the passwordless part:
```
$ cd /etc/sudoers.d
$ sudo mv 010_pi-nopasswd 010_pi-nopasswd.orig
```

## Install dotfiles


## Install some tools

```
$ sudo apt install terminator tree vim
```

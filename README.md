# How to clean your sharc environment

Short version:

`mv ~/.bash_profile ~/.old_bash_profile`

## longer version

`exec env - HOME=$HOME bash`

is not a bad start.

```
LS_COLORS
LANG
LESSOPEN
```

Turns out things like "color `ls`" is an alias.

```
$ alias ls
alias ls='ls --color=auto'
```

The alias is set in `/etc/profile.d/colorls.sh`.

For login shells, the system wide `/etc/profile` will source this file.

For other shells, they will (typically) source `~/.bashrc` which sources `/etc/bashrc`,
which also sources the contents of `/etc/profile/*.sh` in a loop.

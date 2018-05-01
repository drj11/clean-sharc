# clean-sharc
How to clean your sharc environment

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
Where is that sourced from?
Perhaps it is `/etc/bashrc` ?


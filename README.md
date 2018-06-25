# configs
Repo of my linux configs to aid in distrohopping

### .bashrc

```
# .bashrc

# User specific aliases and functions

#alias rm='rm -i'
alias cp='cp -i'
#alias mv='mv -i'

# Source global definitions
if [ -f /etc/bashrc ]; then
        . /etc/bashrc
fi
export PS1="\u@\h:\w\\$ \[$(tput sgr0)\]"
```

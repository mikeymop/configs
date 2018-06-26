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

# Support KDE Blur in konsole transparency

if [[ $(ps --no-header -p $PPID -o comm) =~ yakuake|konsole ]]; then
        for wid in $(xdotool search --pid $PPID); do
            xprop -f _KDE_NET_WM_BLUR_BEHIND_REGION 32c -set _KDE_NET_WM_BLUR_BEHIND_REGION 0 -id $wid; done
fi

```

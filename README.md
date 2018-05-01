Enviro-setup
============

### IDE:
- [VScode](https://code.visualstudio.com/download)
- [Atom](https://atom.io/)
- [Hyper](https://hyper.is/)

### PACKAGE MANAGERS:
- [npm](https://www.npmjs.com/get-npm)
- [brew](https://brew.sh/)
  *Or just paste this line in the terminal*
  `/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"`

### Design:
- [Zeplin](https://zeplin.io/) *Design -> Dev*

### Chrome extensions:
- [Vimium](https://chrome.google.com/webstore/search/vimium?hl=en) *VIM-esk keyboard shortcuts for browser*

### Miscellaneous:
- [Spectacle](http://www.spectacleapp.com) *Mac window control*

### bash_profile
```
export PS1="\[\e[34m\] [\d \T] \[\e[36m\]\w $ "

if [ -f ~/.bashrc ]; then
        source ~/.bashrc
fi
```

### bashrc:
```
## *most utils have a GNU version and BSD version. Linux take the GNU version while OSX may take a BSD version, so options for those commands may differ.

# Checking which environment and assign appropriate ls alias
_myos="$(uname)"

case $_myos in
  Linux) alias ls='ls --color';;
  Darwin) alias ls='ls -G';;
  *) ;;
esac

# ----------------------
# General Aliases
# ----------------------

# Directory shortcuts #
alias beats='cd ~/Documents/Beats'

# ls command output ----#

alias ll='ls -la'

## Show hidden files ##
alias l.='ls -d .* --color=auto'

#---- cd command behaviour ----#

## Get rid of command not found ##
alias cd..='cd ..'

## Shortcut to get out of cuurent directory ##
alias ..='cd ..'
alias ...='cd ../../../'
alias ....='cd ../../../../'
alias .....='cd ../../../../../'
alias .4='cd ../../../../'
alias .5='cd ../../../../../'
```
### Git config 
```
[alias]

### BASIC LOG COMMANDS ###

ls = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate
ll = log --pretty=format:"%C(yellow)%h%Cred%d\\ %Creset%s%Cblue\\ [%cn]" --decorate

### SHOW HISTORY OF A FILE, WITH DIFFS ###

filelog = log -u
fl = log -u

### LOG COMMANDS TO INSPECT (RECENT) HISTORY ###

dl = "!git ll -1"
dlc = diff --cached HEAD^
dr  = "!f() { git diff "$1"^.."$1"; }; f"
lc  = "!f() { git ll "$1"^.."$1"; }; f"
diffr  = "!f() { git diff "$1"^.."$1"; }; f"

### LIST ALL ALIASES (la) ###
la = "!git config -l | grep alias | cut -c 7-"

### BASIC SHORTCUTS ###
cp = cherry-pick
st = status -s
cl = clone
co = checkout
br = branch
diff = diff --word-diff
dc = diff --cached

### RESET COMMANDS ###
r = reset
r1 = reset HEAD^
r2 = reset HEAD^^
rh = reset --hard
rh1 = reset HEAD^ --hard
rh2 = reset HEAD^^ --hard

### STASH OPERATIONS ###
sl = stash list
sa = stash apply
ss = stash save
```

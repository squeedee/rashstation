# dotfiles

## Assumptions

- You are using bash

## Installation

### Install [homebrew](https://brew.sh)

```
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

### Clone this repo

```
git clone https://github.com/squeedee/rashstation.git
```

### Install [rcm](https://github.com/thoughtbot/rcm)

```
brew install thoughtbot/formulae/rcm
```

### Install the dotfiles

```
RCRC="${HOME}/rashstation/dotfiles/rcrc" rcup -v
```

## Optional

### Install the specified formulae and casks

```
brew bundle --global
```

### Install a new key for github etc

```shell
ssh-keygen -f ~/.ssh/id_github # this file is in the ssh config so don't use a different name unless you want to mess with dotfiles 
ssh-add -K ~/.ssh/id_github.pub
ssh-keygen -y -f ~/.ssh/id_github | pbcopy
# Public key is in your buffer, paste it into github
```

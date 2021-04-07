# zsh + tmux

## Requirement

```
sudo apt update
sudo apt install tmux zsh grc git curl
mkdir -p ~/.ssh
```

## Install
### ZSH

```
sh -c "$(curl -fsSL https://raw.github.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
ZSH_PATH=$(grep -oP '^export ZSH="\K[^"]+' ~/.zshrc)
cp zshrc ~/.zshrc
sed -i -e "s|#ZSH_PATH#|${ZSH_PATH}|g" ~/.zshrc
```
### Zgen
```
git clone https://github.com/tarjoilija/zgen.git "${HOME}/.zgen"
source "${HOME}/.zgen/zgen.zsh"
```
### TMUX
```
cp tmux.conf ~/.tmux.conf
cp tmux.local.conf ~/.tmux.local.conf
cp -Rf tmux/* ~/tmux/
```

### Font
**Linux :**

https://github.com/romkatv/powerlevel10k#how-was-the-recommended-font-created

**WSL :**
Install Powerline, Windows compatible font from this repo https://github.com/ryanoasis/nerd-fonts. You need to install version 1.2.0 since version 2.0.0 don't work with Windows.

Download this asset https://github.com/ryanoasis/nerd-fonts/releases/download/v1.2.0/DejaVuSansMono.zip. Unzip file and install the DejaVu Sans Mono for Powerline Nerd Font Complete Mono Windows Compatible.ttf font by right-clicking on the file and select install.

> Don't forget to set policy "PowerLine" on your terminal !

## Usage

Tmux Shortcut : CTRL + A
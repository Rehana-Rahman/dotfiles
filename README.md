# Dotfiles and Scripts for Termux + Linux

This repository contains my personal shell setup — Zsh, Powerlevel10k, Neovim, and a few custom scripts.  
It’s designed to work seamlessly inside **Termux (Android)** and on **Linux distros** like Ubuntu or Arch.

---

## Prerequisites

### On Termux
```
pkg update && pkg upgrade -y
pkg install git zsh neovim curl wget -y
```

### On Ubuntu / Debian
```
sudo apt update && sudo apt install git zsh neovim curl wget -y
```

### On Arch Linux
```
sudo pacman -Syu git zsh neovim curl wget --noconfirm
```

Then install Powerlevel10k and a Nerd Font (for icons):
```
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ~/.powerlevel10k
```
Set your terminal font to a Nerd Font (JetBrainsMono, FiraCode, etc.).

---

## Installation Steps

Clone this repo:
```
git clone https://github.com/Rehana-Rahman/dotfiles.git ~/dotfiles && cd ~/dotfiles
```

Run the setup script:
```
bash setup.sh
```

### This script will
- Symlink `.zshrc` and `.p10k.zsh` to your `$HOME`
- Link your Neovim config to `~/.config/nvim`
- Copy or link custom scripts to `~/bin` or `~/.local/bin`
- Detect whether it’s Termux or Linux and adjust paths automatically

Then reload your shell:
```
exec zsh
```

---

## Folder Structure

```
dotfiles/
├── nvim/             # Neovim config
├── scripts/          # Custom shell/Python utilities
├── .zshrc            # Zsh configuration
├── .p10k.zsh         # Powerlevel10k prompt config
├── setup.sh          # Installs / links configs dynamically
└── README.md
```

---

## Notes

- Works across Termux, Ubuntu, Arch, and other Unix-like environments.  
- The setup script handles platform detection automatically.  
- Portable and easy to rebuild your dev environment anywhere.

---

## Example Usage

```
# On Termux
bash setup.sh termux

# On Ubuntu / Arch
bash setup.sh linux

# Test configs
zsh
nvim ~/.zshrc
```

---

>>> “New machine? Clone, run, zsh and I’m home again.”



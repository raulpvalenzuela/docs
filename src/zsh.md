# zsh

## General stuff

- Which is the current shell?

  ```bash
  echo $SHELL
  ```

- List available shells

  ```bash
  chsh -l
  ```

- Change default shell to bash or zsh

  ```bash
  chsh -s /bin/bash
  ```

  ```bash
  chsh -s /bin/zsh
  ```

## ZSH installation

### Package installation

1. Installation:

   ```bash
   sudo pacman -S zsh
   ```

## oh-my-zsh installation

### Source

`https://github.com/ohmyzsh/ohmyzsh`

### Manual installation

1. Clone the repository

   ```bash
   git clone https://github.com/ohmyzsh/ohmyzsh.git ~/.config/oh-my-zsh/.oh-my-zsh
   ```

2. Replace zsh configuration file with template

    ```bash
    cp ~/.config/oh-my-zsh/.oh-my-zsh/templates/zshrc.zsh-template ~/.zshrc
    ```

## powerlevel10k theme installation

### Source

[https://github.com/romkatv/powerlevel10k](https://github.com/romkatv/powerlevel10k)

## Package installation

1. Installation

   ```bash
   yay -S --noconfirm zsh-theme-powerlevel10k-git
   ```

2. Source powerlevel10k theme from .zshrc

   ```bash
   echo 'source /usr/share/zsh-theme-powerlevel10k/powerlevel10k.zsh-theme' >>~/.zshrc
   ```

3. On the first run, Powerlevel10k configuration wizard will ask you a few questions and configure your prompt. If it doesn't trigger automatically, type p10k configure. Configuration wizard creates ~/.p10k.zsh based on your preferences. Additional prompt customization can be done by editing this file.

**IMPORTANT NOTE:** There is also zsh-theme-powerlevel10k community package. Historicaly, it has been breaking often and for extended periods of time. Do not use it.

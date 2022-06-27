# dhruvi's dotfiles

## Brewfile

### Install

1. Install [`Homebrew`](https://brew.sh/)
2. Run `brew bundle` from the Brewfile directory

### Generate Brewfile

This will also dump applications installed using [`mas`](https://github.com/mas-cli/mas)

```
brew bundle dump
```

## Install

1. Clone the repo to the local machine
2. Use symlinks for the wanted files from the repo

```
ln -s ~/dotfiles/.zshrc ~/.zshrc
ln -s ~/dotfiles/.aliases ~/.aliases
ln -s ~/dotfiles/.gitconfig ~/.gitconfig
ln -s ~/dotfiles/.gitignore ~/.gitignore
ln -s ~/dotfiles/.vimrc ~/.vimrc
ln -s ~/dotfiles/.config/starship.toml ~/.config/starship.toml
```

## iTerm

Use `Terminal` to setup iTerm

1. Install a [nerd font](https://www.nerdfonts.com/)
    - This step will be done if the Brewfile was ran
2. Ensure that the ```~/.iterm``` directory exists with a file ```com.googlecode.iterm2.plist```
    - If ```~/.iterm`/com.googlecode.iterm2.plist``` does not exist:
        - Create directory ```~/.iterm```
        - Open iTerm -> Preferences and check the box to "Load preferenes from a custom foler or URL"
3. Delete ```com.googlecode.iterm2.plist``` in ```~/.iterm```
3. Symlink the configuration file from this repository to ```Users/dhruvisompura/.iterm/com.googlecode.iterm2.plist```
5. Make sure preferences are being loaded from `~/.iterm`

### Git Config

The `.gitconfig.local` file is included by `.gitconfig`. Use it to store user
information.

```
[user]
    name = Dhruvi Sompura
    email = fake@invalid.com
```

## Optional tools

- [`bat`](https://github.com/sharkdp/bat)
- [`fzf`](https://github.com/junegunn/fzf)
- [`fd`](https://github.com/sharkdp/fd)
- [ripgrep `rg`](https://github.com/BurntSushi/ripgrep)
- [`starship`](https://starship.rs/)

### Commit Messages

Messages should start with the affected `[software]`

If there is not a specific piece of software the commit targets then it can be
excluded

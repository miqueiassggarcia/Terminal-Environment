# Terminal-Environment
<p>All installations procedures is based on Ubuntu</p>

## Instalar [zsh](https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH)
```bash
sudo apt install zsh
```
#### Define zsh as default and reboot the system
```bash
sudo chsh -s $(which zsh)
```

## Install [oh-my-zsh](https://ohmyz.sh/)
#### Install depedencies
```bash
sudo apt install curl git
```

#### Install oh-my-zsh
```bash
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
```
### Add oh-my-zsh plugins
#### zsh-autosuggestions
```bash
git clone https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
```

#### Add the new plugin to .zshrc list
```bash
plugins=( 
    # other plugins...
    zsh-autosuggestions
)
```

#### zsh-autosuggestions
```bash
git clone https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
```

#### Add the new plugin to .zshrc list
```bash
plugins=( 
    # other plugins...
    zsh-syntax-highlighting
)
```

## Install [exa](https://the.exa.website/)
```bash
sudo apt install exa
```

#### This is my aliases, change as you need
```bash
alias ls="exa -lbF --icons"
alias l="exa -lbhmua --time-style=long-iso --color-scale --icons"
alias lx="exa -lbhHigmuSa@ --time-style=long-iso --color-scale --icons"
alias llt="exa -l --tree --icons"
alias lt="exa --tree --level=2 --icons"
alias llm="exa -lbGF --sort=modified --icons"
alias lld="exa -lbhHFGmuSa --group-directories-first --icons"
```

## Install [powerlevel10k](https://github.com/romkatv/powerlevel10k)
```bash
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
```

#### Set ZSH_THEME="powerlevel10k/powerlevel10k" in ~/.zshrc

#### Install the [recomended fonts](https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#meslo-nerd-font-patched-for-powerlevel10k)

## Install [fd](https://github.com/sharkdp/fd)
```bash
sudo apt install fd-find
```

#### Create a soft link
```bash
sudo ln -s $(which fdfind) /usr/bin/fd
```

## Install [bat](https://github.com/sharkdp/bat)
```bash
sudo apt install bat
```

#### Create a soft link
```bash
sudo ln -s $(which batcat) /usr/bin/bat
```

## Install [ripgrep](https://github.com/BurntSushi/ripgrep)
```bash
sudo apt-get install ripgrep
```


## Install [fzf](https://github.com/junegunn/fzf)
```bash
sudo apt install fzf
```

## Install [asdf](https://asdf-vm.com/)
```bash
git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.13.1
```

add . "$HOME/.asdf/asdf.sh" in your .zshrc

## Install [broot](https://github.com/Canop/broot) and [difftastic](https://github.com/Wilfred/difftastic)
#### Install rust
```bash
curl --proto '=https' --tlsv1.2 -sSf https://sh.rustup.rs | sh
```

#### Install dependencies
```bash
sudo apt install build-essential libxcb1-dev libxcb-render0-dev libxcb-shape0-dev libxcb-xfixes0-dev -y
```

#### Install broot and difftastic with cargo
```bash
cargo install --locked broot

source "$HOME/.cargo/env"

broot

cargo install --locked difftastic
```

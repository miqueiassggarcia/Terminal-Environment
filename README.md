# Terminal-Environment

Instalar zsh
apt install zsh
https://github.com/ohmyzsh/ohmyzsh/wiki/Installing-ZSH
sudo chsh -s $(which zsh)
reboot

Instalar oh-my-zsh
https://ohmyz.sh/
apt install curl
apt install git
sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"

Install powerlevel10k
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
Set ZSH_THEME="powerlevel10k/powerlevel10k" in ~/.zshrc
Install the recomended fonts https://github.com/romkatv/powerlevel10k?tab=readme-ov-file#meslo-nerd-font-patched-for-powerlevel10k
https://github.com/romkatv/powerlevel10k

sudo apt install fd-find
https://github.com/sharkdp/fd
sudo ln -s $(which fdfind) /usr/bin/fd

sudo apt install bat
https://github.com/sharkdp/bat
sudo ln -s $(which batcat) /usr/bin/bat

sudo apt-get install ripgrep
https://github.com/BurntSushi/ripgrep

sudo apt install fzf
https://github.com/junegunn/fzf

git clone https://github.com/asdf-vm/asdf.git ~/.asdf --branch v0.13.1
add . "$HOME/.asdf/asdf.sh" in .zshrc
https://asdf-vm.com/

# Steps

```bash
# normal updates
sudo apt update
sudo apt upgrade

# dependencies
sudo apt install clang clangd stow libfuse2 wget tmux unzip zip python3-venv -y

# if you want to install neovim the hard way in any other distro other than arch

wget https://github.com/neovim/neovim/releases/download/stable/nvim.appimage

sudo mkdir /usr/local/bin 

chmod u+x nvim.appimage

sudo mv nvim.appimage /usr/local/bin/nvim

# install tpm and nvchad

git clone https://github.com/tmux-plugins/tpm ~/.tmux/plugins/tpm
git clone https://github.com/NvChad/NvChad ~/.config/nvim --depth 1

# final configs

mkdir -p ~/.config/nvim/lua/custom/configs/
mkdir -p ~/.config/tmux 

# zsh (on arch)

sudo pacman -Syu zsh
sudo pacman -Syu openssh which

# follow instructions on https://beebom.com/how-install-zsh-and-oh-my-zsh-linux/

rm -rf ~/.zshrc ~/.bashrc ~/.profile


# stow things

stow .

# final setup
# open nvim, type ':MasonInstallAll'
# open tmux, type 'Ctrl + space + I'

```

# Install and config nix


```bash
# install nix-os
# https://mirrors.tuna.tsinghua.edu.cn/help/nix/
sh <(curl -L https://mirrors.tuna.tsinghua.edu.cn/nix/latest/install) --daemon

# install home-manager
# https://nix-community.github.io/home-manager/index.xhtml#sec-install-standalone
nix-channel --add https://github.com/nix-community/home-manager/archive/master.tar.gz home-manager
nix-channel --update

nix-shell '<home-manager>' -A install



git clone https://github.com/andylin-hao/nix-config.git

## cat /etc/nix/nix.conf 
## experimental-features = nix-command flakes
## build-users-group = nixbld

home-manager switch --flake .#yuanqingwang@Laptop


# install brew
/bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"

# install SF Mono Nerd Font
# https://github.com/epk/SF-Mono-Nerd-Font

brew tap epk/epk
# Homebrew >= 2.6.0
brew install font-sf-mono-nerd-font
```
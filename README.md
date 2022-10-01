# mint.dotfiles

mint + xfce4

### Theme
**DE/WM**

```
$ apt install -y git arc-theme
```

```
$ xfconf-query -c xsettings -p /Net/ThemeName -s Arc-Dark
$ xfconf-query -c xfwm4 -p /general/theme -s Arc-Dark
```

**Icon**

```
$ sudo add-apt-repository -y ppa:papirus/papirus && apt update
$ apt install -y papirus-icon-theme
```

```
$ xfconf-query -c xsettings -p /Net/IconThemeName -s ePapirus-Dark
```

**Desktop**
Wallpaper link [here](https://www.xfce-look.org/p/1483687)

```
$ mv 'XFCE 94 With Logo.png' ~/Pictures/wallpaper.png
$ xfconf-query -c xfce4-desktop -p /backdrop/screen0/monitoreDP/workspace0/last-image -s ~/Pictures/wallpaper.png
```

**Font**
```
$ apt install -y fonts-firacode
```

**VS Code**

extensions:
```
code --install-extension smlombardi.slime
code --install-extension vscode-icons-team.vscode-icons
code --install-extension mortim.noc
code --install-extension ms-python.python
code --install-extension justusadam.language-haskell
code --install-extension redhat.java
code --install-extension ms-vscode.cpptools
code --install-extension shd101wyy.markdown-preview-enhanced
code --install-extension yzhang.markdown-all-in-one
```

config:
```
curl https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/vscode/settings.json > ~/.config/Code/User/settings.json
```

### Packages
```
$ apt install -y neofetch git vim wget curl virtualbox steam feh
```

- [VSCode](https://code.visualstudio.com/) package (with the dpkg package manager)
- [Haskell](https://www.haskell.org/ghcup/) package
- OpenJDK

### VPN
```
$ wget https://infotuto.univ-lille.fr/fileadmin/user_upload/infotuto/images/DSI/Fichiers_telechargeables/Clients_VPN/ULILLE_VPN_ETUDIANT_Linux_v4_2.zip
$ unzip ULILLE_VPN_ETUDIANT_Linux_v4_2.zip
$ nmcli connection import type openvpn file ULILLE_VPN_ETU_TCP_v4_Linux.ovpn
```


### Shell configuration
```
$ cd ~
```

```
$ echo -e "\n\nexport PATH=$HOME/.local/bin:$PATH" >> .bashrc
```

**iJava**

```
$ wget https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/lib/program.jar -P Workspace/iut/lib
$ curl https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/bash/.bash_aliases > .bash_aliases
$ source .bash_aliases
```

**Ghci**

```
$ wget https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/ghci/.ghci
$ chmod go-w .ghci
```
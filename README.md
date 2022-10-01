# mint.dotfiles

mint + xfce4

**Pre-requisites**
```
apt install wget curl
```

### Theme
**DE/WM**

```
$ apt install -y git arc-theme
```

```
$ xfconf-query -c xsettings -p /Net/ThemeName -s Arc-Dark
$ xfconf-query -c xfwm4 -p /general/theme -s Arc-Dark
```

```
$ xfconf-query -c xfwm4 -p /general/show_dock_shadow -s false
$ xfconf-query -c xfwm4 -p /general/show_frame_shadow -s false
```

**Icon**

```
$ sudo add-apt-repository -y ppa:papirus/papirus && apt update
$ apt install -y papirus-icon-theme
```

```
$ xfconf-query -c xsettings -p /Net/IconThemeName -s ePapirus-Dark
```

**Terminal**

```
$ curl https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/xfce4-terminal/terminalrc > ~/.config/xfce4/terminalrc
```
**Panel**

```
$ xfconf-query -c xfce4-panel -p /panels/panel-1/enter-opacity -s 95
$ xfconf-query -c xfce4-panel -p /panels/panel-1/leave-opacity -s 95
```

**Desktop**

```
$ xfconf-query -c xfce4-desktop -p /desktop-icons/file-icons/show-home -s false
```

Wallpaper link [here](https://www.xfce-look.org/p/1483687)

```
$ mv 'XFCE 94 With Logo.png' ~/Pictures/wallpaper.png
$ xfconf-query -c xfce4-desktop -p /backdrop/screen0/monitor$(xrandr --listmonitors | grep "+" | awk {'print $4'})/workspace0/last-image -s ~/Pictures/wallpaper.png
```

**Font**
```
$ apt install -y fonts-firacode
```

---

### Packages
```
$ apt install -y neofetch git vim virtualbox steam feh g++
```

- [VSCode](https://code.visualstudio.com/) package (with the dpkg package manager)
- [Haskell](https://www.haskell.org/ghcup/) package
- OpenJDK

**VS Code**

extensions:
```
curl https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/scripts/install_vscode_ext.sh | sh
```

config:
```
curl https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/vscode/settings.json > ~/.config/Code/User/settings.json
```

---

### VPN
```
$ wget https://infotuto.univ-lille.fr/fileadmin/user_upload/infotuto/images/DSI/Fichiers_telechargeables/Clients_VPN/ULILLE_VPN_ETUDIANT_Linux_v4_2.zip
$ unzip ULILLE_VPN_ETUDIANT_Linux_v4_2.zip
$ nmcli connection import type openvpn file ULILLE_VPN_ETU_TCP_v4_Linux.ovpn
```

---

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
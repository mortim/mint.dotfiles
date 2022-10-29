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
$ curl https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/xfce4-terminal/terminalrc > ~/.config/xfce4/terminal/terminalrc
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
$ xfconf-query -c xfce4-desktop -p /backdrop/screen0/monitor$(xrandr --listmonitors | grep "+" | cut -d " " -f 6)/workspace0/last-image -s ~/Pictures/wallpaper.png
```

**Font**
```
$ apt install -y fonts-firacode
```

---

### Packages
```
$ apt install -y neofetch git vim openjdk-11-jdk virtualbox steam feh g++ filezilla
```

- [VSCode](https://code.visualstudio.com/) package (with the dpkg package manager)
- [Haskell](https://www.haskell.org/ghcup/) package
  
**VS Code**

extensions:
```
$ curl https://raw.githubusercontent.com/mortim/mint.dotfiles/master/bin/install_vscode_ext | sh
```

config:
```
$ curl https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/vscode/settings.json > ~/.config/Code/User/settings.json
```

**Python**
(check the **Bash** configuration to export ~/.local/bin directory)

```
$ curl https://bootstrap.pypa.io/get-pip.py | python3
```

**Virtualbox**
(download Windows VM [here](https://nextcloud.univ-lille.fr/index.php/s/8JN6FYEJo35H4nE))

```
$ wget https://nextcloud.univ-lille.fr/index.php/s/8JN6FYEJo35H4nE/download/Windows%2010.ova
$ VBoxManage import 'Windows 10.ova'
```

---

### VPN
```
$ wget https://infotuto.univ-lille.fr/fileadmin/user_upload/infotuto/images/DSI/Fichiers_telechargeables/Clients_VPN/ULILLE_VPN_ETUDIANT_Linux_v4_2.zip
$ unzip ULILLE_VPN_ETUDIANT_Linux_v4_2.zip -d vpn
$ nmcli connection import type openvpn file vpn/ULILLE_VPN_ETU_TCP_v4_Linux.ovpn
$ rm -r vpn ULILLE_VPN_ETUDIANT_Linux_v4_2.zip
```

---

### Keyboard shortcuts

Use the official GUI software from Xfce for keyboard settings

| Shortcut  | Description  | Command  |
|    ---    |     ---      |   ---    |
| Alt + T  | File explorer  | thunar  |
| Alt + F  | Web browser  | firefox  |
| Alt + D  | Instant messaging software | discord
| Shift + Print  | Screenshot region  | xfce4-screenshooter -r  |
| Alt + Print  | Screenshot the active window  | xfce4-screenshooter -w  |
| Ctrl + Print  | Screenshot fullscreen  | xfce4-screenshooter -f  |

---

### Shell configuration
```
$ cd ~
```

**Bash**

```
$ echo -e '\nexport PATH=~/.local/bin:$PATH' >> .bashrc
$ source .bashrc
```

**iJava**

```
$ wget https://raw.githubusercontent.com/mortim/mint.dotfiles/master/lib/program.jar -P Workspace/iut/lib
$ curl https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/bash/.bash_aliases > .bash_aliases
$ source .bash_aliases
```

**Ghci**

```
$ wget https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/ghci/.ghci
$ chmod go-w .ghci
```

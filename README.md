# dotfiles

### Installation
---

##### Theme
- Arc (Dark)
- Paper (Icon)

```
sudo apt install arc-theme
```
```
sudo add-apt-repository ppa:snwh/ppa && sudo apt update
sudo apt install paper-icon-theme
```

##### Typography
```
sudo apt install fonts-firacode
```

##### Packages
*pre-installed: libreoffice, firefox*

(Desktop)
**For virtualbox package, DISABLE the secure boot**
```
sudo apt install redshift vlc gimp virtualbox neofetch
```
[Discord](https://discord.com/) and [Hakuneko](https://github.com/manga-download/hakuneko/releases/tag/v6.1.7) packages are installed with a deb file.
```
sudo dpkg -i discord.deb
sudo dpkg -i hakuneko.deb
``` 

(OBS Studio)
```
sudo apt install ffmpeg
sudo add-apt-repository ppa:obsproject/obs-studio
sudo apt update
sudo apt install obs-studio
```

(Games)
```
sudo add-apt-repository ppa:lutris-team/lutris
sudo apt install lutris
sudo apt install steam
```

(Dev)
[VS Code](https://code.visualstudio.com/) package is installed with a deb file.
```
sudo dpkg -i vscode.deb
```

```
sudo apt install python3.9 python3-pip haskell-platform git vim
```

```
curl -sSL https://get.haskellstack.org/ | sh
```

---

## Config

The configurations are available [here](here).

#### Hide the password
```
rm - /etc/sudoers.d/Opwfeedback
```

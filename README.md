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

**Font**
```
$ apt install -y fonts-firacode
```

(check the [VSCode](config/vscode/settings.json) configuration)

### Packages
```
$ apt install -y neofetch git vim wget curl
```

- [VSCode](https://code.visualstudio.com/) package (with the dpkg package manager)
- [Haskell](https://www.haskell.org/ghcup/) package
- OpenJDK


### Shell configuration
```
$ cd ~
```

```
$ echo -e "\n\nexport PATH=$HOME/.local/bin:$PATH" >> .bashrc
```

---

**(for cs studies)**

```
$ wget https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/programs/program.jar -P Workspace/iut/
```

---

```
$ curl https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/bash/.bash_aliases > .bash_aliases
$ source .bash_aliases
```

```
$ wget https://raw.githubusercontent.com/mortim/mint.dotfiles/master/config/ghci/.ghci
$ chmod go-w .ghci
```
<details><summary>dependencies fresh install arch</summary>

```
sudo pacman -Syu --needed git libnotify fontconfig fastfetch slock imagemagick stow alacritty dunst tmux zsh unclutter awesome kitty rofi conky fish lf nsxiv picom redshift systemd xf86-input-libinput gimp gnupg pass zathura zoxide wget alsa-utils eza flameshot gpick python-pip --noconfirm
```
  
</details>

---

# .Archdots install

```
cd ~
git clone https://github.com/Paulobox/.Archdots
```

```
cd ~/.Archdots
stow zsh shell x11 alacritty kitty nsxiv tmux myscripts rofi vscode fish lf picom dunst zathura
sudo rm ~/.zprofile ~/.xprofile
sudo ln -s ~/.config/shell/profile ~/.zprofile
chmod +x ~/.config/shell/profile
sudo ln -s ~/.config/x11/xprofile ~/.xprofile
chmod +x ~/.config/x11/xprofile
source ~/.config/zsh/.zshrc
```

##### for scripts make [symbolic links](https://github.com/Paulobox/.dotfiles/blob/main/myscripts/.myscripts/README.md)


## remove symbolic links:

`
find ~/.config -xtype l -delete
`

```
setopt dotglob
mv -f *(D) ../ 2>/dev/null
```

```
mv -f * ~/.config/ 2>/dev/null
```

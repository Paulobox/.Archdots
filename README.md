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
source ~/.zshrc
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

# .Archdots install

```
cd ~
git clone https://github.com/Paulobox/.Archdots
```

```
cd ~/.Archdots/.dotfiles
stow -t ~ x11 alacritty mocp nsxiv tmux awesome i3 kitty myscripts rofi vscode conky fish lf picom dunst zathura --adopt
```

##### for scripts make [symbolic links](https://github.com/Paulobox/.dotfiles/blob/main/myscripts/.myscripts/README.md)

## link profiles

```
sudo ln -s ~/.config/shell/profile ~/.zprofile
sudo ln -s ~/.config/x11/xprofile ~/.xprofile
```

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

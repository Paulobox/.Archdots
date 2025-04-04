## link profiles

```
sudo ln -s ~/.config/shell/profile ~/.zprofile
sudo ln -s ~/.config/x11/xprofile ~/.xprofile
```

# remove symbolic links:

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

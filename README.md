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

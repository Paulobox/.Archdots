<details><summary>dependencies fresh install arch</summary>

```
sudo pacman -Syu --needed git jq xclip libnotify fontconfig fastfetch slock imagemagick stow alacritty dunst tmux zsh unclutter awesome kitty rofi conky fish lf nsxiv picom redshift systemd xf86-input-libinput gimp gnupg pass zathura zoxide wget alsa-utils eza flameshot gpick python-pip --noconfirm
```

</details>

<details><summary>Audio</summary>

```
sudo pacman -S --needed pipewire pipewire-pulse wireplumber pipewire-alsa alsa-utils sof-firmware
sleep 3
systemctl --user status pipewire pipewire-pulse wireplumber
sleep 3
systemctl --user enable --now pipewire pipewire-pulse wireplumber
```

</details>

---

<details open><summary>  .Archdots install </summary>

```
cd ~
git clone https://github.com/Paulobox/.Archdots
cd ~/.Archdots
stow zsh shell x11 alacritty kitty nsxiv tmux myscripts rofi vscode fish lf picom dunst zathura
sudo rm ~/.zprofile ~/.xprofile
sudo ln -s ~/.config/shell/profile ~/.zprofile
chmod +x ~/.config/shell/profile
sudo ln -s ~/.config/x11/xprofile ~/.xprofile
chmod +x ~/.config/x11/xprofile
source ~/.config/zsh/.zshrc
```

</details>

<details><summary> [oh-my-zsh](https://ohmyz.sh/), note: variables must interfere like ZDOTDIR in profile</summary>

```
sudo rm -rf ~/.oh-my-zsh
cd ~
unset ZDOTDIR
echo "Y" | sh -c "$(curl -fsSL https://raw.githubusercontent.com/ohmyzsh/ohmyzsh/master/tools/install.sh)"
git clone --depth=1 https://github.com/zsh-users/zsh-syntax-highlighting.git ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-syntax-highlighting
git clone --depth=1 https://github.com/zsh-users/zsh-autosuggestions ${ZSH_CUSTOM:-~/.oh-my-zsh/custom}/plugins/zsh-autosuggestions
git clone --depth=1 https://github.com/romkatv/powerlevel10k.git ${ZSH_CUSTOM:-$HOME/.oh-my-zsh/custom}/themes/powerlevel10k
sleep 1
sudo rm -rf ~/.zshrc
sudo ln -s ~/.config/zsh/.zshrc ~
source ~/.zshrc
```

</details>

<br>


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

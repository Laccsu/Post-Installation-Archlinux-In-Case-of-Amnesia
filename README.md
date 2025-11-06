# Post Installation Archlinux In Case of Amnesia

Git and other necessary packages
```
sudo pacman -S git vim --noconfirm
```

Yay for AUR Packages
```
git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si
```

SOF Firmware for audio
```
sudo pacman -S sof-firwmare --noconfirm
```

Mkinitcpio Firmware 
```
yay -S mkinitcpio-firmware --noconfirm --removemake
```

Update Grub AUR Package
```
yay -S update-grub --noconfirm --removemake
```

UFW Firewall
```
sudo pacman -S ufw --noconfirm
sudo ufw default deny
sudo ufw enable
sudo systemctl enable ufw
```

Fonts and emojis:
```
sudo pacman -S noto-fonts-cjk noto-fonts-emoji ttf-jetbrains-mono-nerd inter-font --noconfirm
```

File management
```
sudo pacman -S ark p7zip unrar unzip zip --noconfirm
```

TLP for notebook battery
```
sudo pacman -S tlp --noconfirm
sudo systemctl enable tlp
sudo systemctl start tlp
```

Useful commands:
```
sudo pacman -Syyu --noconfirm # Update
```
```
sudo pacman -Scc --noconfirm # Clear cache
```
```
sudo pacman -Rns $(pacman -Qdtq) # Remove Unused Packages
```
```
yay -Syyu --noconfirm # Update AUR Packages
```

VLC, Obsidian and other apps
```
flatpak install flathub org.videolan.VLC
flatpak install flathub md.obsidian.Obsidian
flatpak install flathub org.qbittorrent.qBittorrent
```
```
yay -S vscodium-bin --noconfirm --removemake
```  

Terminal
```
sudo pacman -S ghostty --noconfirm
```

Completo
```
sudo pacman -S git vim sof-firmware ghostty tlp ufw noto-fonts-cjk noto-fonts-emoji ttf-jetbrains-mono-nerd inter-font ark p7zip unrar unzip zip;
sudo ufw default deny;
sudo ufw enable;
sudo systemctl enable tlp ufw;
sudo systemctl start tlp ufw;
git clone https://aur.archlinux.org/yay.git && cd yay && makepkg -si;
yay -S mkinitcpio-firmware update-grub vscodium-bin --noconfirm --removemake;
flatpak install flathub org.videolan.VLC;
flatpak install flathub md.obsidian.Obsidian;
flatpak install flathub org.qbittorrent.qBittorrent;
```
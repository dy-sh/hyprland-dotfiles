
This repository contains configuration scripts for the `Hyprland` (linux window manager).

Config can only be installed to a physical disk (not a virtual machine).
It is recommended to install on a freshly installed Arch Linux.

Installation can be done using a `set-hypr` script.

## Manual installation

For manual installation follow the steps below.

### To support NVidia video cards

Do the following steps before installing `Hyprland`.

```bash
yay -S linux-headers nvidia-dkms qt5-wayland qt5ct libva libva-nvidia-driver-git
```

Add modules: `nvidia nvidia_modeset nvidia_uvm nvidia_drm` to `/etc/mkinitcpio.conf`

Generate new image: 

```bash
sudo mkinitcpio --config /etc/mkinitcpio.conf --generate /boot/initramfs-custom.img
```

Add/create the following: `options nvidia-drm modeset=1` in `/etc/modprobe.d/nvidia.conf`

Then, reboot.

### Install Hyprland

```
yay -S hyprland kitty jq mako waybar-hyprland swww swaylock-effects wofi wlogout xdg-desktop-portal-hyprland swappy grim slurp thunar polkit-gnome python-requests pamixer pavucontrol brightnessctl bluez bluez-utils blueman network-manager-applet gvfs thunar-archive-plugin file-roller btop pacman-contrib starship ttf-jetbrains-mono-nerd noto-fonts-emoji lxappearance xfce4-settings sddm-git sddm-sugar-candy-git 
```

### Install config

Copy configs to home direcoty.

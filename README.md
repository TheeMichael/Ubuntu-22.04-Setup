# Ubuntu-22.04-Setup
Guide on setting up and configuring Ubuntu 22.04 and maybe some other versions the way I like it

## Initial Install
1. Create bootable flashrive (use rufus on windows, use startup disk creator on Ubuntu)
2. Install Ubuntu through a USB media installer
3. Select minimal install when asked, 3rd party drivers check if you have Nvidia 
4. Create an EFI partition with 512MB
5. All the rest mount to root as ext4

## First boot
1. If OS was not updated during install
```
sudo apt update && sudo apt upgrade
reboot
```
2. Do above `twice` then run
```
sudo apt dist-upgrade
reboot
```
3. Get the packages
```
sudo apt install \
gnome-shell-extensions \
chrome-gnome-shell \
gnome-browser-connector \
chromium-browser \
neofetch \
gparted \
htop
```

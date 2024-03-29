# Ubuntu-22.04-Setup
Guide on setting up and configuring Ubuntu 22.04 and maybe some other versions the way I like it

## Initial Install
1. Create bootable flashdrive (use rufus on windows, use startup disk creator on Ubuntu)
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
gnome-tweaks \
gnome-shell-extensions \
chrome-gnome-shell \
chromium-browser \
neofetch \
gparted \
htop \
git
```
4. Get Extensions Use the firefox browser extension if you can (May need to use chromium).
5. If you can't install them through the browser download them manually check 'gnome-shell --version' to download right versions
6. Here is a link to help with manual installation https://www.debugpoint.com/manual-installation-gnome-extension/
```
Audio Output Switcher
https://extensions.gnome.org/extension/751/audio-output-switcher/

Dash to Panel
https://extensions.gnome.org/extension/1160/dash-to-panel/

Removable Drive Menu
https://extensions.gnome.org/extension/7/removable-drive-menu/

Resource Monitor
https://extensions.gnome.org/extension/1634/resource-monitor/

V-Shell (Vertical Workspaces)
https://extensions.gnome.org/extension/5177/vertical-workspaces/
```
5. Clone this repository (if you havent already and navigate to its directory in terminal)
6. Load dconf settings
```
cat ubuntu.preferences | dconf load /
``` 
7. Copy dotfiles
```
mkdir ~/Scripts
cp ./dotfiles/bash_profile ~/.bash_profile
cp ./dotfiles/bashrc ~/.bashrc
cp ./dotfiles/inputrc ~/.inputrc
cp ./dotfiles/profile ~/.profile
```
9. Logout & Login
8. Enable autoscrolling in Firefox
9. Set light theme in Firefox

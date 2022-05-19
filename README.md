# arch

### STEP 1: Download arch iso

> [Official download page](https://archlinux.org/download/)

### STEP 2: Flashing the .iso file

* detect device to flash into
```
fdisk -l
```
* unmount before flash
```
umount /dev/sda
```
* write the live image
```
dd bs=4M if=/path/to/void-live-ARCH-DATE-VARIANT.iso of=/dev/sda && sync
```

### STEP 3: Install

```
arch-install
```

### STEP 4: install yay

```
pacman -S --needed base-devel git 
git clone https://aur.archlinux.org/yay.git
cd yay
makepkg -si
```

### STEP 5: install dwm automatic version
```
yay -S auto-dwm
```
this and others (recommneded ones by terminal)

### STEP 6: enable TAP TO CLICK
enter/open file xorg config file
```
sudo nano /etc/X11/xorg.conf.d/00-keyboard.conf
```
add and save this: (ctrl+S and ctrl+X)

```
Section "InputClass"
       Identifier "tap-by-default"
       MatchIsTouchpad "on"
       MatchDriver "libinput"
       Option "Tapping" "on"
EndSection
```
#### installing important apps

```
yay -S file-roller pcmanfm firefox  
```



+ to be continued...



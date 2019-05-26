# setup archlinux arm
+ formatting
+ flashing etc
+ pacman-key --init
+ pacman-key --populate arhclinuxarm
+ pacman -Syyuu
+ pacman -Syu
+ pacman -S git sudo fish autossh openssh netctl
# for the love of god get the kernel module in for rebooting
+ sudo modprobe bcm2835_wdt
+ then also make it permenant: https://wiki.archlinux.org/index.php/Kernel_module#Automatic_module_loading_with_systemd
# if can install neovim
+ install neovim
+ set as default editor
# create user with sudo
+ alarm ALL=(ALL) ALL
# install package manager
+ mkdir git
+ cd git
+ git clone https://aur.archlinux.org/pikaur.git
+ cd pikaur
+ makepkg -si
# setup networking
+ eduroam + private profiles
+ enable dhcpcd
+ enable netctl-auto
# setup reverse tunnel
  ## install root files:
  + create .ssh dir
  + known_hosts
  + authorized_keys
  + ssh keys
  ## install systemd unit file
  + authosshTunnel service
  ## sshd
  + AllowUsers alarm
  + publik key only
  + systemctl start + enable sshd
# setup fish shell
+ exec fish
# setup Nemesyst
+ pikaur -S nemesyst-git
+ git clone https://github.com/DreamingRaven/nemesyst
# encrypt disk
## wipe disk properly
## cryptsetup
## cryptab
# setup mongodb
+ run my pkgbuild
# install raspberry pi headers
+ https://aur.archlinux.org/packages/linux-aarch64-raspberrypi-headers/
# install driver for wireless
+ https://aur.archlinux.org/packages/rtl8812au-rpi-dkms-git/
# installing python-picamera
+ sudo pikaur -S python-picamera
+ edit PKGBUILD with "export READTHEDOCS=True"
# the list of things needed:
+ user to work with i.e adding to sudoers etc
+ netctl network profiles
+ public keys to allow ssh
+ private key to ssh
+ .ssh config
+ autosshTunnel unit file
+ sshd config file
+ .bashrc config file
+ device to encrypt
+ location desired for mongodb to mount
+ bonus commands

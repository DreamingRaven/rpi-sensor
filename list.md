# setup archlinux arm
+ formatting
+ flashing etc
+ pacman-key --init
+ pacman-key --populate arhclinuxarm
+ pacman -Syyuu
+ pacman -Syu
+ pacman -S git sudo fish autossh openssh netctl
# create user with sudo
+ alarm ALL=(ALL) ALL
# install package manager
+ mkdir git
+ cd git
+ git clone https://aur.archlinux.org/pikaur.git
+ cd pikaur
+ makepkg -si
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
+ pkgbuild + git clone
# encrypt disk
## wipe disk properly
## cryptsetup
## cryptab
# setup mongodb
+ run my pkgbuild

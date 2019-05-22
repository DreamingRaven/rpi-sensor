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

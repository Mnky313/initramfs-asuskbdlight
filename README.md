# initramfs-asuskbdlight

This is a initcpio hook that can be used to turn Asus laptops keyboard
backlight on during boot. This is usefull when prompted to type the LUKS
passphrase, for instance.

## Install

Build:

    makepkg .
    sudo pacman -U ./initramfs-asuskbdlight-*.pkg.tar.zst

Edit /etc/mkinitcpio.conf:

    HOOKS=(base udev autodetect modconf block keyboard asuskbdlight encrypt filesystems resume)

Regenerate initramfs:

    sudo mkinitcpio -p linux

Reboot.

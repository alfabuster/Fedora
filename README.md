# Fedora

## Grub update for Fedora
 ```sudo grub2-mkconfig -o /boot/efi/EFI/fedora/grub.cfg```
 ``` sudo grub2-mkconfig -o /etc/grub2-efi.cfg```

# WireGuard GUI

```nmcli connection import type wireguard file "/home/den/Wireguard/Fedora37.conf"```

```nmcli connection delete Fedora37```

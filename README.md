# Fedora

## Grub update for Fedora
```
sudo grub2-mkconfig -o /boot/efi/EFI/fedora/grub.cfg 
sudo grub2-mkconfig -o /etc/grub2-efi.cfg 
```

# WireGuard GUI

```
nmcli connection import type wireguard file "/home/den/Wireguard/Fedora37.conf"
nmcli connection delete Fedora37
```
# Grub Windows на второй диск

В Windows открыть ком.строку от имени администратора, ввести diskpart и следующие команды

```
list disk
sel disk X  - где Х это номер диска 120 ГБ 
list part
sel part N  - где N это номер раздела 100 МБ (раздел EFI)
assign letter=m
exit


bcdboot C:\windows /s M: /l ru-ru 
```

Должно будет появиться сообщение, что файлы загрузки созданы (перед ru-ru буква L). 

В PowerShell от администратора:
```
Stop-Process -Name VBoxTray -Force
```
Потом:
```
Start-Process "C:\Windows\System32\VBoxTray.exe"
```
Проверь:
```
Get-Process VBoxTray
```

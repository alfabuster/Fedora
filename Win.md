Сейчас пришли мне результат вот этих команд:
```
net view \\vboxsvr
net view \\vboxsrv
net view \\VBoxSF
```
и:
```
net use
```
и, если не лень, последний большой вывод:
```
Get-WinEvent -LogName System -MaxEvents 500 |
Where-Object { $_.Message -match 'VBox|vboxsf|VBoxMRXNP' } |
Select-Object TimeCreated, Id, ProviderName, LevelDisplayName, Message |
Format-List
```

"C:\Program Files\Oracle\VirtualBox Guest Additions\VBoxTray.exe"
```
Test-Path "C:\Program Files\Oracle\VirtualBox Guest Additions\VBoxTray.exe"
```

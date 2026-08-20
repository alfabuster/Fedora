Сейчас мне нужны результаты вот этих пяти команд:
```
Get-Service RpcSs,RpcEptMapper,LanmanWorkstation | Format-Table Name,Status,StartType
Get-Service Netlogon | Format-Table Name,Status,StartType
net view \\localhost
net view \\127.0.0.1
Test-NetConnection localhost -Port 135
```
После этого уже будет понятно, это Windows RPC/Network Provider или конкретно VBoxMRXNP.

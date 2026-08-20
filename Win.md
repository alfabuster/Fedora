А вот теперь я бы сделал официальный workaround VirtualBox

У Oracle прямо описана проблема с разрешением имени VBOXSVR/VBOXSRV в Windows-госте. Они рекомендуют добавить эти имена в lmhosts, после чего перезагрузить гостя.

Открой Блокнот от имени администратора и файл:
```
C:\Windows\System32\drivers\etc\lmhosts
```
Если файла lmhosts нет — создай его без расширения.

Добавь в конец:
```
255.255.255.255    VBOXSVR #PRE
255.255.255.255    VBOXSRV #PRE
```
Сохрани.

Потом перезагрузи Windows Server.

Это не костыль, который мы придумали — это прямо указанный Oracle workaround для проблем с доступом Windows-гостя к VirtualBox Shared Folders.


После перезагрузки

Сначала:
```
net view \\vboxsvr
```
Если увидит шару — отлично.

Тогда:
```
net use Z: \\vboxsvr\lab_share
```
И:
```
dir Z:\
```

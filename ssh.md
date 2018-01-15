# SSH

## Login Service

目前僅提供 SSH 安全連線方式，也請記得使用安全的密碼。

可連線的主機有：

-   Linux: linux1, linux2, …, linux15, oasis1, oasis2, oasis3
-   FreeBSD: bsd1

### Windows 使用教學

在 Windows 的 SSH client 可使用 [PuTTY](http://www.chiark.greenend.org.uk/~sgtatham/putty/) 等軟體，連線方式選擇 SSH 後輸入工作站的 domain name（例如: linux1.csie.ntu.edu.tw），即可連線至工作站。

### Mac/Linux 使用教學

Linux 與 Mac 都有現成的 terminal 可以使用，所以只要打開 Terminal，輸入 `ssh [csie_id]@[domain]`。例如：`ssh b01902000@linux1.csie.ntu.edu.tw`，即可順利登入。

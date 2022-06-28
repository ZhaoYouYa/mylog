
## 1.修改Host文件

最常使用的一个场景是，定位github的IP 。在[这里](https://www.ipaddress.com/)找到对应的IP。

```powershell
# 切换到su
cd /etc/

vim hosts
```


## 2. 设置默认的shell

```bash
chsh -s /bin/bash
```

如果 /bin/bash 不是一个可执行的shell。 使用 which bash 去找到对应的目录。

如果 使用了 ch -s /bin/pwsh, 然后把powershell 删除了，Linux 就无法登录了。
这时候，需要使用 recover 模式，对应腾讯云 使用 vnc 登录，它可以进入 recover 模式。


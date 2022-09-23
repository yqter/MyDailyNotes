# DOS_Command

和Linux都差不多

dir类似ls：显示自己的文件夹

cls（clear screen）类似于clear

cd 还是 cd

只不过换盘符的时候，需要换一下方式，直接用 `E:` 就能直接切换到相应的盘里面。

依然有Linux上面的补全键，TAB

复制文件 `copy a.txt b.txt`

更换名称 `move a.txt b.txt`

删除文件 `rmdir`



查看网卡信息 `ipconfig` 有以下一个选项

1. `ipconfig /all` 查看网卡的详细信息，可以看到MAC信息哦
2. `ipconfig /flushdns` 刷新DNS服务器。
3. `ipconfig /renew` 更新所有适配器



配置hosts文件的话，在系统的这里哦。

在域名解析过程中，操作系统会优先查询本地的记录信息，在windows操作系统中，操作系统会优先查询hosts文件的域名映射关系。

其路径存放在： `C:\Windows\System32\drivers\etc\hosts` 文件中。



环境变量 `set`



find，用于过滤需要的文字，一般会和管道连用。

```bash
 ipconfig | find "IPv4 地址 "
```

当然你也可以用findstr命令做相同的操作，输出的结果基本上是一致的（如：ipconfig | findstr "IPv4 地址 "）



`tree`：以当前目录为准，立即将下面所有的文件夹列出来。

1. tree /f 下面的所有文件也要展示出来

`deltree`：删除整个目录命令

1. 功能：将整个目录及其下属子目录和文件删除。
2. 格式：deltree [盘符：]〈路径名〉
3. 使用说明：该命令可以一步就将目录及其下的所有文件、子目录、更下层的子目录一并删除，而且不管文件的属性为隐藏、系统或只读，只要该文件位于删除的目录之下，deltree都一视同仁，照删不误。使用时务必小心！
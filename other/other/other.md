gitbash乱码

![image-20200406162013481](other.assets/image-20200406162013481.png)

![image-20200406162112930](other.assets/image-20200406162112930.png)

![img](other.assets/1588162427146.png)

vscode终端配置

```ini
"terminal.integrated.shell.windows":  "D:\\WorkApp\\Git\\bin\\bash.exe",
"terminal.integrated.shellArgs.windows": ["--login","-i"]
```

#### 无法直接运行python

在 git bash 中运行下`python --version` 或 `pip list` 等命令，都可以正常使用。
 但是输入 `python` 却会进入前台运行界面并且无任何响应，只能 Ctrl+c 退出。
 解决方式有 3 种：

1. 使用 winpty 接口
    `winpty python`

2. 显式使用 `python -i`

3. 使用 alias 映射
    在 `/etc/bash.bashrc` 中加入 `alias python='winpty python'`，之后便可以直接输入 `python` 了

   ```bash
     #临时执行或修改/etc/profile文件，在文件内容末尾加入
     export TIME_STYLE='+%Y-%m-%d %H:%M:%S'
   ```

```mermaid
graph LR

st[程序语句]-->java
st-->python
st-->p3(php)

s2(数据库)-->o1{oracle}
s2-->mysql
s2-->sqlite
s2-->mssql

o1-->t1{sql}
o1-->pl1
o1-->优化1
o1-->备份1
o1-->导入导出1

t1-->t2{sql}
t1-->pl2
t1-->优化2
t1-->备份2
t1-->导入导出2
t2-->t3{sql}
t2-->pl3
t2-->优化3
t2-->备份3
t2-->导入导出3
t3-->t4{sql}
t3-->pl4
t3-->优化4
t3-->备份4
t3-->导入导出4
t4-->t5{sql}
t4-->pl5
t4-->优化5
t4-->备份5
t4-->导入导出5

pl1-->t6{sql}
pl1-->pl6
pl1-->优化6
pl1-->备份6
pl1-->导入导出6
```

```powershell
#scoop
https://www.jianshu.com/p/50993df76b1c
https://blog.csdn.net/qqb67g8com/article/details/83445453
#执行策略，允许执行不信任的脚本
Set-ExecutionPolicy RemoteSigned -scope CurrentUser
iex (new-object net.webclient).downloadstring('https://raw.githubusercontent.com/lukesampson/scoop/master/bin/install.ps1')
```


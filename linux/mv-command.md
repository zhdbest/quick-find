# 简介
在 Linux 中使用`mv`命令可以进行多种任务，例如移动文件、改名。

### 移动文件
mv 即 move 的缩写，其最初就是被用来移动文件的。

首先，在根目录下创建 test 目录，再在该目录下创建两个目录：d1、d2，再在 d1 目录下创建一个文件 readme.md，下面我们把 readme.md 移动到 d2 中去
``` bash
# 命令句式： mv source dest
$ mv /test/d1/readme.md /test/d2
```

该命令可以使用的选项有如下：

 选项 | 作用 | 例子
-------|------|-----
-f     | 若目标目录下已存在同名文件，则直接覆盖 | `mv -f /test/d1/readme.md /test/d2`
-i     | 若目标目录下已存在同名文件，则询问是否覆盖 | `mv -i /test/d1/readme.md /test/d2`
-u     | 若目标目录下已存在同名文件，且源文件比较新时才进行覆盖 | `mv -u /test/d1/readme.md /test/d2`

### 文件重命名
可以使用如下命令进行文件的重命名：
``` bash
# 将当前目录下的 readme.md 文件改名为 readme1.md
$ mv readme.md readme1.md
```

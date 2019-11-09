# 简介
在 Linux 中可能存在一些命令比较长，此时我们可以通过创建命令别名来简化操作。

``` bash
# 查看当前所设置的别名
$ alias
alias cp='cp -i'
alias egrep='egrep --color=auto'
alias fgrep='fgrep --color=auto'
alias grep='grep --color=auto'
alias l.='ls -d .* --color=auto'
alias ll='ls -l --color=auto'
alias ls='ls --color=auto'

# 设置别名
$ alias cp='cp -i'

# 取消设置别名
$ unalias cp
```

像上面这样设置别名，只是临时的别名。比如，我们通过 ssh 连接到服务器上，设置了某个别名，然后退出，然后再次通过 ssh 进行连接，执行 `alias` 命令就会发现刚才设置的别名没有了。那我们该如何设置永久的别名呢？

永久的别名也分为以下两种:  
1. 只对某用户生效  
如果真想对某用户生效，可以修改/home/用户名/.bashrc，该文件中包含如下内容：  
    ``` bash
    # User specific aliases and functions

    alias rm='rm -i'
    alias cp='cp -i'
    alias mv='mv -i'
    ```
    只要在此处维护别名即可。

2. 对所有用户生效
    在 `/etc/bashrc` 文件中进行维护，但是就我本人的使用场景来说，这个设置几乎用不到。
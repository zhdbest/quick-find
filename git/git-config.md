### git config
git 配置分为以下几个等级：
* 仓库级别
* 用户级别
* 系统级别

其优先级从上至下逐渐降低。

#### 查看 git配置
1. 查看仓库级别配置
    ``` bash
    $ git config --local -l
    ```
2. 查看用户级别配置
    ``` bash
    $ git config --global -l
    ```
3. 查看系统级别配置
    ``` bash
    $ git config --system -l
    ```
4. 查看所有配置
    ``` bash
    # 也可以使用 git config -l
    $ git config --list
    ```

5. 查看具体某一项，可采用如下命令：
    ``` bash
    $ git config 具体配置项
    ```


#### 如何查看当前 Git用户信息
实例如下：
``` bash
# 查看用户的用户名
$ git config user.name

# 查看用户的邮箱
$ git config user.email
```
执行上面这两个命令所得到的用户名和密码，得到的结果和当前目录是否为 Git项目目录有关。
* 当前目录是 Git项目目录，得到的是仓库级别的配置。
* 当前目录不是 Git项目目录，得到的是 Git的用户级别的配置。

#### 修改 git配置
例如，修改 git用户的用户名：
``` bash
$ git config user.name yourname
# 如果当前目录不是一个git 仓库，会得到下面的报错
fatal: not in a git directory
```

如果想修改用户级别的配置，可以按如下设置：
``` bash
git config --global user.name yourname
```




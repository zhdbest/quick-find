有时，我们想要获取某目录下的目录结构，然后将其放入 Markdown 文本中，该如何操作呢？可以使用 mddir 工具来解决这个问题。

### 安装
mddir 是个 npm 包，你需要先确保你已经安装了 Node.js，然后执行如下命令安装 mddir：
```
$ npm install mddir -g
```

### 使用
安装完之后，进入你想要生成目录结构的目录下，执行命令 `mddir`，然后就会在当前目录下生成一个 directoryList.md 文件，其内容大致如下：
```
|-- undefined
    |-- README.md
    |-- SUMMARY.md
    |-- new
```

### 注意
该文件需要注意以下两点：
1. 顶层目录是 undefined，这个要改成你自己的目录
2. 该文件内的内容 copy 出来之后，要放入 Markdown 的代码块内

### 其他问题
1. 某些场景下执行无效  
使用的 mddir 版本是 1.1.1，操作步骤如下：  
    1. 创建一个新目录，命名为 newbook
    2. 进入 newbook，执行 `gitbook init`，生成了 README.md 和 SUMMARY.md 两个文件
    3. 执行 `mddir`，命令行无任何输出，并且也未生成 directoryList.md 文件  
    
    解决方案：在该目录下先创建一个文件夹，然后再执行命令就OK了
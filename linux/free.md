# 简介

在 Linux 中如果想查看系统内存的占用情况可以使用`free`命令。

```bash
$ free
		total		used		free		shared		buff/cache		available
Mem:  1014756	  490656	   71316		   448		    452784		   353180
Swap:	   0		   0		   0
```



直接使用`free`命令，得到的结果是以 kb 为单位来展示的，如果想以 MB 来展示，可以使用`free -h`命令。

输出结果包括了一行标题和两行数据，“Mem”是内存的使用情况， “Swap”是交换空间的使用情况。

各列的含义如下：

| 列         | 含义                                                         |
| ---------- | ------------------------------------------------------------ |
| total      | 可用物理内存和交换空间的大小                                 |
| used       | 已被使用的物理内存和交换空间                                 |
| free       | 未被使用的物理内存和交换空间                                 |
| shared     | 临时文件系统（tmpfs）使用的物理内存                          |
| buff/cache | buff 是内核缓冲区使用的内存，cache 是 内核页缓存和 Slab 用到的内存 ，该列是展示的 buff 和 cache 之和 |
| available  | 还可用于应用程序的内存（不包括 swap）                        |








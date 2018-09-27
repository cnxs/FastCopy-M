FastCopy-M
===========
"FastCopy-M" 是免费开源软件 "FastCopy" 的一个二次开发分支。<br />
"FastCopy-M" is a branch of open source soft "FastCopy", "M" means Multilanguage or Mapaler.

现在拥有如下语言：<br />
Now has the following language:

| Language | LCID Dec | Detail |
| --- | --- | --- |
| Japanese | 1041 | 日本語,Original |
| English | 1033 | Official translation by H.Shirouzu |
| Chinese, simplified | 2052 | 简体中文，从英文翻译而来 |
| Chinese, traditional | 1028 | 繁体中文，用MS Word從簡中轉換而來，稍加修訂 |

## Original FastCopy feature | 原版FastCopy特点

* FastCopy 是Windows上最快的复制/删除软件。<br />
FastCopy is the Fastest Copy/Delete Software on Windows.

* 它支持UNICODE和超过MAX_PATH(260字符)的文件路径名。<br />
It supports UNICODE and over MAX_PATH (260 characters) file pathnames.

* 它会根据来源与目录在相同或不同的硬盘自动选择不同的方法。<br />

| 不同硬盘 | 相同硬盘 |
| --- | --- |
| 读写分别由单独的线程并行处理。 | 首先做连续读取直到充满缓冲区。当缓冲区填满时，才开始大块数据写入。 |

It automatically selects different methods according to whether Source and DestDir are in the same or different HDD(or SSD).<br />

| Diff HDD | Same HDD |
| --- | --- |
| Reading and writing are processed respectively in parallel by separate threads. | Reading is processed until the big buffer fills. When the big buffer is filled, writing is started and processed in bulk. |
	

* 因为不使用操作系统缓存来处理读/写，所以其他应用程序就不容易变得缓慢。<br />
Reading/Writing are processed with no OS cache, as such other applications do not become slow.

* 它可以实现接近设备极限的读写性能。<br />
It can achieve Reading/Writing performance that is close to device limit.

* 可以使用 包含/排除 筛选器 (UNIX通配符样式)。<br />
Include/Exclude Filter (UNIX Wildcard style) can be specified. ver3.0 or later, Relative Path can be specified.

* 仅使用Win32 API和C运行时，没有使用MFC等框架，因此可以轻量、紧凑、轻快的运行。（注：XP下也不需要安装运行库）——所以也导致无法支持手机的MTP模式<br />
It runs fast and does not hog resources, because MFC is not used. (Designed using Win32 API and C Runtime only)

* 你可以修改此款软件，所有源代码都以GPLv3许可开源。<br />
You can modify this software, because all source code has been opened to the public under the GPL ver3 license.

## FastCopy-M feature | FastCopy-M特点

* 汉化并支持更加完整的多国语言显示，添加语言只需要修改资源文件。<br />

FastCopy Chinesization and modify to support other language more overall, add language only need add new resources

* 支持调用网络URL作为帮助文件，资源文件内“IDS_FASTCOPYHELP”修改为网页url即可。<br />
Support use http url to replace "chm" help files, change "IDS_FASTCOPYHELP" in resource to your URL.<br />
![URL help](http://ww4.sinaimg.cn/large/6c84b2d6gw1ewbd1y0bygj20rw0le4bq.jpg)

### Build | 编译
FastCopy-M采用[VS2017](https://www.visualstudio.com/zh-cn/downloads/download-visual-studio-vs.aspx) v141工具集。<br />
FastCopy-M used [VS2017](https://www.visualstudio.com/en-us/downloads/download-visual-studio-vs.aspx) with v141 tools.

## Website
### FastCopy-M website | FastCopy-M网站

http://mapaler.github.io/FastCopy-M/

### Official website | FastCopy官方网站

http://ipmsg.org/tools/fastcopy.html
 
## Official License | FastCopy官方许可
> FastCopy ver3.x Copyright(C) 2004-2018 by SHIROUZU Hiroaki
> 
> This program is free software. You can redistribute it and/or modify it under the GNU General Public License version 3(GPLv3).<br />
> [license-gpl3.txt](http://ipmsg.org/tools/license-gpl3.txt)

> xxHash Library Copyright (c) 2012-2016, Yann Collet All rights reserved.<br>
> [License details](https://ipmsg.org/tools/xxhash-LICENSE.txt).

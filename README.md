# QuarkPanTool

[![Python Version](https://img.shields.io/badge/python-3.11.6-blue.svg)](https://www.python.org/downloads/release/python-3116/)
[![Latest Release](https://img.shields.io/github/v/release/ihmily/QuarkPanTool)](https://github.com/ihmily/QuarkPanTool/releases/latest)
[![Downloads](https://img.shields.io/github/downloads/ihmily/QuarkPanTool/total)](https://github.com/ihmily/QuarkPanTool/releases/latest)

本项目在 [https://github.com/ihmily/QuarkPanTool](https://github.com/ihmily/QuarkPanTool) 的基础上，解决转存文件数量超过限制的情况。在录入分享链接之后，可以指定转存的层级。层级之上的父目录需要后续手动整理。

QuarkPanTool 是一个简单易用的小工具，旨在帮助用户快速批量转存夸克网盘分享文件。它提供了一种简便的方式，让您能够轻松地将夸克网盘中的共享文件保存到您的个人账户中。

## 功能特点

- 运行稳定：基于 playwright 支持网页登录夸克网盘，无需手动获取 Cookie。
- 轻松操作：简洁直观的命令行界面，方便快捷地完成文件转存。
- 批量转存：支持一次性转存多个夸克网盘分享链接中的文件。
- 本地下载：支持批量下载网盘文件夹中的所有文件。
- 文件分批转存：分享链接中文件数量过多的情况下无法一次转存，可以指定按某一层级的子文件夹自动存储。

## 如何使用

如果不想自己部署环境，可以下载打包好的可执行文件(exe)压缩包 [QuarkPanTool](https://github.com/ihmily/QuarkPanTool/releases) ，解压后直接运行即可。

1.下载代码

```
git clone https://github.com/sudot/QuarkPanTool.git
```

2.安装依赖

```
pip install -r requirements.txt
playwright install firefox
```

3.运行

```
python quark.py
```

运行后会使用 playwright 进行登录操作，当然也可以自己手动获取 cookie 填写到 config/cookies.txt 文件中。如果想切换登录账号，直接将 cookies.txt 文件清空，然后打开软件重新登录即可。

## 注意事项

- 首次运行会比较缓慢，请注意底部任务栏，程序会自动打开一个浏览器，让你登录夸克网盘，登录完成后，请不要手动关闭浏览器，回到软件界面按 Enter 键，浏览器会自动关闭并保存你的登录信息，下次运行就不需要登录了。
- 接着会提示让你输入保存位置的文件夹 ID，如果你不知道 ID 请直接按回车键，或者输入 0 代表将你的文件保存在网盘根目录。
- 执行批量转存之前，请先在 url.txt 文件中填写网盘分享地址（一行一个）

## 效果演示

![演示截图](./images/PixPin_2024-09-05_18-05-41)

## 许可证

QuarkPanTool 使用 [Apache-2.0 license](https://github.com/sudot/QuarkPanTool#Apache-2.0-1-ov-file) 许可证，详情请参阅 LICENSE 文件。

---

**免责声明**：本工具仅供学习和研究使用，请勿用于非法目的。由使用本工具引起的任何法律责任，与本工具作者无关。

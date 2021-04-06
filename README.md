# lanraragi

![GitHub Workflow Status](https://img.shields.io/github/workflow/status/ylqjgm/lanraragi/Docker%20CI%20Release?label=build&logo=github&style=for-the-badge&logoWidth=24)
 ![Docker Image Version (latest by date)](https://img.shields.io/docker/v/ylqjgm/lanraragi?label=version&logo=docker&sort=date&style=for-the-badge&logoWidth=24) ![Docker Image Size (latest by date)](https://img.shields.io/docker/image-size/ylqjgm/lanraragi?label=size&logo=docker&sort=date&style=for-the-badge&logoWidth=24) ![Docker Pulls](https://img.shields.io/docker/pulls/ylqjgm/lanraragi?logo=docker&style=for-the-badge&logoWidth=24)

## 简介

LANraragi 是一个开源的在线漫画阅读器，原版由 [Difegue/LANraragi](https://github.com/Difegue/LANraragi) 开发，本程序是来自于 [uparrows/LANraragi_cn](https://github.com/uparrows/LANraragi_cn) 的汉化版。

本项目来自于 [uparrows/LANraragi_cn](https://github.com/uparrows/LANraragi_cn)，原项目提供的 [Docker](https://hub.docker.com/r/dezhao/lanraragi_cn/) 仅包含 **linux/amd64** 平台，无法在 **N1** 上使用，故此自行编译 **linux/arm** 版本。

## 使用

要使用本项目，请先安装 [Docker](https://www.docker.com)，然后执行：

```shell
docker pull ylqjgm/lanraragi:latest
docker run --name lanraragi -p 3000:3000 -v /data/lanraragi/content:/root/lanraragi/content -v /data/lanraragi/database:/root/lanraragi/database --restart always -d ylqjgm/lanraragi:latest
```

程序运行在 **3000** 端口，包含两个外挂存储：**/root/lanraragi/database**、**/root/lanraragi/content**

## 功能

> 1. 以存档格式存储您的漫画。 （支持 zip / rar / targz / lzma / 7z / xz / cbz / cbr / pdf，epub 准支持）
> 2. 直接从 Web 浏览器读取档案：服务器使用临时文件夹从压缩文件中读取。
> 3. 使用内置的 OPDS 目录在专用的阅读器软件中阅读档案
> 4. 使用客户端 API 与其他程序中的 LANraragi 进行交互
> 5. 两种不同的用户界面：紧凑的存档列表，带有悬停缩略图或缩略图视图。
> 6. 从 5 种预装的响应库样式中进行选择，或使用 CSS 添加您自己的样式。
> 7. 命名空间的完整标签支持：添加您自己的名称或使用插件从其他来源导入它们。
> 8. 设置收藏夹标签，以便能够快速在您的收藏夹中找到包含它们的档案
> 9. 自动标记：将存档添加到 LANraragi 后，将使用插件自动导入元数据。
> 10. 将数据库备份为 JSON，以将标签传递到另一个 LANraragi 实例。

## 鸣谢

Docker: [https://www.docker.com](https://www.docker.com)  
difegue: [https://github.com/Difegue/LANraragi](https://github.com/Difegue/LANraragi)  
uparrows: [https://github.com/uparrows/LANraragi_cn](https://github.com/uparrows/LANraragi_cn)

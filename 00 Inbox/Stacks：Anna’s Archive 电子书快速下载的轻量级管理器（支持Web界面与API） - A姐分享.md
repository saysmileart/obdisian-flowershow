---
title: "Stacks：Anna’s Archive 电子书快速下载的轻量级管理器（支持Web界面与API） - A姐分享"
source: "https://www.ahhhhfs.com/77800/"
author:
  - "[[ahhhhfs]]"
published: 2025-11-26
created: 2025-12-08
description: "Stacks 是一款为 Anna’s Archive 打造的轻量级下载管理器，支持快速下载、Web控制台、队列管理、自动镜像切换与 API 调用，可通过 Docker 一键部署，帮助用户稳定、高效地批量获取电子书资源。"
tags:
  - "clippings"
---
## Stacks：Anna’s Archive 电子书快速下载的轻量级管理器（支持Web界面与API）

2025-11-26 [GitHub项目](https://www.ahhhhfs.com/funny_site/github%e9%a1%b9%e7%9b%ae/) [趣站](https://www.ahhhhfs.com/funny_site/) 0 0 [0](https://www.ahhhhfs.com/77800/#comments)

- [详情介绍](https://www.ahhhhfs.com/77800/#pills-details)
- [常见问题](https://www.ahhhhfs.com/77800/#pills-faq)
- [评论建议](https://www.ahhhhfs.com/77800/#pills-comments)

## Stacks 是什么

Stacks 是一款专为 **Anna’s Archive** 打造的下载队列管理器，通过简洁的 Web 控制台完成电子书的排队、管理与自动下载。它支持 Anna’s Archive 的高速下载 API，并在不可用时自动切换镜像站，保持下载过程稳定顺畅。

系统以容器化方式运行，几乎不需要维护，适合自托管用户、重度电子书读者与数字资料收集者。

[![Stacks：Anna’s Archive 电子书快速下载的轻量级管理器（支持Web界面与API）](https://www.ahhhhfs.com/wp-content/uploads/2025/11/Stacks%EF%BC%9AAnnas-Archive-%E7%94%B5%E5%AD%90%E4%B9%A6%E5%BF%AB%E9%80%9F%E4%B8%8B%E8%BD%BD%E7%9A%84%E8%BD%BB%E9%87%8F%E7%BA%A7%E7%AE%A1%E7%90%86%E5%99%A8%EF%BC%88%E6%94%AF%E6%8C%81Web%E7%95%8C%E9%9D%A2%E4%B8%8EAPI%EF%BC%89.jpg "Stacks：Anna’s Archive 电子书快速下载的轻量级管理器（支持Web界面与API） 1")](https://www.ahhhhfs.com/wp-content/uploads/2025/11/Stacks%EF%BC%9AAnnas-Archive-%E7%94%B5%E5%AD%90%E4%B9%A6%E5%BF%AB%E9%80%9F%E4%B8%8B%E8%BD%BD%E7%9A%84%E8%BD%BB%E9%87%8F%E7%BA%A7%E7%AE%A1%E7%90%86%E5%99%A8%EF%BC%88%E6%94%AF%E6%8C%81Web%E7%95%8C%E9%9D%A2%E4%B8%8EAPI%EF%BC%89.jpg)

---

## 核心亮点

### 🖥 Web 操作面板

提供密码保护的管理界面，可查看任务、进度、历史与系统状态，并支持会话管理与自动登录保护。

### 📚 下载队列管理

浏览器中一键加入下载任务，自动排序、自动重试，中断后可继续，减少人工干预。

### ⚡ 快速下载支持

适配 Anna’s Archive 会员的高速下载 API，让电子书以更快的速度获取。

### 🔄 自动镜像切换

当高速下载不可用时自动切换到镜像，下载不中断。

### 📊 实时监控

使用 Dracula 主题界面呈现队列、进度与历史记录，下载状态清晰可见。

### 🔌 浏览器集成

提供 Tampermonkey 脚本，在 Anna’s Archive 页面上直接生成下载按钮，省去手动复制链接。

### 🐳 Docker 随时部署

通过 Docker Compose 或 Docker CLI 一键启动，无需复杂配置。

---

## 通过 Docker 快速部署

### 使用 docker-compose（推荐）

创建 `docker-compose.yaml` ：  
（文本已在原文给出，内容无需重复演示）

修改路径、端口后执行：

```
docker compose up -d
```

安装完成后可通过 [http://localhost:7788](http://localhost:7788/) 访问 Web 控制台。

---

## 使用 Docker CLI

手动创建所需目录并运行：

```bash
docker run -d \
  --name stacks \
  -p 7788:7788 \
  -v /path/to/config:/opt/stacks/config \
  -v /path/to/download:/opt/stacks/download \
  -v /path/to/logs:/opt/stacks/logs \
  -e USERNAME=admin \
  -e PASSWORD=stacks \
  -e TZ=UTC \
  --restart unless-stopped \
  zelest/stacks:latest
```

用户名与密码仅首次生效；后续可通过配置文件修改。

---

## 初次使用指南

- 浏览器访问 Web UI 并登录
- 更改默认密码
- 复制 API 密钥，用于 Tampermonkey
- 配置高速下载 Key（如有）
- 设置下载延迟、重试次数等
- 保存设置即可开始使用

---

## 安全机制

Stacks 在自托管环境加入了多层安全保护：

- Bcrypt 密码加密
- HTTPOnly Cookie + SameSite
- 登录失败锁定机制
- 32 位安全 API Key
- 自动生成会话密钥
- 不建议暴露到公网，如需远程访问建议搭配 VPN 或反向代理 + HTTPS

---

## Stacks开源链接地址

GitHub地址： **[https://github.com/zelestcarlyone/stacks](https://github.com/zelestcarlyone/stacks "Stacks")**

适用于希望高效下载电子书、批量管理任务和提升资料获取效率的用户。

本文链接： [https://www.ahhhhfs.com/77800/](https://www.ahhhhfs.com/77800/ "Stacks：Anna’s Archive 电子书快速下载的轻量级管理器（支持Web界面与API）")

### 相关

[HallowLib-免费Z-Library电子书搜索下载站 无限制下载 用爱发电](https://www.ahhhhfs.com/32816/ "HallowLib-免费Z-Library电子书搜索下载站 无限制下载 用爱发电")

[Gopeed：开源、跨平台的高速下载工具（HTTP/BT/磁力全支持）](https://www.ahhhhfs.com/45198/ "Gopeed：开源、跨平台的高速下载工具（HTTP/BT/磁力全支持）")

[番茄小说下载器精简版：跨平台小说下载工具，支持EPUB格式与断点续传](https://www.ahhhhfs.com/72406/ "番茄小说下载器精简版：跨平台小说下载工具，支持EPUB格式与断点续传")

1. 转载请保留原文链接谢谢！
- 本站所有资源文章出自互联网收集整理，本站不参与制作，如果侵犯了您的合法权益，请联系本站我们会及时删除。
- 本站发布资源来源于互联网，可能存在水印或者引流等信息，请用户擦亮眼睛自行鉴别，做一个有主见和判断力的用户。
- 本站资源仅供研究、学习交流之用，若使用商业用途，请购买正版授权，否则产生的一切后果将由下载用户自行承担。
- 联系方式（#替换成@）：feedback#abskoop.com[上一篇

批发式爆单陪跑营，20节课带你实现批发式爆单，带你经松月入过W

](https://www.ahhhhfs.com/77795/ "批发式爆单陪跑营，20节课带你实现批发式爆单，带你经松月入过W")[下一篇

AI-CodeNexus：开发者专属的编程资讯与工具聚合平台

](https://www.ahhhhfs.com/77804/ "AI-CodeNexus：开发者专属的编程资讯与工具聚合平台")
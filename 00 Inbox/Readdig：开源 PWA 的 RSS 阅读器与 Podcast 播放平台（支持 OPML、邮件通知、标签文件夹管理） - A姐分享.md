---
title: "Readdig：开源 PWA 的 RSS 阅读器与 Podcast 播放平台（支持 OPML、邮件通知、标签/文件夹管理） - A姐分享"
source: "https://www.ahhhhfs.com/77675/"
author:
  - "[[ahhhhfs]]"
published: 2025-11-21
created: 2025-12-08
description: "Readdig 是一款开源的 PWA RSS 与 Podcast 阅读器，可订阅新闻站、博客、微博、YouTube、X 与 Newsletter，支持文件夹与标签管理、收藏与阅读记录、OPML 导入/导出、邮件通知与 Paddle 支付集成，基于 Node.js + React + PostgreSQL + Redis，支持 Docker 快速部署。"
tags:
  - "clippings"
---
## Readdig：开源 PWA 的 RSS 阅读器与 Podcast 播放平台（支持 OPML、邮件通知、标签/文件夹管理）

2025-11-21 [AI工具](https://www.ahhhhfs.com/funny_site/ai-tool/) [GitHub项目](https://www.ahhhhfs.com/funny_site/github%e9%a1%b9%e7%9b%ae/) 0 0 [0](https://www.ahhhhfs.com/77675/#comments)

- [详情介绍](https://www.ahhhhfs.com/77675/#pills-details)
- [常见问题](https://www.ahhhhfs.com/77675/#pills-faq)
- [评论建议](https://www.ahhhhfs.com/77675/#pills-comments)

## Readdig简介

**Readdig** 是一款面向个人与团队的 **RSS 与 Podcast 阅读器** ，以 **PWA** 形态运行，覆盖桌面与移动端。通过 RSS 订阅即可把新闻网站、博客、微博、YouTube、X 以及各类 Newsletter 收纳在同一处，保持专注与高效阅读。项目开源，适合自建与二次开发。

- 官网： [https://readdig.com](https://readdig.com/ "Readdig 官网地址")
- 开源仓库： [https://github.com/readdig/readdig](https://github.com/readdig/readdig "Readdig 开源地址")

[![Readdig：开源 PWA 的 RSS 阅读器与 Podcast 播放平台（支持 OPML、邮件通知、标签/文件夹管理）](https://www.ahhhhfs.com/wp-content/uploads/2025/11/Readdig%EF%BC%9A%E5%BC%80%E6%BA%90-PWA-%E7%9A%84-RSS-%E9%98%85%E8%AF%BB%E5%99%A8%E4%B8%8E-Podcast-%E6%92%AD%E6%94%BE%E5%B9%B3%E5%8F%B0%EF%BC%88%E6%94%AF%E6%8C%81-OPML%E3%80%81%E9%82%AE%E4%BB%B6%E9%80%9A%E7%9F%A5%E3%80%81%E6%A0%87%E7%AD%BE-%E6%96%87%E4%BB%B6%E5%A4%B9%E7%AE%A1%E7%90%86%EF%BC%89.jpg "Readdig：开源 PWA 的 RSS 阅读器与 Podcast 播放平台（支持 OPML、邮件通知、标签/文件夹管理） 1")](https://www.ahhhhfs.com/wp-content/uploads/2025/11/Readdig%EF%BC%9A%E5%BC%80%E6%BA%90-PWA-%E7%9A%84-RSS-%E9%98%85%E8%AF%BB%E5%99%A8%E4%B8%8E-Podcast-%E6%92%AD%E6%94%BE%E5%B9%B3%E5%8F%B0%EF%BC%88%E6%94%AF%E6%8C%81-OPML%E3%80%81%E9%82%AE%E4%BB%B6%E9%80%9A%E7%9F%A5%E3%80%81%E6%A0%87%E7%AD%BE-%E6%96%87%E4%BB%B6%E5%A4%B9%E7%AE%A1%E7%90%86%EF%BC%89.jpg)

## 核心功能

- **RSS 订阅阅读** ：统一管理各来源内容。
- **Podcast 播放** ：边听边看，随时同步进度。
- **账号与权限** ：支持用户注册登录与基础管理。
- **文件夹与标签** ：按主题整理订阅源，结构清晰。
- **收藏与阅读历史** ：重要内容一键标记，追踪已读进度。
- **OPML 导入/导出** ：一键迁移现有订阅清单。
- **邮件通知** ：新内容邮件提醒，不错过更新。
- **Paddle 支付集成** ：便于后续扩展增值功能或订阅方案。

## 适用场景

- **内容创作者与运营者** ：集中跟进行业新闻、平台更新与竞品动态。
- **学习与研究** ：统一整理学术博客、技术周刊与媒体报道。
- **播客重度用户** ：跨设备同步播放进度，体系化管理节目单。
- **信息极简主义** ：减少多 APP 来回切换，建立自己的信息中心。

## 技术架构

- **API** ：Node.js（Express.js）
- **前端** ：React（Create React App）
- **数据库** ：PostgreSQL
- **缓存** ：Redis
- **任务队列** ：Bull（基于 Redis）
- **部署** ：Docker / Docker Compose
- **PWA** ：安装到桌面，获得类原生体验

## 部署与本地开发

**步骤 1｜克隆仓库**

```bash
git clone https://github.com/readdig/readdig.git
cd readdig
```

**步骤 2｜配置并运行 API（Node.js ≥ 18.20.8）**

```bash
cd api
yarn install
cp .env.example .env     # 按需修改环境变量
yarn db:migrate          # 执行数据库迁移（PostgreSQL ≥ 12）
yarn dev                 # 本地服务: http://localhost:8000
```

**步骤 3｜启动前端应用**

```bash
cd ../app
yarn install
cp .env.example .env     # 按需修改环境变量
yarn start               # 本地访问: http://localhost:3000
```

**运行依赖**

- PostgreSQL 12+
- Redis 6+
- Docker & Docker Compose（可选，用于容器化部署）

### Nginx 反向代理提示

- 将 `yourdomain.com` 替换为实际域名。
- 非 www 域名跳转到 www。
- `proxy_pass http://api:8000/` 指向 API 容器（使用 Docker 网络名）。
- `/api/` 与 `http://api:8000/` 末尾斜杠需保留，以在转发时移除 `/api` 前缀。
- 若采用外部反向代理进行生产部署，可按实际环境调整。

## Readdig开源与链接

官方网站： [https://readdig.com/](https://readdig.com/ "Readdig 官网地址")

GitHub 开源地址： [https://github.com/readdig/readdig](https://github.com/readdig/readdig "Readdig 开源地址")

本文链接： [https://www.ahhhhfs.com/77675/](https://www.ahhhhfs.com/77675/ "Readdig：开源 PWA 的 RSS 阅读器与 Podcast 播放平台（支持 OPML、邮件通知、标签/文件夹管理）")

### 相关

[Free News Agent｜开源新闻聚合与 RSS 订阅生成器](https://www.ahhhhfs.com/77212/ "Free News Agent｜开源新闻聚合与 RSS 订阅生成器")

[WeRSS：高效管理微信公众号内容的开源RSS订阅工具](https://www.ahhhhfs.com/72214/ "WeRSS：高效管理微信公众号内容的开源RSS订阅工具")

[Fluent Reader 开源跨平台RSS阅读器](https://www.ahhhhfs.com/21837/ "Fluent Reader 开源跨平台RSS阅读器")

1. 转载请保留原文链接谢谢！
- 本站所有资源文章出自互联网收集整理，本站不参与制作，如果侵犯了您的合法权益，请联系本站我们会及时删除。
- 本站发布资源来源于互联网，可能存在水印或者引流等信息，请用户擦亮眼睛自行鉴别，做一个有主见和判断力的用户。
- 本站资源仅供研究、学习交流之用，若使用商业用途，请购买正版授权，否则产生的一切后果将由下载用户自行承担。
- 联系方式（#替换成@）：feedback#abskoop.com[上一篇

TLDW 开源 AI 工具：把 1 小时 YouTube 长视频压缩成 5 分钟的结构化学习笔记

](https://www.ahhhhfs.com/77661/ "TLDW 开源 AI 工具：把 1 小时 YouTube 长视频压缩成 5 分钟的结构化学习笔记")[下一篇

LibrePods：让 AirPods 完整适配 Android 的开源工具｜解锁降噪、自适应通透、入耳检测与多设备连接

](https://www.ahhhhfs.com/77679/ "LibrePods：让 AirPods 完整适配 Android 的开源工具｜解锁降噪、自适应通透、入耳检测与多设备连接")
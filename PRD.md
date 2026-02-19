# PRD: Chrome 书签管理扩展

## 1. 产品概述
开发一个 Chrome 扩展，帮助用户管理书签，支持死链检测、分类管理、WebDAV 同步，并通过集成大语言模型为书签生成描述和标签，提升书签的可读性和组织性。

## 2. 目标用户
- 普通用户：需要高效管理大量书签
- 开发者：需要快速访问技术文档和资源
- 研究人员：需要分类和标记大量参考链接
- 跨设备用户：需要在不同设备间同步书签

## 3. 核心功能

### 3.1 书签管理
- 增删改查：添加、删除、编辑、查看书签
- 集成 Chrome 原生书签栏

### 3.2 死链检测
- 自动检测无法访问的链接
- 红色标记死链，提供删除选项

### 3.3 书签分类管理
- 添加分类标签（工作、学习、娱乐等）
- 按分类过滤书签

### 3.4 大语言模型集成
- 配置页输入 API 密钥
- 自动为书签生成描述和标签

### 3.5 WebDAV 同步
- 配置 WebDAV 服务器（URL、用户名、密码）
- 手动/自动同步书签到 WebDAV
- JSON 格式存储（bookmarks.json）

### 3.6 新标签页
- 替换 Chrome 新标签页
- 展示书签列表（标题、链接、描述、标签、分类）

## 4. 技术实现

### 4.1 文件结构
```
bookmark-manager-extension/
├── manifest.json
├── background.js
├── newtab/
│   ├── newtab.html
│   ├── newtab.js
│   └── newtab.css
├── config/
│   ├── config.html
│   ├── config.js
│   └── config.css
├── assets/
│   ├── icon16.png
│   ├── icon48.png
│   └── icon128.png
└── README.md
```

### 4.2 技术栈
- 前端：HTML、CSS、JavaScript
- Chrome API：chrome.bookmarks、chrome.storage
- WebDAV 客户端：dav 库
- 大语言模型 API：OpenAI GPT 或兼容 API

## 5. 与现有项目协同
- 可与 **StarSage** 协同：GitHub 星标 + 书签统一管理
- 可与 **网络安全聚合** 协同：安全情报书签管理
- 可与 **AI Nutritionist** 协同：健康资源书签管理

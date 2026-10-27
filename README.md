# Local WebTools 本地工具箱

一个注重隐私的纯前端本地工具箱。无需注册、打开即用，所有文件与文本处理均在浏览器本地完成，数据不会上传到任何服务器。

部署地址：`https://<用户名>.github.io/tool/`

## 功能清单

| 分类 | 工具 | 说明 |
|------|------|------|
| 编解码 | Base64 编解码 | UTF-8 安全，编码/解码/交换 |
| 编解码 | URL 编解码 | 支持 encodeURIComponent / encodeURI 两种模式 |
| 编解码 | HTML 实体编解码 | 转义与还原 |
| 编解码 | Hex 编解码 | 文本与十六进制互转 |
| 哈希 | 哈希计算器 | MD5 / SHA-1 / SHA-256 / SHA-512，本地计算 |
| 开发工具 | UUID 生成器 | UUID v4，加密安全随机数，支持批量与大写 |
| 开发工具 | 随机密码生成 | 可配置长度、字符集、排除易混淆字符 |
| 开发工具 | 时间戳转换 | Unix 秒/毫秒与日期时间互转 |
| 开发工具 | JSON 格式化 | 格式化、压缩、校验 |
| 开发工具 | 文本统计 | 字符数、单词数、行数、段落数 |
| 开发工具 | 大小写转换 | 大写/小写/标题/驼峰/kebab/snake |

## 技术说明

- 纯静态站点：HTML + CSS + 原生 JavaScript，无任何构建依赖
- 哈希计算使用 Web Crypto API（SHA 系列）与标准 MD5 实现
- 随机数全部来自 `crypto.getRandomValues`，安全可靠
- 所有计算在浏览器本地完成，无远程接口、无埋点、无追踪

## 部署方法

本仓库已配置 GitHub Pages（Settings → Pages → Deploy from branch → main / root）。

本地预览：

```bash
python3 -m http.server 8080
# 打开 http://localhost:8080
```

## 目录结构

```
.
├── index.html      # 页面入口
├── css/style.css   # 样式
├── js/app.js       # 全部工具逻辑
└── README.md
```

## 隐私声明

本项目不收集任何数据。所有输入输出都只存在于您的浏览器内存中，关闭页面即消失。

# GitHub 开源日刊 / 周刊

一个基于 GitHub 数据源的开源项目发现站。

## 目标

- 周二至周五：GitHub 开源日刊
- 周一：GitHub 开源周刊
- 数据来源限定为 GitHub：仓库主页、README、Issues、Pull Requests、Commits、Releases、Topics、License 等
- 输出可浏览、可搜索、可交互的静态网站

## 网站结构

```text
github-periodical/
├── index.html                 # 首页
├── daily/                     # 日刊
│   └── YYYY-MM-DD/
├── weekly/                    # 周刊
│   └── YYYY-Www/
├── templates/                 # 页面模板
├── data/                      # 内容数据
├── assets/                    # 静态资源
└── .github/workflows/         # 自动任务
```

## 内容原则

### 日刊

关注当天发现：

- 新项目
- 重大版本变化
- 高价值工具
- 可立即上手的开源项目

### 周刊

独立策划专题，不简单汇总日刊：

- 趋势判断
- 项目版图
- 对比矩阵
- 采用路径
- 风险分析

## 自动更新

GitHub Actions 每日运行，用于：

1. 检查 GitHub 项目变化
2. 更新项目数据
3. 生成日刊素材
4. 维护期刊索引

## 数据说明

所有 Star、Fork、语言、License 等数字均为生成时 GitHub 快照。

## 本地预览

直接打开 `index.html` 即可预览。

## License

MIT
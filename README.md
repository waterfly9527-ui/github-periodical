# GitHub 开源日刊 / 周刊

一个仅使用 GitHub 数据源的开源项目发现站。

## 发布节奏

- 周二至周五：GitHub 开源日刊
- 周一：GitHub 开源周刊
- 数据来源限定为 GitHub：Trending、Search、仓库主页、README、Issues、Pull Requests、Commits、Releases、Topics 和 License

## 首页规则

`index.html` 不是导航落地页，而是期刊阅读页：

- 直接完整展示最近一次发布的日刊或周刊
- 日刊首页包含项目搜索、分类筛选、排序、详情展开、数据快照、深浅色切换和 GitHub 跳转
- 周刊首页包含专题正文、项目版图、对比信息、采用路径和风险提示
- 历史内容通过 `archive/` 进入，不占用首页主体
- `data/periodicals.json` 的 `latest` 字段记录当前首页对应期刊

## 网站结构

```text
github-periodical/
├── index.html                 # 最新一期完整正文
├── daily/YYYY-MM-DD/          # 历史日刊独立页面
├── weekly/YYYY-Www/           # 历史周刊独立页面
├── archive/                   # 历史归档
├── data/projects.json         # 最新一期项目快照
├── data/periodicals.json      # 期刊索引与 latest 指针
├── templates/                 # 页面模板
└── assets/                    # 静态资源
```

## 内容原则

### 日刊

关注当天发现、近期活跃信号、立即上手价值和采用提醒，避免在没有重大变化时重复近期项目。

### 周刊

每期独立策划专题，不简单汇总日刊；形成趋势判断、项目版图、对比矩阵、采用路径和风险分析，并区分 GitHub 仓库事实与编辑分析。

## 自动发布

日刊与周刊任务必须直接更新本仓库 `main` 分支，而不是只生成附件：

1. 写入新的独立期刊页面
2. 更新结构化项目数据和期刊索引
3. 更新历史归档
4. 将首页重建为最近一期完整正文
5. 回读关键文件并核对提交 SHA

## 数据说明

所有 Star、Fork、语言、License 和活跃度数字均为生成时 GitHub 快照，后续可能变化。

## 本地预览

直接打开 `index.html` 即可浏览最新一期；历史内容从 `archive/index.html` 进入。

## License

MIT

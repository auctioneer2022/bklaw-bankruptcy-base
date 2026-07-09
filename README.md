# 破产法律知识库

全面、系统的破产法律实务知识库，涵盖法律法规、司法解释、行政法规、典型案例、实务指南等14个模块，为破产法律实务工作者提供便捷的查询和学习平台。

## 访问地址

- GitHub Pages: https://auctioneer2022.github.io/bankruptcy-knowledge-base/

## 知识库架构

本知识库按效力层级和实务场景划分为14个模块：

| 模块 | 目录 | 功能定位 | 文件数 |
|------|------|----------|--------|
| 一、法律 | `01-fa-lv` | 核心破产法律及其他法律中的破产相关条款 | 5 |
| 二、行政法规 | `02-xing-zheng-fa-gui` | 国务院行政法规及规范性文件 | — |
| 三、司法解释 | `03-si-fa-jie-shi` | 最高人民法院"法释"字号司法解释 | 27 |
| 四、最高院司法文件 | `04-zui-gao-fa-yuan-si-fa-wen-jian` | 会议纪要、意见、通知等司法文件 | 13 |
| 五、部门规章 | `05-bu-men-gui-zhang` | 各部委部门规章及规范性文件 | 13 |
| 六、地方法规 | `06-di-fang-fa-gui` | 地方性法规及个人破产试点 | — |
| 七、法院指导意见 | `07-di-fang-fa-yuan-zhi-dao-yi-jian` | 各地法院审判指导意见和规程 | 14 |
| 八、管理人规范 | `08-po-chan-guan-li-ren-xie-hui` | 破产管理人协会行业规范 | — |
| 九、典型案例 | `09-dian-xing-an-li` | 指导案例及各级法院典型案例 | 24 |
| 十、实务指南 | `10-shi-wu-zhi-nan` | 破产程序各环节操作指引 | — |
| 十一、文书模板 | `11-wen-shu-mo-ban` | 常用法律文书模板 | — |
| 十二、刑民交叉 | `12-xing-min-jiao-cha` | 破产程序中的刑民交叉规定 | — |
| 十三、专题研究 | `13-zhuan-ti-yan-jiu` | 破产法领域专题研究成果 | — |
| 十四、参考资料 | `14-can-kao-zi-liao` | 学术著作、数据库、国际比较法资料 | — |

### 模块间关系

```
法律 ──→ 行政法规 ──→ 司法解释 ──→ 最高院司法文件
  │                        │                │
  │                        ↓                ↓
  │                   部门规章          法院指导意见
  │                        │                │
  │                        ↓                ↓
  │                   地方法规          管理人规范
  │
  ├──→ 典型案例（裁判实践）
  ├──→ 实务指南（操作指引）
  ├──→ 文书模板（格式参考）
  ├──→ 刑民交叉（跨领域规定）
  ├──→ 专题研究（深度分析）
  └──→ 参考资料（扩展阅读）
```

## 项目结构

```
bankruptcy-knowledge-base/
├── docs/                                    # 文档源文件
│   ├── index.md                             # 首页
│   ├── 01-fa-lv/                            # 一、法律
│   ├── 02-xing-zheng-fa-gui/                # 二、行政法规
│   ├── 03-si-fa-jie-shi/                    # 三、司法解释
│   ├── 04-zui-gao-fa-yuan-si-fa-wen-jian/   # 四、最高院司法文件
│   ├── 05-bu-men-gui-zhang/                 # 五、部门规章
│   ├── 06-di-fang-fa-gui/                   # 六、地方法规
│   ├── 07-di-fang-fa-yuan-zhi-dao-yi-jian/  # 七、法院指导意见
│   ├── 08-po-chan-guan-li-ren-xie-hui/      # 八、管理人规范
│   ├── 09-dian-xing-an-li/                  # 九、典型案例
│   ├── 10-shi-wu-zhi-nan/                   # 十、实务指南
│   ├── 11-wen-shu-mo-ban/                   # 十一、文书模板
│   ├── 12-xing-min-jiao-cha/                # 十二、刑民交叉
│   ├── 13-zhuan-ti-yan-jiu/                 # 十三、专题研究
│   └── 14-can-kao-zi-liao/                  # 十四、参考资料
├── mkdocs.yml                               # MkDocs 配置
├── requirements.txt                         # Python 依赖
└── README.md                                # 项目说明
```

## 本地开发

### 环境要求

- Python 3.8+
- pip

### 安装依赖

```bash
pip install -r requirements.txt
```

### 本地预览

```bash
mkdocs serve
```

访问 http://127.0.0.1:8000 预览站点。

### 构建站点

```bash
mkdocs build
```

构建后的文件位于 `site/` 目录。

## 文档规范

### YAML Front Matter 模板

每个文档须包含以下元数据：

```yaml
---
title: "文件标题"
category: "模块分类"
tags: ["标签1", "标签2"]
date: "YYYY-MM-DD"
author: "发布机关"
status: "现行有效"
source: "官方来源URL"
---
```

### 文件命名规范

- 目录命名：`序号-拼音缩写`（如 `01-fa-lv`）
- 文件命名：`拼音全拼-编号.md`（如 `qi-ye-po-chan-fa.md`）
- 索引文件：`index.md`

### status 字段取值

| 值 | 说明 |
|----|------|
| `现行有效` | 文件当前有效 |
| `已废止` | 文件已被新文件替代或明文废止 |
| `部分失效` | 文件部分条款失效 |

## 协作规范

1. 使用 Markdown 格式编写内容
2. 文件命名使用小写拼音和连字符
3. 每个文档包含完整的 Front Matter 元数据
4. 通过 Pull Request 提交内容更新
5. 新增文件须在对应模块的 `index.md` 中添加链接
6. 新增文件须在 `mkdocs.yml` 的 `nav` 中添加导航条目

## 许可证

本项目采用 MIT 许可证。

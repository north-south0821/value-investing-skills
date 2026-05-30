# 🏰 Value Investing Skills

> **"投资不是一种智商游戏——智商 160 的人可能打败不了智商 130 的人。你需要的是控制冲动情绪的能力，这种冲动会让其他人在投资中陷入困境。"**
> — Warren Buffett

## 项目定位

这是一个基于**大师智慧**的价值投资知识库。我们将巴菲特、芒格、段永平等投资大师的思想拆解为可执行的**技能模块**——每个模块包含核心概念、检查清单和实战案例。

**目标用户**：希望用价值投资框架进行长期投资的个人投资者。

**核心理念**：所有分析围绕"企业长期价值"展开，拒绝短期投机。普通投资者无需追求复杂公式，重点掌握核心逻辑和可落地方法。

## 快速导航

### 🎯 大师技能模块

| 大师 | 核心侧重 | 状态 | 入口 |
|------|---------|------|------|
| **巴菲特** | 价值投资 · 护城河 · 安全边际 · 长期持有 | ✅ 完成 | [`skills/buffett/`](skills/buffett/index.md) |
| **芒格** | 多元思维 · 逆向思考 · 理性决策 · 检查清单 | 🚧 计划中 | `skills/munger/` |
| **段永平** | 本分哲学 · Right Business/People/Price · 不懂不投 | 🚧 计划中 | `skills/duan-yongping/` |

### 🛠️ 通用工具

| 模块 | 内容 | 入口 |
|------|------|------|
| **投资检查清单** | 投资前/后通用检查清单 | [`skills/checklist/`](skills/checklist/) |
| **思维模型库** | 芒格式多元思维模型索引 | `skills/checklist/mental-models/` |
| **分析模板** | 股票分析、投资日志、年度复盘模板 | `skills/checklist/templates/` |
| **术语词典** | 价值投资关键术语定义 | [`docs/glossary.md`](docs/glossary.md) |

### 📊 辅助工具

| 工具 | 用途 | 入口 |
|------|------|------|
| **数据获取脚本** | A 股/美股财务数据获取 | `tools/data-fetch/` |
| **估值分析脚本** | DCF、安全边际计算 | `tools/analysis/` |
| **配置文件** | API 密钥、参数配置 | `tools/config/` |

### 📚 资源索引

| 资源 | 内容 | 入口 |
|------|------|------|
| **经典书单** | 价值投资必读书目与阅读笔记 | `docs/books/` |
| **投资哲学** | 大师思想索引 | `docs/philosophy/` |
| **视频与播客** | 推荐视频、音频资源 | `resources/videos.md` |
| **社区与课程** | 优质社区与在线课程 | `resources/communities.md` |

### 📖 实战案例

| 案例 | 大师 | 入口 |
|------|------|------|
| 可口可乐 (1988) | 巴菲特 | `skills/buffett/case-studies/coke-1988.md` |
| 华盛顿邮报 (1973) | 巴菲特 | `skills/buffett/case-studies/washington-post.md` |
| 通用电气 (2008) | 巴菲特 | `skills/buffett/case-studies/ge-2008.md` |
| 喜诗糖果 (1972) | 巴菲特 | `skills/buffett/case-studies/sees-candies-1972.md` |

## 仓库结构

```
value-investing-skills/
├── README.md                   # 你在这里
├── CONTRIBUTING.md             # 贡献指南与内容规范
├── docs/                       # 文档目录
│   ├── philosophy/             # 投资哲学索引
│   ├── books/                  # 书单与阅读笔记
│   └── glossary.md             # 术语词典
├── skills/                     # 核心技能模块
│   ├── buffett/                # 巴菲特 skill ✅
│   │   ├── index.md
│   │   ├── 01-value-investing.md
│   │   ├── ... (共 8 个概念文件)
│   │   ├── checklists/         # 投资检查清单
│   │   └── case-studies/       # 实战案例
│   ├── munger/                 # 芒格 skill 🚧
│   ├── duan-yongping/          # 段永平 skill 🚧
│   ├── checklist/              # 通用检查清单
│   └── templates/              # 分析模板
├── tools/                      # 辅助工具与脚本
│   ├── data-fetch/
│   ├── analysis/
│   └── config/
├── examples/                   # 实战案例
├── resources/                  # 外部资源索引
└── .github/                    # GitHub 配置
```

## 推荐学习路径

### 初学者路径

```
1. 阅读 docs/glossary.md → 掌握核心术语
2. 阅读 skills/buffett/01-value-investing.md → 理解"买股票就是买公司"
3. 阅读 skills/buffett/02-moat-theory.md → 学会识别好公司
4. 阅读 skills/buffett/03-margin-of-safety.md → 学会等待好价格
5. 阅读 skills/buffett/case-studies/sees-candies-1972.md → 通过案例加深理解
6. 使用 skills/buffett/checklists/pre-investment.md → 第一次实战
```

### 有经验者路径

```
1. 直接跳到 skills/buffett/08-buffetts-3M.md → 完整的投资框架
2. 阅读案例研究获取灵感
3. 使用检查清单建立自己的投资纪律
4. 贡献案例或改进内容
```

## 内容质量标准

所有内容遵循以下标准：
- **可落地**：每个概念包含"如何实践"的具体步骤
- **有出处**：引用原文（巴菲特致股东信、芒格演讲等），标注来源年份
- **跨链接**：使用 `[[wikilinks]]` 在概念之间建立网状连接（Obsidian 兼容）
- **中英双语**：中文为主，关键术语和引用保留英文原文
- **拒绝空泛**：从各维度拆解到可执行的方法

详见 [`CONTRIBUTING.md`](CONTRIBUTING.md)

## 维护计划

- **年度更新**：每年 3/6/9/12 月更新大师最新言论和案例
- **版本归档**：重要更新打 tag（如 `v1.0-buffett-core-complete`）
- **功能扩展**：AI 辅助股票诊断、估值工具脚本、提醒系统（计划中）

## 灵感来源

- [awesome-investing](https://github.com/mr-karan/awesome-investing) — 开源投资资源整合
- 巴菲特致股东信（1957–2023）
- 查理·芒格《穷查理宝典》
- 段永平雪球博客归档

---

> **"投资很简单，但不容易。"** — Warren Buffett
>
> 这个仓库的目标是帮你掌握"简单"的部分，然后你就可以把精力集中在"不容易"的部分：**纪律和耐心**。

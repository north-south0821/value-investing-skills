# 🏰 Value Investing Skills

> **"投资不是一种智商游戏——智商 160 的人可能打败不了智商 130 的人。你需要的是控制冲动情绪的能力，这种冲动会让其他人在投资中陷入困境。"**
> — Warren Buffett

## 项目定位

这是一个基于**大师智慧**的价值投资知识库。我们将巴菲特、芒格、段永平等投资大师的思想拆解为可执行的**技能模块**——每个模块是独立的 Claude Code skill，包含核心概念、检查清单和实战案例。

**目标用户**：希望用价值投资框架进行长期投资的个人投资者。

**核心理念**：所有分析围绕"企业长期价值"展开，拒绝短期投机。普通投资者无需追求复杂公式，重点掌握核心逻辑和可落地方法。

## 快速导航

### 🎯 大师技能模块

| 大师 | 核心侧重 | 状态 | 入口 |
|------|---------|------|------|
| **巴菲特** | 价值投资 · 护城河 · 安全边际 · 长期持有 | ✅ 完成 | [`value-investing-buffett/SKILL.md`](value-investing-buffett/SKILL.md) |
| **芒格** | 多元思维 · 逆向思考 · 理性决策 · 检查清单 | 🚧 模板就绪 | [`value-investing-munger/SKILL.md`](value-investing-munger/SKILL.md) |
| **段永平** | 本分哲学 · Right Business/People/Price · 不懂不投 | 🚧 模板就绪 | [`value-investing-duan-yongping/SKILL.md`](value-investing-duan-yongping/SKILL.md) |

### 📖 共享资源

| 资源 | 内容 | 入口 |
|------|------|------|
| **术语词典** | 价值投资关键术语定义 | [`value-investing-buffett/glossary.md`](value-investing-buffett/glossary.md) |

### 📊 实战案例

| 案例 | 大师 | 入口 |
|------|------|------|
| 可口可乐 (1988) | 巴菲特 | `value-investing-buffett/case-studies/coke-1988.md` |
| 华盛顿邮报 (1973) | 巴菲特 | `value-investing-buffett/case-studies/washington-post.md` |
| 通用电气 (2008) | 巴菲特 | `value-investing-buffett/case-studies/ge-2008.md` |
| 喜诗糖果 (1972) | 巴菲特 | `value-investing-buffett/case-studies/sees-candies-1972.md` |

## 仓库结构

```
value-investing-skills/
├── README.md                          # 你在这里
├── CONTRIBUTING.md                    # 贡献指南与内容规范
├── value-investing-buffett/           # 巴菲特 skill ✅
│   ├── SKILL.md                       # 技能入口（YAML frontmatter）
│   ├── 01-value-investing.md          # 价值投资哲学
│   ├── 02-moat-theory.md              # 护城河理论
│   ├── 03-margin-of-safety.md         # 安全边际
│   ├── 04-circle-of-competence.md     # 能力圈
│   ├── 05-long-term-holding.md        # 长期持有
│   ├── 06-avoid-market-timing.md      # 不预测市场
│   ├── 07-financial-statements.md     # 财报阅读
│   ├── 08-buffett-3M.md               # 3M 投资法
│   ├── pre-investment-checklist.md    # 投资前检查清单
│   ├── annual-review-checklist.md     # 年度复盘清单
│   ├── glossary.md                    # 术语词典
│   └── case-studies/                  # 实战案例
│       ├── coke-1988.md
│       ├── sees-candies-1972.md
│       ├── washington-post.md
│       └── ge-2008.md
├── value-investing-munger/            # 芒格 skill 🚧
│   └── SKILL.md                       # 模板就绪
└── value-investing-duan-yongping/     # 段永平 skill 🚧
    └── SKILL.md                       # 模板就绪
```

## Claude Code 集成

每个大师模块是一个独立的 Claude Code skill，通过符号链接激活：

```
~/.claude/skills/
├── value-investing-buffett → <本项目>/value-investing-buffett
├── value-investing-munger  → <本项目>/value-investing-munger   (将来)
└── value-investing-duan-yongping → <本项目>/value-investing-duan-yongping (将来)
```

Claude Code 会根据任务上下文自动发现并加载对应的 skill。每个 skill 的 `SKILL.md` 包含 YAML frontmatter（name + description），描述触发条件。

## 推荐学习路径

### 初学者路径

```
1. 阅读 value-investing-buffett/glossary.md → 掌握核心术语
2. 阅读 value-investing-buffett/01-value-investing.md → 理解"买股票就是买公司"
3. 阅读 value-investing-buffett/02-moat-theory.md → 学会识别好公司
4. 阅读 value-investing-buffett/03-margin-of-safety.md → 学会等待好价格
5. 阅读 value-investing-buffett/case-studies/sees-candies-1972.md → 通过案例加深理解
6. 使用 value-investing-buffett/pre-investment-checklist.md → 第一次实战
```

### 有经验者路径

```
1. 直接跳到 value-investing-buffett/08-buffett-3M.md → 完整的投资框架
2. 阅读案例研究获取灵感
3. 使用检查清单建立自己的投资纪律
4. 贡献案例或改进内容
```

## 内容质量标准

所有内容遵循以下标准：
- **可落地**：每个概念包含"如何实践"的具体步骤
- **有出处**：引用原文（巴菲特致股东信、芒格演讲等），标注来源年份
- **双语**：中文为主，关键术语和原文引用保留英文（Claude Code skill 采用双语以优化检索）
- **拒绝空泛**：从各维度拆解到可执行的方法
- **Skill 格式**：每个大师模块包含符合 [agentskills.io 规范](https://agentskills.io/specification) 的 `SKILL.md`

详见 [`CONTRIBUTING.md`](CONTRIBUTING.md)

## 维护计划

- **年度更新**：每年 3/6/9/12 月更新大师最新言论和案例
- **版本归档**：重要更新打 tag（如 `v1.0-buffett-core-complete`）
- **功能扩展**：芒格和段永平模块（模板已就绪，待填充内容）

## 灵感来源

- [awesome-investing](https://github.com/mr-karan/awesome-investing) — 开源投资资源整合
- 巴菲特致股东信（1957–2023）
- 查理·芒格《穷查理宝典》
- 段永平雪球博客归档

---

> **"投资很简单，但不容易。"** — Warren Buffett
>
> 这个仓库的目标是帮你掌握"简单"的部分，然后你就可以把精力集中在"不容易"的部分：**纪律和耐心**。

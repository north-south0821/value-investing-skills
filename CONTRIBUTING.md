# 贡献指南

> 感谢你对 Value Investing Skills 项目的兴趣！本指南帮助你了解如何贡献内容。

## Skill 格式规范

本项目中的每个大师模块都是一个符合 [agentskills.io 规范](https://agentskills.io/specification) 的 **Claude Code skill**。每个 skill 目录包含一个 `SKILL.md` 作为入口文件，以及若干支持文件。

### 目录结构

```
value-investing-<master>/
├── SKILL.md                    # 必需：YAML frontmatter（name + description）
├── 0X-<concept-name>.md        # 概念文件（数字前缀排序）
├── <checklist-name>.md         # 检查清单（平铺在根目录）
├── glossary.md                 # 术语词典（可选）
└── case-studies/               # 实战案例（唯一允许的子目录）
    └── <company>-<year>.md
```

### SKILL.md 规范

每个 `SKILL.md` 必须包含 YAML frontmatter：

```yaml
---
name: value-investing-<master-slug>    # 必须与目录名一致，仅字母/数字/连字符
description: Use when [触发条件]. [覆盖范围].  # 最多 1024 字符，第三人称，以 "Use when" 开头
---
```

**description 编写原则**：只描述**触发条件**和覆盖范围，不要总结 skill 的工作流程。Claude 会根据 description 决定是否加载此 skill。

### 文件命名

- 使用 **kebab-case**（小写 + 连字符）：`01-value-investing.md` ✓，`01_Value_Investing.md` ✗
- 数字前缀用于排序：`01-`, `02-`, `03-`
- 案例文件：`公司名-年份.md`（如 `coke-1988.md`）
- Skill 目录名：`value-investing-<master-slug>`（如 `value-investing-buffett`）

### Markdown 风格

#### 标题层级
```markdown
# H1 — 文件标题（每个文件只有一个 H1）
## H2 — 主要章节
### H3 — 子章节
```

#### 引用
```markdown
> **"原文引用。"**
> — 作者，来源年份
```

#### 内部链接
使用标准 Markdown 相对路径链接（不使用 Obsidian `[[]]` 语法）：
```markdown
[价值投资哲学](01-value-investing.md)
[护城河理论](../value-investing-buffett/02-moat-theory.md)
[投资前检查清单](pre-investment-checklist.md)
```

#### 表格
```markdown
| 列 1 | 列 2 | 列 3 |
|------|------|------|
| 数据 | 数据 | 数据 |
```

### 内容结构模板

每个概念文件应包含以下部分（按顺序）：

1. **引用**（Quote）— 核心思想的一句话原文引用
2. **核心思想**（Core Idea）— 2-3 段解释
3. **详细讨论**（Why It Matters / Detailed Breakdown）
4. **如何实践**（How to Apply）— 可操作步骤
5. **常见误区**（Common Misconceptions）— 3-5 个错误认知
6. **关键来源**（Key Sources）— 出处年份和文档名
7. **相关概念**（Related Concepts）— 标准 Markdown 链接

每个案例文件应包含：

1. **背景**（Background）— 公司、时代、竞争环境
2. **投资逻辑**（Investment Thesis）— 看到了什么别人没看到的
3. **关键数据**（Key Numbers）— 价格、估值、回报
4. **投资结果**（Outcome）— 发生了什么
5. **关键启示**（Key Lessons）— 3-5 个要点

### 语言规范

- **双语**：中文为主，英文术语和原文引用保留英文
- 关键术语标注英文：**安全边际（Margin of Safety）**
- 巴菲特/芒格原文引用使用双语：中文翻译 + 英文原文

### 引用规范

必须标注来源的**年份和文档名**：

```markdown
> "以合理价格买入优质企业……"（*It's far better to buy a wonderful company at a fair price...*）
> — Warren Buffett, 1989 年致股东信
```

主要来源缩写对照：
- `19XX/20XX 年致股东信` = Berkshire Hathaway Shareholder Letter
- `股东大会` = Berkshire Hathaway Annual Meeting
- `《穷查理宝典》` = Poor Charlie's Almanack
- `《聪明的投资者》` = The Intelligent Investor

## 如何贡献

### 添加新的大师 Skill

1. 在项目根目录创建 `value-investing-<master-slug>/` 目录
2. 创建 `SKILL.md`，包含正确的 YAML frontmatter（name 与目录名一致）
3. 创建概念文件（`0X-concept-name.md`）
4. 创建检查清单（平铺在根目录）
5. 更新本 README 的导航表
6. 创建符号链接到 `~/.claude/skills/`：
   ```bash
   ln -s "<项目路径>/value-investing-<master-slug>" ~/.claude/skills/value-investing-<master-slug>
   ```

### 添加新概念文件

1. 在对应大师目录下创建文件，命名遵循 `XX-concept-name.md` 格式
2. 遵循上述内容结构模板
3. 在 `SKILL.md` 中添加指向新文件的引用

### 添加新案例

1. 在 `value-investing-<master>/case-studies/` 下创建文件
2. 命名格式：`公司名-年份.md`
3. 遵循案例模板结构
4. 在相关概念文件中添加案例引用

### 添加新检查清单

1. 在对应大师目录根下创建（平铺，不使用子目录）
2. 使用勾选框格式：`- [ ] 检查项`
3. 每个清单项目应是一句话能说清的、可明确判断的

### 修改现有内容

1. 先开 Issue 讨论（如果是实质性的改动）
2. 保持与周围文件的风格一致
3. 更新所有引用该概念的相关文件链接

## 内容质量标准

所有 Pull Request 将按以下标准审查：

- [ ] 有原文引用且标注了来源
- [ ] 包含"如何实践"的可操作步骤
- [ ] 使用标准 Markdown 链接（非 `[[]]` 语法）
- [ ] 没有给出**具体的买卖建议**（"买入茅台"）——只给出分析框架
- [ ] 至少 300 字以上的实质性内容
- [ ] 双语可读性良好
- [ ] SKILL.md（如是新 skill）的 YAML frontmatter 符合规范

## 禁止事项

- ⛔ 不提供具体的股票买卖建议（"现在买入 XXX"）
- ⛔ 不推荐具体券商或投资产品
- ⛔ 不使用短期回报数据（< 3 年）来论证投资策略
- ⛔ 不鼓励使用杠杆
- ⛔ 不进行政治性讨论

## 行为准则

- 基于事实和数据讨论，而非情绪
- 尊重不同的投资风格和观点
- 承认自己的错误和不足
- 引用要给出来源——不给来源的"巴菲特说"默认是编的

---

> **"我们不寻求成为最聪明的人，我们寻求避免做愚蠢的事。"**
> — Charlie Munger

---

Co-Authored-By: Claude Code <noreply@anthropic.com>

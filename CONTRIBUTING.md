# 贡献指南

> 感谢你对 Value Investing Skills 项目的兴趣！本指南帮助你了解如何贡献内容。

## 内容规范

### 文件命名

- 使用 **kebab-case**（小写 + 连字符）：`01-value-investing.md` ✓，`01_Value_Investing.md` ✗
- 数字前缀用于排序：`01-`, `02-`, `03-`
- 案例文件：`公司名-年份.md`（如 `coke-1988.md`）

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
使用 Obsidian 兼容的 Wiki 链接语法：
```markdown
[[01-value-investing|价值投资哲学]]
[[../munger/02-multidisciplinary-models|芒格：多元思维模型]]
[[checklists/pre-investment|投资前检查清单]]
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
3. **为什么重要**（Why It Matters）— 心理学/经济学/实践意义
4. **如何实践**（How to Apply）— 可操作步骤
5. **常见误区**（Common Pitfalls）— 3-5 个错误
6. **关键来源**（Sources）— 出处年份和文档名
7. **相关概念**（Related Concepts）— Wiki 链接

每个案例文件应包含：

1. **背景**（Background）— 公司、时代、竞争环境
2. **投资逻辑**（Thesis）— 看到了什么别人没看到的
3. **关键数据**（Key Numbers）— 价格、估值、回报
4. **投资结果**（Outcome）— 发生了什么
5. **关键启示**（Lessons）— 3-5 个要点

### 语言规范

- **中文为主**，英文术语和原文引用保留英文
- 第一次出现的专业术语标注英文：**安全边际（Margin of Safety）**
- 巴菲特/芒格原文引用使用**双语**：中文翻译 + 英文原文

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

### 添加新的概念文件

1. 在对应大师目录下创建新文件（`skills/buffett/`, `skills/munger/`, `skills/duan-yongping/`）
2. 命名遵循 `XX-concept-name.md` 格式（XX 为数字排序）
3. 遵循上述内容结构模板
4. 在对应大师的 `index.md` 中添加导航链接

### 添加新的案例

1. 在 `skills/<master>/case-studies/` 下创建文件
2. 命名格式：`公司名-年份.md`
3. 遵循案例模板结构
4. 在相关概念文件中添加案例引用

### 添加新的检查清单

1. 在对应大师的 `checklists/` 或通用 `skills/checklist/` 下创建
2. 使用勾选框格式：`- [ ] 检查项`
3. 每个清单项目应是一句话能说完的、可明确判断的

### 修改现有内容

1. 先开 Issue 讨论（如果是实质性的改动）
2. 保持与周围文件的风格一致
3. 更新所有引用该概念的相关文件链接

## 内容质量标准

所有 Pull Request 将按以下标准审查：

- [ ] 有原文引用且标注了来源
- [ ] 包含"如何实践"的可操作步骤
- [ ] 链至少 2-3 个相关概念
- [ ] 没有给出**具体的买卖建议**（"买入茅台"）——只给出分析框架
- [ ] 至少 300 字以上的实质性内容
- [ ] 中文可读性良好

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

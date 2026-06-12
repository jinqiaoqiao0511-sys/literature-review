# 自动化任务：文献调研-文献深度阅读（任务06）

> 调用 paper-quick-reader 技能对核心文献进行深度阅读

---

## 第一步：计算ISO周编号

根据当前日期计算ISO周编号：YYYY-WXX

---

## 第二步：读取高优先级文献

从 `D:\.A硕士\.A干\每周文献调研(1)\每周文献调研\文献调研\YYYY-WXX\step03-classified-YYYY-WXX.md` 提取 ⭐⭐⭐⭐⭐ 文献列表：

```json
{
  "papers": [
    {
      "id": "001",
      "title": "论文标题",
      "doi": "10.xxx/xxx",
      "arxiv_id": "2301.12345",
      "priority": "⭐⭐⭐⭐⭐"
    }
  ]
}
```

**处理上限**：
- ⭐⭐⭐⭐⭐：精读，最多 5 篇
- ⭐⭐⭐⭐：引导阅读，最多 3 篇

---

## 第三步：调用 paper-quick-reader 技能

使用 Skill 工具调用 `paper-quick-reader`：

### 3.1 单篇精读模式

对每篇 ⭐⭐⭐⭐⭐ 文献：

```json
{
  "mode": "single",
  "papers": [
    {
      "source": {
        "kind": "arxiv_id",
        "content": "2301.12345"
      },
      "label": "paper-001"
    }
  ],
  "context": {
    "my_direction": "合成生物学、RNA语言模型、启动子工程、发酵优化、破囊壶菌、解脂耶氏酵母、酵母"
  },
  "preferences": {
    "depth_hint": "auto",
    "include_peer_review": false
  }
}
```

### 3.2 批量对比模式

对 ⭐⭐⭐⭐ 文献（≤10篇）：

```json
{
  "mode": "compare",
  "papers": [...],
  "compare_dimensions": ["method", "dataset", "results", "innovation"],
  "context": {
    "my_direction": "合成生物学、RNA语言模型、启动子工程"
  }
}
```

---

## 第四步：处理速读结果

解析 paper-quick-reader 输出，提取：

```json
{
  "summary_card": {
    "research_question": "...",
    "method": "...",
    "key_results": "...",
    "contributions": "...",
    "limitations": "..."
  },
  "connection_points": [...],
  "one_line_plain": "..."
}
```

---

## 第五步：生成深度阅读报告

路径：`D:\.A硕士\.A干\每周文献调研(1)\每周文献调研\文献调研\YYYY-WXX\deep-reading-YYYY-WXX.md`

```markdown
# 文献深度阅读报告 - YYYY-WXX

**生成时间**：YYYY-MM-DD HH:mm

---

## 精读文献

### 1. [论文标题]

- **DOI**：10.xxx/xxx
- **核心问题**：...
- **方法框架**：...
- **关键结果**：...
- **核心贡献**：...
- **局限性**：...
- **一句话总结**：...

### 2. ...

---

## 引导阅读文献

### [对比分析]

| 论文 | 方法 | 数据集 | 结果 |
|------|------|--------|------|
| 论文A | ... | ... | ... |
| 论文B | ... | ... | ... |

---

## 输出文件

- 深度阅读报告：`文献调研/YYYY-WXX/deep-reading-YYYY-WXX.md`
- Obsidian笔记：`文献调研/YYYY-WXX/001-xxx.md`
```

---

## 执行完成确认

```
✅ 文献深度阅读完成（auto-06）
- ISO周编号：YYYY-WXX
- 精读文献：N 篇
- 引导文献：N 篇
- 输出一：文献调研/YYYY-WXX/deep-reading-YYYY-WXX.md
- 输出二：文献调研/YYYY-WXX/（Obsidian笔记）
- 后续任务：auto-07（知识库整理）
```

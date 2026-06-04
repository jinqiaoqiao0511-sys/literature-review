# 自动化任务：文献调研-检索LLM+专项

请严格执行以下调研任务。

> **输出文件**：`D:\WorkBuddy\每周文献调研\中间结果\step02b-merged-YYYY-WXX.md`

---

## 第一步：计算时间窗口

请根据当前日期计算本周的检索时间窗口：
1. 确定"上周"的日期范围：
   - 上周一 = 今天往前推到今天所在的周一，再往前推7天
   - 上周日 = 上周一 + 6天
2. 确定ISO周编号：YYYY-WXX
3. 记录时间窗口，后续所有检索使用此窗口

**跨周补跑检测**：
- 检查上周的输出文件（`step02b-merged-YYYY-WXX.md`）是否已存在
- 若不存在 → 说明上周可能未执行，在输出文件头部标注"⚠️ 疑似跨周未执行"
- 本次执行仅覆盖本周时间窗口，不自动补检缺失周次

---

## 第二步：执行检索F — LLM生物设计（3组关键词）

你是一个专业的科研文献检索助手。请使用以下工具执行检索：

**可用工具**：WebSearch、ArXiv论文追踪、Tavily AI Search、多引擎搜索、Wechat Article Search

**工具调用示例**（请按此语法调用）：
- ArXiv论文追踪：调用 `arxiv-watcher` skill，输入搜索关键词如 `"synthetic biology" AND "large language model"`
- WebSearch：使用 WebSearch 工具，查询如 `"synthetic biology" "large language model" "design" site:nature.com OR site:science.org`
- Tavily AI Search：调用 `tavily` skill，输入查询如 `"synthetic biology" AND ("large language model" OR "foundation model") design generation`
- Exa网络搜索：调用 `web-search-exa` skill，输入语义查询如 `"LLM driven biological design generation"`

**关键词列表**：

34. `"synthetic biology" AND ("large language model" OR "LLM" OR "foundation model") AND ("design" OR "generation" OR "prediction") NOT ("NLP" OR "linguistic" OR "sentiment analysis")`
35. `("biology" OR "biomedicine") AND ("large language model" OR "LLM") AND ("design" OR "generation") NOT ("NLP" OR "linguistic" OR "sentiment analysis")`
36. `"protein language model" AND ("design" OR "generation")`

**执行顺序**：
1. ArXiv论文追踪：覆盖#34-36
2. WebSearch：覆盖#34-36，侧重期刊官网
3. Tavily AI Search：覆盖#34-36，侧重摘要聚合
4. Exa网络搜索：语义扩展

**Exa语义查询建议**：
- "foundation model biological design"
- "LLM driven protein generation"

---

## 第三步：执行检索G — 专项补强（5组关键词）

**关键词列表**：

37. `("ancestral sequence reconstruction" OR "ancestral protein") AND ("machine learning" OR "deep learning")`
38. `("polyketide synthase" OR ("PKS" AND "biosynthesis")) AND ("machine learning" OR "prediction" OR "deep learning")`
39. `"CRISPR" AND ("machine learning" OR "AI") AND ("design" OR "optimization")`
40. `"biosensor" AND ("machine learning" OR "deep learning")`
41. `("peptide design" OR "peptide generation") AND ("deep learning" OR "machine learning" OR "AI")`

**执行顺序**：
1. ArXiv论文追踪：覆盖#37-41
2. WebSearch：覆盖#39-41（CRISPR/生物传感器/肽设计），侧重期刊官网
3. Tavily AI Search：覆盖#37-41，侧重摘要聚合
4. Exa网络搜索：覆盖#37-38（ASR/PKS专项方向），语义扩展

**Exa语义查询建议**：
- "ancestral protein reconstruction machine learning"
- "polyketide synthase prediction deep learning"
- "PKS biosynthesis computational analysis"

---

## 每篇论文必须收集以下信息

- 标题（完整）
- 作者（格式：`姓, 名首字母.` 多作者用`; `分隔，>5人写前3+et al.）
- 期刊（标准全称或公认缩写）
- 发表日期（YYYY-MM-DD）
- DOI（以`10.`开头）
- 发表状态（`已发表`或`预印本`）
- 摘要（**完整存储，不做截取**）
- 论文关键词（从论文原文收集，用`; `分隔；若无法获取则标`N/A`）
- 核心发现（**从摘要中提炼**，2-3句话概括，以"该研究…"开头，避免直接复制摘要）
- 检索来源（如`ArXiv; Exa`）
- 关键词编号（如`#34,#38`）

---

## 异常处理

- 某工具失败 → 重试2次，仍失败则跳过，标记状态
- 某关键词零命中 → 正常记录
- 若Exa工具不可用 → 跳过Exa步骤，在其他工具结果中标记"Exa不可用"

---

## 第四步：去重合并（组内）

将F+G两组检索结果合并，按DOI去重：
- DOI相同 → 保留信息更完整的条目
- 合并「检索来源」和「关键词编号」列（取并集）
- 无DOI时 → 基于「标题+第一作者+年份」判断（相似度≥90%视为重复）

**数量控制**：
- 单方向最多保留8篇
- 总数量不设上限（留给整合阶段统一控制）

---

## 第五步：写入输出文件

将合并去重后的结果写入文件：

**文件路径**：`D:\WorkBuddy\每周文献调研\中间结果\step02b-merged-YYYY-WXX.md`
（YYYY-WXX替换为实际ISO周编号）

**文件格式**：

```markdown
## 检索结果：LLM+专项

**ISO周编号**：YYYY-WXX
**时间窗口**：YYYY-MM-DD 至 YYYY-MM-DD
**工具执行状态**：ArXiv ✅/❌ | WebSearch ✅/❌ | Tavily ✅/❌ | Exa ✅/❌
**关键词覆盖**：#34-#41，共8组
**原始命中**：[X] 条
**去重后**：[Y] 条

| # | 标题 | 作者 | 期刊 | 发表日期 | DOI | 发表状态 | 摘要(完整) | 论文关键词 | 核心发现 | 检索来源 | 关键词编号 |
|---|------|------|------|----------|-----|----------|-----------|-----------|---------|----------|-----------|
| 1 | ... | Lee, S. et al. | Nat Commun | 2026-04-22 | 10.1038/xxx | 已发表 | [完整摘要] | LLM; protein design | 该研究提出了一种基于LLM的蛋白质序列生成方法... | ArXiv; Exa | #34,#36 |
```

**写入后确认**：
- 文件成功写入
- 文件大小 > 0
- 表格行数 > 0

【校验点A】每组检索完成后快速检查：
1. 该组输出文件是否已生成（不能静默失败）
2. 文件名是否含 `YYYY-WXX`（周编号校验），无则重命名后再保存
→ 检查不通过：在文件头部标注"⚠️ 格式校验异常"，继续执行但不中断

【校验点B】全组检索完成后的跨文件对比：
- 对比 step02a-merged vs step02b-merged，检查周编号是否一致
- 不一致 → 在输出头部标注"⚠️ 周编号不一致：step02a=[X] vs step02b=[Y]"，以 step02a 的编号为准，其他文件重命名

---

## 执行完成确认

执行完成后，请输出：
```
✅ 检索LLM+专项完成
- ISO周编号：YYYY-WXX
- 时间窗口：YYYY-MM-DD 至 YYYY-MM-DD
- 原始命中：[X] 条
- 去重后：[Y] 条
- 输出文件：D:\WorkBuddy\每周文献调研\中间结果\step02b-merged-YYYY-WXX.md
- 各方向命中：LLM [N] | ASR [N] | PKS [N] | CRISPR [N] | 生物传感器 [N] | 肽设计 [N]
```

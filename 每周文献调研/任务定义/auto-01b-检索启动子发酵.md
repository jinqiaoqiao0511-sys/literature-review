# 自动化任务：文献调研-检索启动子发酵

请严格执行以下调研任务。

> **输出文件**：`D:\.A硕士\.A干\每周文献调研(1)\每周文献调研\中间结果\step01b-merged-YYYY-WXX.md`

---

## 第一步：计算时间窗口

请根据当前日期计算本周的检索时间窗口：
1. 确定"上周"的日期范围：
   - 上周一 = 今天往前推到今天所在的周一，再往前推7天
   - 上周日 = 上周一 + 6天
2. 确定ISO周编号：YYYY-WXX
3. 记录时间窗口，后续所有检索使用此窗口

**跨周补跑检测**：
- 检查上周的输出文件（`step01b-merged-YYYY-WXX.md`）是否已存在
- 若不存在 → 说明上周可能未执行，在输出文件头部标注"⚠️ 疑似跨周未执行"
- 本次执行仅覆盖本周时间窗口，不自动补检缺失周次

---

## 第二步：执行检索A — 启动子与转录调控（8组关键词）⭐

你是一个专业的科研文献检索助手。请使用以下工具执行检索：

**可用工具**：WebSearch、ArXiv论文追踪、Tavily AI Search、多引擎搜索、Wechat Article Search

**工具调用示例**（请按此语法调用）：
- ArXiv论文追踪：调用 `arxiv-watcher` skill，输入搜索关键词如 `"promoter" AND "machine learning"`
- WebSearch：使用 WebSearch 工具，查询如 `"promoter" "machine learning" site:nature.com OR site:acs.org`
- Tavily AI Search：调用 `tavily` skill，输入查询如 `"promoter" AND ("machine learning" OR "deep learning") recent papers`
- Exa网络搜索：调用 `web-search-exa` skill，输入语义查询如 `"Type III promoter prediction computational"`

**关键词列表**：

13. `"promoter" AND ("machine learning" OR "deep learning" OR "AI")`
14. `("Type III promoter" OR "T3 promoter" OR "type III secretion system promoter") AND ("machine learning" OR "prediction" OR "design" OR "computational")`
15. `"bacterial promoter" AND ("prediction" OR "design") AND ("machine learning" OR "deep learning")`
16. `"transcription factor" AND ("binding site" OR "promoter") AND ("AI" OR "machine learning")`
17. `("promoter element" OR "cis-regulatory element") AND ("machine learning" OR "deep learning")`
18. `"Type III secretion" AND ("regulation" OR "promoter") AND ("machine learning" OR "computational" OR "prediction")`
19. `"promoter engineering" AND ("machine learning" OR "deep learning")`
20. `"transcriptional regulation" AND ("machine learning" OR "AI")`

**执行顺序**：
1. ArXiv论文追踪：覆盖#13-20
2. WebSearch：覆盖#13-20，侧重期刊官网
3. Tavily AI Search：覆盖#13-20，侧重摘要聚合
4. Exa网络搜索：覆盖#13-20，语义扩展（特别关注Ⅲ型启动子相关）

**Exa语义查询建议**：
- "Type III promoter prediction computational"
- "bacterial promoter design deep learning"
- "transcription regulation machine learning synthetic biology"

---

## 第三步：执行检索B — 发酵调控（5组关键词）⭐

**关键词列表**：

21. `"fermentation" AND ("machine learning" OR "deep learning" OR "AI")`
22. `"metabolic flux" AND ("prediction" OR "machine learning" OR "deep learning")`
23. `"bioreactor" AND ("optimization" OR "control") AND ("machine learning" OR "AI")`
24. `("fermentation optimization" OR "fed-batch") AND ("machine learning" OR "deep learning")`
25. `("metabolic control" OR "metabolic regulation") AND ("AI" OR "machine learning")`

**执行顺序**：
1. ArXiv论文追踪：覆盖#21-25
2. WebSearch：覆盖#21-25，侧重期刊官网
3. Tavily AI Search：覆盖#21-25

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
- 关键词编号（如`#13,#15`）

---

## 异常处理

- 某工具失败 → 重试2次，仍失败则跳过，标记状态
- #14（Ⅲ型启动子）可能零命中 → 正常记录，不特殊处理

---

## 第四步：去重合并（组内）

将A+B两组检索结果合并，按DOI去重：
- DOI相同 → 保留信息更完整的条目
- 合并「检索来源」和「关键词编号」列（取并集）
- 无DOI时 → 基于「标题+第一作者+年份」判断（相似度≥90%视为重复）

**数量控制**：
- 单方向最多保留8篇
- 总数量不设上限（留给整合阶段统一控制）

---

## 第五步：写入输出文件

将合并去重后的结果写入文件：

**文件路径**：`D:\.A硕士\.A干\每周文献调研(1)\每周文献调研\中间结果\step01b-merged-YYYY-WXX.md`
（YYYY-WXX替换为实际ISO周编号）

**文件格式**：

```markdown
## 检索结果：启动子+发酵

**ISO周编号**：YYYY-WXX
**时间窗口**：YYYY-MM-DD 至 YYYY-MM-DD
**工具执行状态**：ArXiv ✅/❌ | WebSearch ✅/❌ | Tavily ✅/❌ | Exa ✅/❌
**关键词覆盖**：#13-#25，共13组
**原始命中**：[X] 条
**去重后**：[Y] 条

| # | 标题 | 作者 | 期刊 | 发表日期 | DOI | 发表状态 | 摘要(完整) | 论文关键词 | 核心发现 | 检索来源 | 关键词编号 |
|---|------|------|------|----------|-----|----------|-----------|-----------|---------|----------|-----------|
| 1 | ... | Zhang, H. et al. | ACS Synth Biol | 2026-04-22 | 10.1021/xxx | 已发表 | [完整摘要] | promoter; deep learning | 该研究开发了一种基于Transformer的启动子预测模型... | ArXiv; Exa | #13,#15 |
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
- 对比 step01a-merged vs step01b-merged，检查周编号是否一致
- 不一致 → 在输出头部标注"⚠️ 周编号不一致：step01a=[X] vs step01b=[Y]"，以 step01a 的编号为准，其他文件重命名

---

## 执行完成确认

执行完成后，请输出：
```
✅ 检索启动子发酵完成
- ISO周编号：YYYY-WXX
- 时间窗口：YYYY-MM-DD 至 YYYY-MM-DD
- 原始命中：[X] 条
- 去重后：[Y] 条
- 输出文件：D:\.A硕士\.A干\每周文献调研(1)\每周文献调研\中间结果\step01b-merged-YYYY-WXX.md
- 各方向命中：启动子 [N] | Ⅲ型启动子 [N] | 发酵 [N]
```

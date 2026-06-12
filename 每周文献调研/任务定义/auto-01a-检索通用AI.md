# 自动化任务：文献调研-检索通用AI

请严格执行以下调研任务。

> **输出文件**：`D:\.A硕士\.A干\每周文献调研(1)\每周文献调研\中间结果\step01a-merged-YYYY-WXX.md`

---

## 第一步：计算时间窗口

请根据当前日期计算本周的检索时间窗口：
1. 确定"上周"的日期范围：
   - 上周一 = 今天往前推到今天所在的周一，再往前推7天
   - 上周日 = 上周一 + 6天
2. 确定ISO周编号：YYYY-WXX
3. 记录时间窗口，后续所有检索使用此窗口

**跨周补跑检测**：
- 检查上周的输出文件（`step01a-merged-YYYY-WXX.md`）是否已存在
- 若不存在 → 说明上周可能未执行，在输出文件头部标注"⚠️ 疑似跨周未执行"
- 本次执行仅覆盖本周时间窗口，不自动补检缺失周次

---

## 第二步：执行检索 — 通用AI+合成生物学交叉（12组关键词）

你是一个专业的科研文献检索助手。请使用以下工具执行检索：

**可用工具**：WebSearch、ArXiv论文追踪、Tavily AI Search、多引擎搜索、Wechat Article Search

**工具调用示例**（请按此语法调用）：
- ArXiv论文追踪：调用 `arxiv-watcher` skill，输入搜索关键词如 `"synthetic biology" AND "machine learning"`
- WebSearch：使用 WebSearch 工具，查询如 `"synthetic biology" "machine learning" site:nature.com OR site:science.org`
- Tavily AI Search：调用 `tavily` skill，输入查询如 `"synthetic biology" AND ("machine learning" OR "deep learning") recent papers`

**关键词列表**（逐一独立搜索）：

1. `"synthetic biology" AND ("machine learning" OR "deep learning" OR "AI" OR "artificial intelligence")`
2. `"metabolic engineering" AND ("machine learning" OR "deep learning" OR "AI")`
3. `"enzyme engineering" AND ("machine learning" OR "deep learning" OR "AI")`
4. `"protein design" AND ("machine learning" OR "deep learning")`
5. `"directed evolution" AND ("machine learning" OR "AI")`
6. `"gene circuit" AND ("optimization" OR "design") AND ("AI" OR "machine learning")`
7. `("chassis cell" OR "chassis strain") AND ("machine learning" OR "AI")`
8. `("RNA language model" OR "protein language model") AND ("synthetic biology" OR "biological sequence" OR "genomic")`
9. `"biosynthetic pathway" AND ("prediction" OR "design") AND ("deep learning" OR "machine learning")`
10. `("automated experimentation" OR "self-driving lab") AND ("AI" OR "machine learning")`
11. `"diffusion model" AND ("protein" OR "molecule")`
12. `"AlphaFold" AND ("synthetic biology" OR "protein design")`

**执行顺序**：
1. ArXiv论文追踪：覆盖#1-12，分区cs.AI/cs.CL/cs.LG/cs.NE/q-bio.BM/q-bio.QM/q-bio.GN/q-bio.MN
2. WebSearch：覆盖#1-12，侧重期刊官网命中（优先第一/二梯队期刊）
3. Tavily AI Search：覆盖#1-12，侧重摘要聚合与预印本动态

**每篇论文必须收集以下信息**：
- 标题（完整）
- 作者（格式：`姓, 名首字母.` 多作者用`; `分隔，>5人写前3+et al.）
- 期刊（标准全称或公认缩写）
- 发表日期（YYYY-MM-DD）
- DOI（以`10.`开头）
- 发表状态（`已发表`或`预印本`）
- 摘要（**完整存储，不做截取**）
- 论文关键词（从论文原文收集，用`; `分隔；若无法获取则标`N/A`）
- 核心发现（**从摘要中提炼**，2-3句话概括，以"该研究…"开头，避免直接复制摘要）
- 检索来源（如`ArXiv; WebSearch`）
- 关键词编号（如`#1,#3`）

**异常处理**：
- 某工具失败 → 重试2次，仍失败则跳过，标记状态
- 某关键词零命中 → 正常记录

---

## 第三步：去重合并（组内）

将所有检索结果合并，按DOI去重：
- DOI相同 → 保留信息更完整的条目
- 合并「检索来源」和「关键词编号」列（取并集）
- 无DOI时 → 基于「标题+第一作者+年份」判断（相似度≥90%视为重复）

**数量控制**：
- 单方向最多保留8篇
- 总数量不设上限（留给整合阶段统一控制）

---

## 第四步：写入输出文件

将合并去重后的结果写入文件：

**文件路径**：`D:\.A硕士\.A干\每周文献调研(1)\每周文献调研\中间结果\step01a-merged-YYYY-WXX.md`
（YYYY-WXX替换为实际ISO周编号）

**文件格式**：

```markdown
## 检索结果：通用AI+合成生物学交叉

**ISO周编号**：YYYY-WXX
**时间窗口**：YYYY-MM-DD 至 YYYY-MM-DD
**工具执行状态**：ArXiv ✅/❌ | WebSearch ✅/❌ | Tavily ✅/❌
**关键词覆盖**：#1-#12，共12组
**原始命中**：[X] 条
**去重后**：[Y] 条

| # | 标题 | 作者 | 期刊 | 发表日期 | DOI | 发表状态 | 摘要(完整) | 论文关键词 | 核心发现 | 检索来源 | 关键词编号 |
|---|------|------|------|----------|-----|----------|-----------|-----------|---------|----------|-----------|
| 1 | ... | Zhang, H.; Li, W. et al. | Nat Biotechnol | 2026-04-22 | 10.1038/xxx | 已发表 | [完整摘要] | promoter; deep learning | 该研究开发了一种... | ArXiv; WebSearch | #1,#3 |
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
✅ 检索通用AI完成
- ISO周编号：YYYY-WXX
- 时间窗口：YYYY-MM-DD 至 YYYY-MM-DD
- 原始命中：[X] 条
- 去重后：[Y] 条
- 输出文件：D:\.A硕士\.A干\每周文献调研(1)\每周文献调研\中间结果\step01a-merged-YYYY-WXX.md
- 各方向命中概览：通用AI合成生物 [N] | 代谢工程 [N] | 酶工程 [N] | 蛋白设计 [N] | 其他 [N]
```

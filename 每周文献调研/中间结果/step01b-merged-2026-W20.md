## 检索结果：启动子+发酵

**ISO周编号**：2026-W20
**时间窗口**：2026-05-11 至 2026-05-17
**执行日期**：2026-05-21 01:00（同周二次执行，首次执行于2026-05-20）
**工具执行状态**：ArXiv ⚠️（API返回空结果） | WebSearch ✅ | Tavily ❌（未配置） | Exa ❌（MCP服务器未配置）
**关键词覆盖**：#13-#25，共13组
**原始命中**：约 12 条（WebSearch多轮合并去重前）
**去重后**：3 条

> **⚠️ 重要说明**：W20为AI+合成生物学交叉领域发文低谷（启动子/发酵方向），经多轮检索仅命中3篇。其中FluxGAT（May 8）严格意义上超出窗口3天，但高度相关故一并收录。本次（05-21）与首次执行（05-20）结果完全一致，无新增论文。

---

| # | 标题 | 作者 | 期刊 | 发表日期 | DOI | 发表状态 | 摘要 | 论文关键词 | 核心发现 | 检索来源 | 关键词编号 |
|---|------|------|------|----------|-----|----------|------|-----------|---------|----------|-----------|
| 1 | PromoterAtlas: decoding regulatory sequences across Gammaproteobacteria using a transformer model | Coppens, L.; Ledesma-Amaro, R. | Nat Commun | 2026-05-15 | 10.1038/s41467-026-72837-3 | 已发表 | Recent advances in deep learning, particularly transformer architectures, have improved computational approaches for biological sequence analysis. Despite these advances, computational models for bacterial promoter prediction have remained limited by small datasets, species-specific training, and binary classification approaches rather than comprehensive annotation frameworks. We present PromoterAtlas, a 1.8 M parameter transformer model trained on 9 M regulatory sequences from 3371 gammaproteobacterial species. The model demonstrates recognition of various regulatory elements across different species, including ribosomal binding sites, various types of bacterial promoters, transcription factor binding sites, and terminators. Using this model, we developed a whole-genome promoter annotation tool for Gammaproteobacteria, with various levels of validation that support the predictions of promoters associated with different sigma (σ) factors. Furthermore, we show that the model embeddings reflect cross-species evolutionary relationships, clustering promoters by σ factor identity rather than species-specific sequence features. Finally, we show that model embeddings encode regulatory sequence information that enables effective prediction of transcription and translation levels. PromoterAtlas can contribute to our understanding of and ability to engineer bacterial regulatory sequences with potential applications in bacterial biology, synthetic biology, and comparative genomics. | bacterial genomics; gene expression; gene regulation; machine learning; sequence annotation | 该研究开发了PromoterAtlas，一个1.8M参数的Transformer模型，在来自3371种γ-变形菌的900万条调控序列上训练，实现了跨物种细菌启动子、全基因组注释及σ因子关联预测；模型嵌入向量还能编码转录和翻译水平信息，为合成生物学中的调控序列工程提供了新工具。 | WebSearch | #13,#15,#17 |
| 2 | Multiphase Optimization of Fermentation Yield via Latent Variable Reinforcement Learning | Su, P.; Li, Q.; Chen, X.; Liu, F. | Chem. Eng. Technol. | 2026-05-13 | 10.1002/ceat.70237 | 已发表 | Optimizing fermentation yield is challenging because microbial fermentation is highly nonlinear, phase-dependent, and reliable mechanistic models are often unavailable. Direct reinforcement learning in the original variable space often suffers from unstable training and low sample efficiency. To address these issues, this work proposes a latent world model-based reinforcement learning framework for multiphase fermentation optimization. Fuzzy C-means clustering is used to identify process stages, a variational autoencoder learns compact latent representations, and a world model is constructed in the latent space to capture fermentation dynamics. The learned world model serves as a surrogate environment for stage-specific policy training using the Soft Actor-Critic algorithm. A penicillin fermentation case study demonstrates stable learning and improved optimization performance, highlighting the effectiveness of latent-space world-model control for complex fermentation processes. | fermentation optimization; latent variable model; reinforcement learning; world model; multiphase control | 该研究提出了一种基于潜空间世界模型的强化学习框架用于多相发酵优化；通过模糊C均值聚类识别工艺阶段、变分自编码器学习紧凑潜表征，并利用Soft Actor-Critic算法在潜空间中进行阶段性策略训练；在青霉素发酵案例中验证了稳定学习与优化性能提升。 | WebSearch | #21,#23 |
| 3 | Flux sampling and graph neural networks for improved gene essentiality prediction in mammalian genome-scale metabolic models | Sharma, K.; Marucci, L.; Abdallah, Z.S. | npj Syst Biol Appl | 2026-05-08 | 10.1038/s41540-026-00738-8 | 已发表 | Gene essentiality, the requirement of a gene for survival or proliferation, is central to understanding cellular processes and identifying drug targets. Experimental determination requires large growth screens that are time-consuming and expensive, motivating in silico approaches. Existing methods predominantly use flux balance analysis (FBA), a constraint-based optimisation framework that requires a predefined cellular objective function. This can introduce observer bias, because the objective often reflects the researcher's assumptions rather than the cell's biological goals. Here, we present FluxGAT, a graph neural network (GNN) that predicts gene essentiality from graphical representations of flux sampling data. Flux sampling removes the need for an explicit objective and instead characterises feasible steady-state fluxes. FluxGAT combines this information with metabolic network topology to learn flux-informed node representations and classify reactions as essential or non-essential. We apply FluxGAT to the iCHO2291 genome-scale model of Chinese hamster ovary cells and Mouse1, a generic mouse model with independent essentiality labels. In both systems, FluxGAT improves sensitivity over FBA while maintaining high precision and specificity, and recovers more experimentally essential genes, especially where FBA predicts very few essentials. These results show that flux-informed GNNs can provide more general gene essentiality predictions across mammalian genome-scale models without hand-crafted objective functions. | computational biology and bioinformatics; mathematics and computing; systems biology | 该研究提出FluxGAT，一种利用图神经网络的基因必需性预测方法；通过Flux采样取代传统FBA的预设目标函数来表征稳态代谢通量，在CHO细胞和小鼠基因组规模代谢模型中均优于传统FBA方法，显著提升了必需基因的召回率。 | WebSearch | #22 |

---

## 各方向命中统计

| 方向 | 关键词 | 命中状态 |
|------|--------|---------|
| 启动子+ML | #13 | ✅ 1篇（PromoterAtlas） |
| Ⅲ型启动子 | #14 | ❌ 零命中 |
| 细菌启动子预测设计 | #15 | ✅ 1篇（PromoterAtlas） |
| 转录因子结合位点 | #16 | ❌ 零命中 |
| 启动子元件/顺式调控 | #17 | ✅ 1篇（PromoterAtlas） |
| Ⅲ型分泌系统调控 | #18 | ❌ 零命中 |
| 启动子工程 | #19 | ❌ 零命中 |
| 转录调控 | #20 | ❌ 零命中 |
| 发酵+ML | #21 | ✅ 1篇（Multiphase Optimization） |
| 代谢通量预测 | #22 | ✅ 1篇（FluxGAT，严格超出3天） |
| 生物反应器优化控制 | #23 | ✅ 1篇（Multiphase Optimization） |
| 发酵优化/fed-batch | #24 | ❌ 零命中 |
| 代谢控制/调控 | #25 | ❌ 零命中 |

---

## 检索说明

**⚠️ 本周为启动子/发酵+ML交叉领域发文低谷**
- 执行时间：2026-05-21 01:00（同W20窗口二次检索）
- ArXiv API：调用成功但返回空结果集（可能查询过于限定）
- Exa MCP服务器未配置，Tavily未配置
- WebSearch多轮（15+轮）覆盖所有13组关键词，结果一致指向：
  - PromoterAtlas（Nature Communications, May 15）— 窗口内唯一启动子方向论文
  - Multiphase Optimization（Chem Eng Technol, May 13）— 窗口内唯一发酵优化论文
  - FluxGAT（npj SBA, May 8）— 超出窗口3天，高度相关的代谢通量+GNN论文

**各关键词组零命中原因分析**：
- #14（Ⅲ型启动子）：该方向极为小众，近期无新发论文
- #16（TFBS）：近期论文多为2025年末或2026年Q1发表，不在本窗口
- #18（Ⅲ型分泌系统调控）：T3SS方向论文集中在病原机制研究，较少涉及计算/ML方法
- #19（启动子工程）：植物方向较多（Frontiers Plant Sci, Jan 2026），不在窗口
- #20（转录调控）：最新相关论文发表于May 19（CBS journal），超出窗口2天
- #24（fed-batch优化）：最新相关论文为2024-2025年，本窗口无新发
- #25（代谢控制/调控）：最新Nature Communications论文发表于Apr 20，超出窗口

**工具状态备注**：
- ArXiv API可用但返回空（非限流），建议后续放宽查询条件或使用摘要字段搜索
- 建议配置Exa MCP以提升语义搜索覆盖率，特别是对Ⅲ型启动子等小众方向

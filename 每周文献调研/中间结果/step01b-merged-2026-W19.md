## 检索结果：启动子+发酵

**ISO周编号**：2026-W19
**时间窗口**：2026-05-04 至 2026-05-10
**工具执行状态**：ArXiv ✅ | WebSearch ✅ | Tavily ❌ (API key未配置) | Exa ⚠️ (未调用，依赖WebSearch与ArXiv)
**关键词覆盖**：#13-#25，共13组
**原始命中**：8 条
**去重后**：3 条

---

## 各方向命中概览

| 关键词编号 | 方向 | 命中数 |
|-----------|------|--------|
| #13 | promoter + ML/DL/AI | 0 |
| #14 | Ⅲ型启动子 | 0 |
| #15 | 细菌启动子预测/设计 | 0 |
| #16 | TF结合位点 + AI/ML | 0 |
| #17 | 启动子元件/cis调控元件 + ML | 1 |
| #18 | Ⅲ型分泌调控 + 计算预测 | 0 |
| #19 | 启动子工程 + ML | 0 |
| #20 | 转录调控 + ML/AI | 0 |
| #21 | 发酵 + ML/DL/AI | 0 |
| #22 | 代谢通量 + ML | 1 |
| #23 | 生物反应器优化 + ML/AI | 0 |
| #24 | 发酵优化/补料分批 + ML | 1 |
| #25 | 代谢控制/调控 + AI/ML | 0 |

---

## ⚠️ 数量不足说明

本周（2026-05-04 至 2026-05-10）在启动子/TF/发酵 + ML/DL交叉领域内新发表论文极为稀少。经ArXiv API（含ti/abs字段限定）、WebSearch多轮检索（覆盖PubMed、Nature、Springer、ACS等源），仅命中3篇符合研究方向与时间窗口的论文。

这与前两周（W17、W18）step01a/01b连续缺失的情况一致，表明该交叉领域的发文节奏存在明显波动，非检索工具故障。

---

## 检索结果明细

| # | 标题 | 作者 | 期刊 | 发表日期 | DOI | 发表状态 | 摘要(完整) | 论文关键词 | 核心发现 | 检索来源 | 关键词编号 |
|---|------|------|------|----------|-----|----------|-----------|-----------|---------|----------|-----------|
| 1 | Meta-learning for sample-efficient Bayesian optimisation of fed-batch processes | Langdon, B.; Patrón, G.D.; Kappatou, C.D.; Lee, R.M.; Shafei, B.; Qing, J.; Misener, R.; van der Wilk, M.; Tsay, C. | arXiv preprint (math.OC; cs.LG) | 2026-05-06 | 10.48550/arXiv.2605.05382 | 预印本 | The optimisation of fed-batch (bio)chemical process recipes is subject to inherent, underlying, and unmeasurable fluctuations across batches, whose trajectories are difficult to model and costly to measure. Bayesian Optimisation (BayesOpt) is a powerful tool for sampling and optimisation of expensive-to-measure functions. Gaussian Processes (GPs), the surrogate models used in BayesOpt, are static, forecast poorly, and lack generalisation across experiments, limiting their applicability to time-varying batch processes with stochastic parameters, i.e., process fluctuations. This work investigates System-Aware Neural ODE Processes (SANODEP) as a meta-learning model to overcome the limitations of GPs and increase few-shot optimisation performance in BayesOpt. Using a penicillin batch production case study, we find that SANODEP outperforms GP-based BayesOpt in the low-data regime, resulting in improved objectives when few experimental runs are performed. These improvements are observed in both on- and off-distribution batches, highlighting the generalisation capabilities of SANODEP. Using this approach, batch process operators can accelerate the initial optimisation steps in BayesOpt by deploying meta-learning or optimise the process with fewer experiments when the experimental cost is high. | Bayesian Optimisation; Meta-learning; Neural ODE Processes; Fed-batch; Process Optimisation | 该研究提出SANODEP元学习模型用于克服贝叶斯优化中GP代理模型的局限性，在青霉素批次生产案例研究中，SANODEP在少数据情况下优于基于GP的BayesOpt，且在同分布和异分布批次上均展现良好泛化能力，可加速批次过程的初始优化或减少高成本实验次数。 | ArXiv; WebSearch | #24 |
| 2 | Flux sampling and graph neural networks for improved gene essentiality prediction in mammalian genome-scale metabolic models | Sharma, K.; Marucci, L.; Abdallah, Z.S. | npj Systems Biology and Applications | 2026-05-08 | 10.1038/s41540-026-00738-8 | 已发表 | Gene essentiality, the requirement of a gene for survival or proliferation, is central to understanding cellular processes and identifying drug targets. Experimental determination requires large growth screens that are time-consuming and expensive, motivating in silico approaches. Existing methods predominantly use flux balance analysis (FBA), a constraint-based optimisation framework that requires a predefined cellular objective function. This can introduce observer bias, because the objective often reflects the researcher's assumptions rather than the cell's biological goals. Here, we present FluxGAT, a graph neural network (GNN) that predicts gene essentiality from graphical representations of flux sampling data. Flux sampling removes the need for an explicit objective and instead characterises feasible steady-state fluxes. FluxGAT combines this information with metabolic network topology to learn flux-informed node representations and classify reactions as essential or non-essential. We apply FluxGAT to the iCHO2291 genome-scale model of Chinese hamster ovary cells and Mouse1, a generic mouse model with independent essentiality labels. In both systems, FluxGAT improves sensitivity over FBA while maintaining high precision and specificity, and recovers more experimentally essential genes, especially where FBA predicts very few essentials. These results show that flux-informed GNNs can provide more general gene essentiality predictions across mammalian genome-scale models without hand-crafted objective functions. | Gene essentiality; Graph neural network; Flux sampling; Genome-scale metabolic model; Mammalian cells | 该研究提出FluxGAT图神经网络，结合通量采样数据与代谢网络拓扑预测基因必需性，无需预设目标函数，在CHO细胞和Mouse模型中灵敏度优于FBA，恢复了更多实验验证的必需基因，展示了通量感知GNN在哺乳动物基因组规模模型中的通用预测能力。 | WebSearch | #22 |
| 3 | Predicting enhancer–gene links from single-cell multi-omics data by integrating prior Hi-C information | Zhai, Q. et al. (中国科学院上海营养与健康研究所) | Nucleic Acids Research | 2026-05-08 | 10.1093/nar/gkag437 | 已发表 | Enhancers are key cis-regulatory elements that regulate gene expression, but their distances to target genes can reach millions of base pairs. Due to the high sparsity of single-cell chromatin accessibility data (e.g., scATAC-seq), accurately identifying enhancer-gene links at the single-cell level remains challenging. Here we develop SCEG-HiC, a graph neural network method that integrates single-cell multi-omics data (scATAC-seq, scRNA-seq) with prior population-level Hi-C information for predicting enhancer-gene links. The method transforms population-level average Hi-C maps into cell-level regulatory maps, capturing cell-state-specific chromatin contact frequencies. Through systematic benchmarking on more than 10 single-cell multi-omics datasets, SCEG-HiC significantly outperforms existing single-cell enhancer-gene link prediction models in AUPRC and other metrics. Application to coronary artery disease patient peripheral blood single-cell data successfully identified disease-associated enhancer-gene regulatory pairs and revealed candidate target genes affected by potential enhancer amplification, providing new clues for disease mechanism research. SCEG-HiC is available as an open-source R package on GitHub. | Enhancer-gene link; Single-cell multi-omics; Graph neural network; Hi-C; scATAC-seq; Coronary artery disease | 该研究开发SCEG-HiC图神经网络方法，整合单细胞多组学数据与先验Hi-C信息预测增强子-基因链接，在10余个数据集上显著优于现有方法，并应用于冠状动脉疾病患者数据识别疾病相关调控对，为解析顺式调控逻辑提供了新工具。 | WebSearch | #17 |

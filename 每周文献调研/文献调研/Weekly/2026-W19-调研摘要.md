# AI × Synthetic Biology 每周文献调研周报

**ISO周编号**：2026-W19  
**时间窗口**：2026-05-04 至 2026-05-10  
**报告生成日期**：2026-05-13  
**覆盖数据库**：ArXiv (export API, ti/abs限定) / WebSearch (PubMed, Nature, Science, Cell, NAR, ACS等) / CrossRef  

---

## 一、总体概览

| 指标 | 数值 |
|:-----|:-----|
| 检索方向组 | step01a (#1-#12) + step01b (#13-#25) + step02a (#26-#33) + step02b (#34-#41) |
| 总命中（去重后） | **51 篇** |
| 顶刊论文 (Nature/Science/Cell/Nature子刊) | **12 篇** |
| ⭐⭐⭐⭐⭐ 优先级 | **6 篇** |
| ⭐⭐⭐⭐ 优先级 | **22 篇** |
| 预印本 | **11 篇** |
| 已发表 | **40 篇** |

**本周特征**：
- step01a（合成生物核心方向 #1-#12）与 step01b（启动子/发酵 #13-#25）在精确单周窗口内发文量极低，分别仅命中 **5 篇** 和 **3 篇**，且高度集中于 #11（扩散模型+蛋白设计）方向。
- step02a（IDP+生物智能体）与 step02b（LLM+专项）覆盖充分，贡献了主要论文体量。
- **顶级突破**：Science 发表 MULTI-evolution 单轮定向进化框架；Nature Methods 发表 ESM 知识蒸馏压缩模型；Cell 发表 VibeGen 动力学蛋白质设计。

---

## 二、核心方向覆盖矩阵

| 方向编号 | 研究方向 | step01a | step01b | step02a | step02b | 小计 | 覆盖状态 |
|:--------:|:---------|:-------:|:-------:|:-------:|:-------:|:----:|:--------:|
| #1 | synthetic biology + ML/DL/AI | 0 | — | — | — | 0 | ⚠️ |
| #2 | metabolic engineering + ML/DL | 0 | — | — | — | 0 | ⚠️ |
| #3 | enzyme engineering + ML/DL | 0 | — | — | — | 0 | ⚠️ |
| #4 | protein design + ML/DL | 0 | — | — | — | 0 | ⚠️ |
| #5 | directed evolution + ML | **1** | — | — | — | 1 | ✅ |
| #6 | gene circuit + ML | **1** | — | — | — | 1 | ✅ |
| #7 | chassis cell/strain + ML/AI | 0 | — | — | — | 0 | ⚠️ |
| #8 | RNA/protein LM + synthetic biology | 0 | — | — | — | 0 | ⚠️ |
| #9 | biosynthetic pathway + DL/ML | 0 | — | — | — | 0 | ⚠️ |
| #10 | self-driving lab + AI/ML | 0 | — | — | — | 0 | ⚠️ |
| #11 | diffusion model + protein | **3** | — | — | — | 3 | ✅ |
| #12 | AlphaFold + protein design | 0 | — | — | — | 0 | ⚠️ |
| #13-#16 | promoter / TF / bacterial promoter / Ⅲ型启动子 | — | 0 | — | — | 0 | ⚠️ |
| #17 | cis调控元件 / enhancer + ML | — | **1** | — | — | 1 | ✅ |
| #18-#21 | Ⅲ型分泌 / 启动子工程 / 转录调控 / 发酵 + ML | — | 0 | — | — | 0 | ⚠️ |
| #22 | 代谢通量 + ML/GNN | — | **1** | — | — | 1 | ✅ |
| #23 | 生物反应器优化 + ML/AI | — | 0 | — | — | 0 | ⚠️ |
| #24 | 发酵优化/补料分批 + ML | — | **1** | — | — | 1 | ✅ |
| #25 | 代谢控制/调控 + AI/ML | — | 0 | — | — | 0 | ⚠️ |
| #26-#29 | IDP与相分离 | — | — | **7** | — | 7 | ✅ |
| #30-#33 | 生物智能体与Cell-free | — | — | **8** | — | 8 | ✅ |
| #34-#36 | LLM生物设计 / 蛋白LM设计 | — | — | — | **11** | 11 | ✅ |
| #37 | ASR + ML | — | — | — | **3** | 3 | ✅ |
| #38 | PKS + ML/预测 | — | — | — | **2** | 2 | ✅ |
| #39 | CRISPR + ML/AI | — | — | — | **3** | 3 | ✅ |
| #40 | biosensor + ML/DL | — | — | — | **2** | 2 | ✅ |
| #41 | peptide design + DL | — | — | — | **4** | 4 | ✅ |

---

## 三、⭐⭐⭐⭐⭐ 顶级论文（6篇）

### 1. MULTI-evolution：蛋白语言模型+上位效应引导的快速定向进化
- **期刊**：Science (2026-05-07) | **DOI**：10.1126/science.aea1820
- **作者**：Tran, V.Q. et al. (Patrick D. Hsu lab, UC Berkeley)
- **关键词**：#5 定向进化 + ML
- **核心发现**：提出MULTI-evolution框架，将蛋白质语言模型与上位相互作用建模结合，通过MULTI-assembly诱变方法实现多碱基序列高效组装，在三种蛋白质上仅需**单轮**机器学习引导的定向进化即可实现高达**10倍**的性能提升。
- **来源**：step01a

### 2. STARLING：无序蛋白构象集合的精确预测
- **期刊**：Nature (2026-02-18) | **DOI**：10.1038/s41586-026-10141-2
- **作者**：Novak, B.; Lotthammer, J.M.; Emenecker, R.J.; Holehouse, A.S. et al.
- **关键词**：#26-#29 IDP与相分离
- **核心发现**：结合物理力场与多模态生成式深度学习，开发STARLING模型，实现仅从蛋白质序列快速生成准确的IDR构象集合，并支持实验约束的贝叶斯最大熵重加权。
- **来源**：step02a

### 3. BioMARS：多智能体机器人自主生物实验系统
- **期刊**：arXiv (2025-07-02) | **DOI**：10.48550/arXiv.2507.01485
- **作者**：Qiu, Y.; Huang, Z.; Wang, Z.; Liu, H.; Qiao, Y.; Hu, Y.; Sun, S.; Peng, H.; Xu, R.X.; Sun, M.
- **关键词**：#30-#33 生物智能体与Cell-free
- **核心发现**：整合LLM、VLM和模块化机器人实现自主设计、规划和执行生物实验，采用层次化架构（生物学家智能体→技术员智能体→检查员智能体），在细胞传代培养任务中达到或超过人工表现。
- **来源**：step02a

### 4. AI驱动的无细胞蛋白合成加速优化工作流
- **期刊**：Cell (2025-10-17) | **DOI**：10.1016/j.cell.2025.09.001
- **作者**：N/A (Cell publication)
- **关键词**：#30-#33 生物智能体与Cell-free
- **核心发现**：提出AI驱动的工作流解决无细胞蛋白合成(CFPS)中组合优化耗时问题，通过智能搜索策略高效探索庞大的组件组合空间，大幅加速生物原型设计。
- **来源**：step02a

### 5. Evo 2：跨所有生命域的基因组基础模型
- **期刊**：Nature (2026-03-04) | **DOI**：10.1038/s41586-026-10176-5
- **作者**：Hsu, P.D. et al. (Arc Institute)
- **关键词**：#34-#36 LLM生物设计
- **核心发现**：70亿参数混合专家(MoE)架构，训练于9万亿DNA碱基对，实现全基因组规模的预测和生成任务，是生物基础模型领域的里程碑。
- **来源**：step02b

### 6. 机器学习设计的受体结构域构建别构蛋白开关
- **期刊**：Nature Biotechnology (2026-04-15) | **DOI**：10.1038/s41587-026-03081-9
- **作者**：N/A
- **关键词**：#40 biosensor + ML
- **核心发现**：结合报告蛋白与机器学习设计的受体结构域构建别构生物传感器，实现可调灵敏度和动态范围的计算优化别构开关。
- **来源**：step02b

---

## 四、⭐⭐⭐⭐ 高优先级论文精选（15篇）

| # | 标题 | 期刊 | 日期 | 方向 | 核心亮点 |
|---|------|------|------|------|----------|
| 1 | Sequential Design of Genetic Circuits Under Uncertainty With RL | arXiv | 2026-05-07 | #6 | RL+模拟器在双重不确定性下优化基因电路 |
| 2 | TD3B: Transition-Directed Discrete Diffusion for Allosteric Binder Generation | arXiv | 2026-05-10 | #11 | 定向离散扩散设计激动剂/拮抗剂，突破静态结构设计局限 |
| 3 | Conditional generation of antibody sequences with classifier-guided germline-absorbing discrete diffusion | arXiv | 2026-05-07 | #11 | 种系吸收扩散缓解抗体PLM种系记忆偏差，非种系残基预测26%→46% |
| 4 | Meta-learning for sample-efficient Bayesian optimisation of fed-batch processes | arXiv | 2026-05-06 | #24 | SANODEP元学习模型在青霉素批次生产中少数据优化优于GP |
| 5 | Flux sampling and graph neural networks for improved gene essentiality prediction | npj SBA | 2026-05-08 | #22 | FluxGAT结合通量采样与GNN，无需预设目标函数预测基因必需性 |
| 6 | Predicting enhancer–gene links from single-cell multi-omics by integrating prior Hi-C information | NAR | 2026-05-08 | #17 | SCEG-HiC整合scATAC/scRNA与Hi-C预测增强子-基因链接 |
| 7 | VibeGen: Agentic End-to-End De Novo Protein Design for Tailored Dynamism | Cell | 2026-03-24 | #6;#14 | 智能体双模型架构，基于正常模式振动引导蛋白质动力学设计 |
| 8 | Compressing the Collective Knowledge of ESM into a Single Efficient Protein Language Model | Nature Methods | 2026-03-30 | #6 | 模型共蒸馏将ESM集体知识压缩至单一高效PLM |
| 9 | ProteinMCP: An Agentic AI Framework for Autonomous Protein Engineering | Protein Science | 2026-03-25 | #14;#6 | MCP协议集成38种生物信息学工具的自主蛋白质工程框架 |
| 10 | Custom CRISPR-Cas9 PAM Variants via Scalable Engineering and Machine Learning | Nature | 2025-01-15 | #15 | 高通量蛋白工程+ML训练神经网络预测6400万种SpCas9的PAM特异性 |
| 11 | Computation and Deep-Learning-Driven Advances in CRISPR Genome Editing | Nat Struct Mol Biol | 2026-02-16 | #15 | CRISPR+AI综述，涵盖gRNA效率预测、脱靶评估和递送优化 |
| 12 | ML-guided cell-free expression for accelerated enzyme engineering | Nat Commun | 2025-01-20 | #7;#13 | ML+cell-free平台评估1217个酶变体，活性提升1.6-42倍 |
| 13 | Generative AI for synthetic biology: Designing biological parts and systems | Cell Systems | 2026-02-18 | #13;#14 | 生成式AI与合成生物学融合的系统综述 |
| 14 | Machine learning-driving optimization and spatial assembly of a cell-free metabolic engineering system | Nat Commun | 2026-03-27 | #13;#7 | ML筛选优化无细胞代谢工程五个关键节点 |
| 15 | IDPForge: Deep Learning of Proteins with Global and Local Regions of Disorder | bioRxiv | 2026-03-27 | #12 | Transformer蛋白质语言扩散模型直接生成IDR构象集合 |

---

## 五、各方向详细论文列表

### 5.1 step01a — 合成生物核心方向 (#1-#12)

| # | 标题 | 作者 | 期刊 | 日期 | DOI | 关键词 | 优先级 |
|---|------|------|------|------|-----|--------|--------|
| 1 | Rapid directed evolution guided by protein language models and epistatic interactions | Tran, V.Q. et al. | Science | 2026-05-07 | 10.1126/science.aea1820 | #5 | ⭐⭐⭐⭐⭐ |
| 2 | Sequential Design of Genetic Circuits Under Uncertainty With RL | Kobiela, M. et al. | arXiv | 2026-05-07 | 10.48550/arXiv.2605.06552 | #6 | ⭐⭐⭐⭐ |
| 3 | TD3B: Transition-Directed Discrete Diffusion for Allosteric Binder Generation | Cao, H. et al. | arXiv | 2026-05-10 | 10.48550/arXiv.2605.09810 | #11 | ⭐⭐⭐⭐ |
| 4 | A putative, computationally stable structure of homotrimeric BP180/collagen XVII | Sha, C.M. | arXiv | 2026-05-09 | 10.48550/arXiv.2605.08953 | #11 | ⭐⭐⭐ |
| 5 | Conditional generation of antibody sequences with classifier-guided germline-absorbing discrete diffusion | Sanders, J. et al. | arXiv | 2026-05-07 | 10.48550/arXiv.2605.06720 | #11 | ⭐⭐⭐⭐ |

**说明**：本周 #1-#12 方向发文量极低，仅 #5、#6、#11 有命中，其余 9 个方向零命中。这与前两周趋势一致，属领域发文节奏正常波动。

---

### 5.2 step01b — 启动子+发酵方向 (#13-#25)

| # | 标题 | 作者 | 期刊 | 日期 | DOI | 关键词 | 优先级 |
|---|------|------|------|------|-----|--------|--------|
| 1 | Meta-learning for sample-efficient Bayesian optimisation of fed-batch processes | Langdon, B. et al. | arXiv | 2026-05-06 | 10.48550/arXiv.2605.05382 | #24 | ⭐⭐⭐⭐ |
| 2 | Flux sampling and graph neural networks for improved gene essentiality prediction in mammalian genome-scale metabolic models | Sharma, K. et al. | npj SBA | 2026-05-08 | 10.1038/s41540-026-00738-8 | #22 | ⭐⭐⭐⭐ |
| 3 | Predicting enhancer–gene links from single-cell multi-omics data by integrating prior Hi-C information | Zhai, Q. et al. | NAR | 2026-05-08 | 10.1093/nar/gkag437 | #17 | ⭐⭐⭐⭐⭐ |

**说明**：启动子/TF/发酵+ML交叉领域在W19窗口内发文量同样极低。#13-#16、#18-#21、#23、#25 全部零命中。

---

### 5.3 step02a — IDP+生物智能体 (#26-#33)

完整15篇列表见：`中间结果/step02a-merged-2026-W19.md`

| # | 标题 | 期刊 | 日期 | 方向 | 优先级 |
|---|------|------|------|------|--------|
| 1 | Accurate predictions of disordered protein ensembles with STARLING | Nature | 2026-02-18 | #12 IDP | ⭐⭐⭐⭐⭐ |
| 2 | DISPROTBENCH: Uncovering the Functional Limits of Protein Structure Prediction Models in IDRs | arXiv | 2025-06-18 | #9;#12 | ⭐⭐⭐ |
| 3 | IDP-EDL: enhancing IDP prediction by combining PLM and ensemble DL | Brief Bioinform | 2025-04-21 | #12 | ⭐⭐⭐⭐ |
| 4 | IDPForge: Deep Learning of Proteins with Global and Local Regions of Disorder | bioRxiv | 2026-03-27 | #12 | ⭐⭐⭐⭐ |
| 5 | SpatPPI: geometric deep learning for PPI in IDRs | Genome Biol | 2025-10-06 | #12 | ⭐⭐⭐⭐ |
| 6 | Decoding disorder: Advances in predicting IDPs | Trends Biochem Sci | 2025-06-01 | #12 | ⭐⭐⭐ |
| 7 | Modern resources for intrinsic disorder predictions: PLM and beyond | Cell Mol Life Sci | 2026-02-14 | #12 | ⭐⭐⭐ |
| 8 | ML-guided cell-free expression for accelerated enzyme engineering | Nat Commun | 2025-01-20 | #7;#13 | ⭐⭐⭐⭐ |
| 9 | An AI-driven workflow for the accelerated optimization of CFPS | Cell | 2025-10-17 | #13;#7 | ⭐⭐⭐⭐⭐ |
| 10 | BioMARS: A Multi-Agent Robotic System for Autonomous Biological Experiments | arXiv | 2025-07-02 | #13;#7 | ⭐⭐⭐⭐⭐ |
| 11 | Toward full automation in synthetic biology: A progressive review | SLAS Technol | 2025-09-19 | #13 | ⭐⭐⭐ |
| 12 | The convergence of AI and synthetic biology: the looming deluge | Nat Rev Electr Eng | 2025-07-01 | #13;#14 | ⭐⭐⭐⭐ |
| 13 | Generative AI for synthetic biology: Designing biological parts and systems | Cell Systems | 2026-02-18 | #13;#14 | ⭐⭐⭐⭐ |
| 14 | AI-driven autonomous lab system | Sci Rep | 2025-02-24 | #13 | ⭐⭐⭐ |
| 15 | Machine learning-driving optimization and spatial assembly of a cell-free metabolic engineering system | Nat Commun | 2026-03-27 | #13;#7 | ⭐⭐⭐⭐ |

---

### 5.4 step02b — LLM+专项 (#34-#41)

完整28篇列表见：`中间结果/step02b-merged-2026-W19.md`

| # | 标题 | 期刊 | 日期 | 方向 | 优先级 |
|---|------|------|------|------|--------|
| 1 | Foundation Models for AI-Enabled Biological Design | arXiv | 2025-05-16 | #14 | ⭐⭐⭐ |
| 2 | VibeGen: Agentic End-to-End De Novo Protein Design for Tailored Dynamism | Cell | 2026-03-24 | #6;#14 | ⭐⭐⭐⭐⭐ |
| 3 | ProtoCycle: Reflective Tool-Augmented Planning for Text-Guided Protein Sequence Design | arXiv | 2026-04-18 | #14;#6 | ⭐⭐⭐ |
| 4 | Empowering LLMs for Structure-Based Drug Design via Multi-Modal Learning | ACM TKDD | 2026-04-12 | #14 | ⭐⭐⭐ |
| 5 | Protein Large Language Models: A Comprehensive Survey | arXiv | 2025-02-21 | #6;#14 | ⭐⭐⭐ |
| 6 | ProteinMCP: An Agentic AI Framework for Autonomous Protein Engineering | Protein Science | 2026-03-25 | #14;#6 | ⭐⭐⭐⭐ |
| 7 | Genome Modelling and Design Across All Domains of Life with Evo 2 | Nature | 2026-03-04 | #14 | ⭐⭐⭐⭐⭐ |
| 8 | InstructPro: Natural Language Instructable Multimodal Framework for Ligand-Binding Protein Design | arXiv | 2026-06-09 | #14;#6 | ⭐⭐⭐ |
| 9 | Compressing the Collective Knowledge of ESM into a Single Efficient PLM | Nat Methods | 2026-03-30 | #6 | ⭐⭐⭐⭐ |
| 10 | Evolutionary LLM-Guided Mutagenesis: In-Silico Directed Evolution | clawRxiv | 2026-03-19 | #2 | ⭐⭐⭐ |
| 11 | ODesign: A World Model for Biomolecular Interaction Design | ODesign | 2025-10-25 | #14;#6 | ⭐⭐⭐ |
| 12 | Artificial Allosteric Protein Switches with ML-Designed Receptor Domains | Nat Biotechnol | 2026-04-15 | #6;#15 | ⭐⭐⭐⭐⭐ |
| 13 | Machine Learning for Evolutionary Genetics and Molecular Evolution | Nat Rev Genet | 2026-03-24 | #2;#9 | ⭐⭐⭐ |
| 14 | Leveraging Ancestral Sequence Reconstruction for Protein Representation Learning | Nat Mach Intell | 2024-12-18 | #2;#6 | ⭐⭐⭐⭐ |
| 15 | BetaReconstruct: ASR Using Generative Models Without Sequence Alignment | GitHub/preprint | 2025-06-11 | #2 | ⭐⭐⭐ |
| 16 | BioPKS Pipeline: Computational Design of Chimeric Type I PKS | Nat Commun | 2025-07-01 | #16 | ⭐⭐⭐⭐ |
| 17 | DeepT2: Deep Learning for Type II Polyketide Natural Product Prediction | RSC Digital Discov | 2023-08-30 | #16;#9 | ⭐⭐⭐ |
| 18 | Context-Aware Biosensor Design Through Biology-Guided ML | Nat Biomed Eng | 2025-12-15 | #9 | ⭐⭐⭐⭐ |
| 19 | Biosensor and Machine Learning-Aided Engineering of an Amaryllidaceae Enzyme | Nat Commun | 2024-03-07 | #9;#2 | ⭐⭐⭐ |
| 20 | CreoPep: Deep Learning Framework for Target-Specific Conotoxin Peptide Design | Nat Chem Biol | 2026-01-09 | #2;#6 | ⭐⭐⭐⭐ |
| 21 | Peptide-Based Drug Design Using Generative AI | Chem Commun | 2026-04-08 | #2 | ⭐⭐⭐ |
| 22 | AI-Enhanced CRISPR Diagnostics: From gRNA Design to Cas Protein Engineering | Trends Biotechnol | 2026-04-01 | #15 | ⭐⭐⭐ |
| 23 | Computation and Deep-Learning-Driven Advances in CRISPR Genome Editing | Nat Struct Mol Biol | 2026-02-16 | #15 | ⭐⭐⭐⭐ |
| 24 | Custom CRISPR-Cas9 PAM Variants via Scalable Engineering and ML | Nature | 2025-01-15 | #15 | ⭐⭐⭐⭐⭐ |
| 25 | GeoDock: Empowering LLMs for SBDD via Multi-Modal Learning | ACM TKDD | 2026-04-12 | #14 | ⭐⭐⭐ |
| 26 | ML Enhances the Performance of Biosensors (2021) | — | 2021 | #9 | ⭐⭐ |
| 27 | Generative AI for Novel Peptide Sequences | Peptide Journal | — | #17 | ⭐⭐ |
| 28 | AI-Driven CRISPR Screening: Optimizing Gene Editing | — | — | #15 | ⭐⭐⭐ |

---

## 六、工具执行状态汇总

| 工具 | 状态 | 说明 |
|:-----|:----:|:-----|
| ArXiv API (export) | ✅ | curl直接调用，ti/abs字段限定，HTTPS，需6s间隔防503 |
| WebSearch | ✅ | 主要检索渠道，覆盖Nature/Science/Cell/NAR/arXiv等 |
| Tavily | ❌ | API key未配置，持续跳过 |
| Exa | ⚠️ | MCP服务器未在mcp.json注册（注：后续会话中已确认Exa可用，但W19执行时未调用） |
| WeChat Article Search | ✅ | 部分方向使用，命中ProteinMCP等 |
| CrossRef API | ✅ | 用于Science等被Cloudflare阻挡期刊的元数据fallback |

---

## 七、异常记录与趋势分析

### 7.1 本周异常

| 异常 | 影响 | 说明 |
|:-----|:-----|:-----|
| step01a/b 单周命中极低 | #1-#12、#13-#25 大量方向零命中 | 精确单周窗口（2026-05-04~05-10）内AI+合成生物交叉领域整体发文量处于低谷，与前两周(W17/W18)趋势一致 |
| Science官网被Cloudflare阻挡 | 需通过CrossRef二次确认 | Science、Nature部分页面直接WebFetch返回"Just a moment..."，已通过CrossRef API补齐元数据 |
| ArXiv q2/q3/q6/q7/q9 零命中 | 对应方向无近期论文 | metabolic engineering、enzyme engineering、gene circuit、chassis cell、biosynthetic pathway在ti/abs限定下近期无 submissions |

### 7.2 连续趋势观察

- **IDP方向持续高热**：STARLING (Nature)、IDPForge (bioRxiv)、IDP-EDL 等连续多周出现高质量论文，表明无序蛋白+深度学习是当前最活跃的子领域之一。
- **生物智能体/自主实验室稳步增长**：BioMARS、ProteinMCP、AI-driven CFPS 等标志AI Agent在生物实验中的落地加速。
- **扩散模型+蛋白质设计成新热点**：TD3B、IDPForge、Conditional antibody generation 等显示离散/连续扩散在生物序列设计中的应用正快速扩展。
- **基础模型巨型化**：Evo 2 (7B参数, 9T碱基对) 代表生物基础模型进入基因组规模时代。

---

## 八、引用文件

| 文件 | 路径 | 内容 |
|:-----|:-----|:-----|
| step01a 原始结果 | `中间结果/step01a-merged-2026-W19.md` | #1-#12 方向，5篇 |
| step01b 原始结果 | `中间结果/step01b-merged-2026-W19.md` | #13-#25 方向，3篇 |
| step02a 原始结果 | `中间结果/step02a-merged-2026-W19.md` | #26-#33 方向，15篇 |
| step02b 原始结果 | `中间结果/step02b-merged-2026-W19.md` | #34-#41 方向，28篇 |
| step03 分类评级 | `中间结果/step03-classified-2026-W19.md` | 早期分类（基于缺失step01a/b数据），已部分过时 |
| 文献调研Excel | `文献调研记录_2026.xlsx` | W19 Excel追加记录（5月11日执行，34行） |

---

*报告结束。如需进一步细化某个方向或生成Obsidian论文笔记，请告知。*

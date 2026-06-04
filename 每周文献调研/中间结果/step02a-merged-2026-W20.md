# 检索结果：IDP+生物智能体

**ISO周编号**：2026-W20
**时间窗口**：2026-05-12 至 2026-05-18
**工具执行状态**：ArXiv ❌（持续触发速率限制，未调用）| WebSearch ✅ | Tavily ❌（未配置）| Exa ❌（MCP服务器未配置）
**关键词覆盖**：#26-#33，共8组
**原始命中**：约8条
**去重后**：3条
**⚠️ 重要标注**：W20为IDP+生物智能体+cell-free交叉领域发文低谷，多个方向零命中

---

## 检索D方向：IDP与相分离（关键词#26-29）

### 各关键词命中情况

| 关键词编号 | 检索词 | 命中状态 | 备注 |
|---|---|---|---|
| #26 | ("intrinsically disordered protein" OR "IDP") AND ("machine learning" OR "deep learning" OR "prediction") | ✅ 1篇 | ENSEMBITS（arXiv 2605.13789，2026-05-13） |
| #27 | ("prion-like" OR "prion domain") AND ("machine learning" OR "deep learning" OR "prediction") | ❌ 零命中 | 本窗口期无新发表 |
| #28 | ("liquid-liquid phase separation" OR "LLPS" OR "biomolecular condensate") AND ("machine learning" OR "deep learning" OR "prediction") | ✅ 1篇 | LLPS-RCD综述（Cell Death Discovery，2026-05-12） |
| #29 | ("intrinsically disordered region" OR "IDR") AND ("prediction" OR "deep learning") | ✅ 2篇 | ENSEMBITS + Frequency-Space Mechanics |

**IDP方向合计**：3篇

---

## 检索E方向：生物智能体与Cell-free（关键词#30-33）

### 各关键词命中情况

| 关键词编号 | 检索词 | 命中状态 | 备注 |
|---|---|---|---|
| #30 | ("synthetic biology agent" OR ("biological agent" AND "synthetic biology")) AND ("AI" OR "machine learning") | ❌ 零命中 | 本窗口期无新发表 |
| #31 | "cell-free" AND ("synthetic biology" OR "protein synthesis") AND ("machine learning" OR "AI") | ❌ 零命中 | GPT-5 autonomous lab CFPS（2026-02-05）超出窗口 |
| #32 | ("xenobot" OR "living robot" OR "biobot") AND ("design" OR "machine learning") | ❌ 零命中 | Neurobot（Advanced Science，2026-02-20）超出窗口 |
| #33 | ("cell-free system" OR "CFPS") AND ("optimization" OR "machine learning" OR "deep learning") | ❌ 零命中 | 本窗口期无新发表 |

**生物智能体/Cell-free方向合计**：0篇

---

## 合并去重结果

| # | 标题 | 作者 | 期刊 | 发表日期 | DOI | 发表状态 | 摘要 | 论文关键词 | 核心发现 | 检索来源 | 关键词编号 |
|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | ENSEMBITS: an alphabet of protein conformational ensembles | Shi, K.; Oliver, C. | arXiv | 2026-05-13 | 10.48550/arXiv.2605.13789 | 预印本 | Protein structure tokenizers (PSTs) are workhorses in protein language modeling, function prediction, and evolutionary analysis. However, existing PSTs only capture local geometry of static structures, and miss the correlated motions and alternative conformational states revealed by protein ensembles. Here we introduce Ensembits, the first tokenizer of protein conformational ensembles. Ensembits address challenges inherent to tokenizing dynamics: deriving informative geometric descriptors across conformations, permutation-invariance encoding of variable-size ensembles, and conquering sparsity in dynamics data. Trained with a Residual VQ-VAE using a frame distillation objective on a large molecular dynamics corpus, Ensembits outperforms all related methods on RMSF prediction, and is the strongest standalone structural tokenizer on an token-conditioned ANOVA test on per-residue motion amplitude. Ensembits further matches or exceeds static tokenizers on EC, GO, binding site/affinity prediction, and zero-shot mutation-effect prediction despite using far less pretraining data. Notably, the distillation objective enables Ensembits to predict dynamics token from one single predicted structure, which alleviates dynamics data sparsity. As the field moves from static structure prediction toward ensemble generation, Ensembits offer the discrete vocabulary needed to bring dynamics into protein language modeling and design. | Protein tokenizer; conformational ensemble; protein language model; dynamics; VQ-VAE; molecular dynamics; RMSF prediction | 该研究提出了Ensembits，首个针对蛋白构象集合的tokenizer，通过残差VQ-VAE结合帧蒸馏目标进行训练，解决了构象集合大小可变、置换不变性等tokenization难题，在RMSF预测上超越所有现有方法，并在功能预测、结合位点/亲和力预测和零样本突变效应预测上匹配或超越静态tokenizer。 | WebSearch | #26,#29 |
| 2 | Frequency-Space Mechanics: A Sequence and Coordinate-Free Representation for Protein Function Prediction | Reilly, C. B. | arXiv | 2026-05-12 | 10.48550/arXiv.2605.13899 | 预印本 | Protein function prediction is dominated by representations grounded in sequence and static structure, neither of which captures the collective vibrational dynamics through which proteins act. Here we introduce frequency-space mechanics, a representational framework in which a protein is encoded as a mechanical harmonics graph (MHG): nodes are vibrational modes derived from molecular dynamics, and edges are harmonic couplings weighted by octave alignment between mode frequencies. Key characteristics include: coordinate-free, sequence-independent, scale-invariant. Trained on 5,238 SwissProt proteins under strict 30% sequence-identity split using no sequence information, a graph neural network over static MHGs predicts GO molecular function terms across the ontology, demonstrating that vibrational physics alone encodes broad functional class. Kuramoto entrainment of the harmonic coupling graph improves prediction for proteins whose function depends on collective conformational dynamics. On CLIC1 (a fold- and function-switching chloride channel excluded from training), entrainment amplified channel-activity signal 7.5-fold and antioxidant signal 2.4-fold, recovering both functional states from dynamics alone. | Protein function prediction; vibrational dynamics; graph neural network; mechanical harmonics; Kuramoto entrainment; molecular dynamics; coordinate-free representation | 该研究提出了频率空间力学（frequency-space mechanics）框架，用振动模式和耦合权重构建无坐标、无序列依赖的蛋白表示图，在5,238个SwissProt蛋白上仅凭振动物理信息即可预测GO分子功能术语，在CLIC1蛋白上Kuramoto同步方法将通道活性信号放大7.5倍，证明了振动动力学可编码蛋白功能。 | WebSearch | #29 |
| 3 | Liquid-liquid phase separation-driven regulated cell death: from molecular mechanisms to therapeutic strategies | Li, B.; Lan, Z.; Cui, H.; Liu, W.; Tian, Z.; Lian, J.; Zhao, Y.; Yu, G. | Cell Death Discovery | 2026-05-12 | 10.1038/s41420-026-03150-7 | 已发表 | Regulated cell death (RCD) is a tightly controlled biological process essential for development, tissue homeostasis, and host defense. Despite extensive investigation, how these signaling pathways are spatially and temporally organized to ensure precise cell death decisions remains incompletely understood. Liquid-liquid phase separation (LLPS), a biophysical mechanism driving the formation of dynamic biomolecular condensates, has emerged as a fundamental principle for cellular organization, signal integration, and stress adaptation. Increasing evidence indicates that LLPS plays a critical role in orchestrating cell fate decisions; however, its involvement in RCD has not yet been systematically defined. In this review, we provide a comprehensive overview of LLPS in the context of RCD. We summarize the physicochemical principles, molecular determinants, and regulatory factors governing LLPS, as well as the functional properties of phase-separated condensates, and then discuss how LLPS modulates key RCD pathways, including apoptosis, necroptosis, autophagy-dependent cell death, pyroptosis, and ferroptosis, highlighting shared and pathway-specific regulatory mechanisms. Furthermore, we examine the pathological consequences of aberrant phase separation-mediated RCD in human diseases and discuss emerging therapeutic strategies aimed at targeting LLPS-driven cell death processes. Finally, we catalog RCD-associated proteins with phase separation potential and outline major conceptual and technical challenges, proposing future directions for this rapidly evolving field. | Liquid-liquid phase separation; regulated cell death; biomolecular condensate; apoptosis; necroptosis; pyroptosis; ferroptosis; autophagy-dependent cell death | 该综述系统概述了LLPS在RCD中的作用，总结了LLPS的物理化学原理和调控因子，讨论了LLPS如何调控凋亡、坏死性凋亡、自噬依赖性细胞死亡、细胞焦亡和铁死亡等关键RCD通路，并梳理了异常相分离介导的RCD在人类疾病中的病理后果及新兴治疗策略。 | WebSearch | #28,#29 |

---

## 方向分布

| 方向 | 篇数 |
|---|---|
| IDP（#26-#29） | 3 |
| 生物智能体（#30-#33） | 0 |
| **合计** | **3** |

---

## 重要说明

- **W20为发文低谷**：#27（prion-like）、#30-#33（生物智能体/cell-free/xenobot）等5个关键词方向零命中
- **ArXiv本周持续限流**：本次未通过API批量检索，改为WebSearch渠道
- **Exa MCP未配置**：未能使用语义搜索补充覆盖率
- **跨文件周编号一致性**：待step02b完成后校验

---

*生成时间：2026-05-21*
*执行时间窗口：2026-05-12 至 2026-05-18（ISO W20）*
*工具版本：minimax-m2.7*

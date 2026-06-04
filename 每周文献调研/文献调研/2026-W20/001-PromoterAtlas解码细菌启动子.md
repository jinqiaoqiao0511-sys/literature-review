---
uid: 2026-W20-001
title: PromoterAtlas: decoding regulatory sequences across Gammaproteobacteria using a transformer model
authors: Coppens, L.; Ledesma-Amaro, R.
journal: Nat Commun
published: 2026-05-15
doi: 10.1038/s41467-026-72837-3
tags: [启动子预测, 转录调控, Transformer, 细菌合成生物学, 核心方向#10]
stars: ⭐⭐⭐⭐⭐
date: 2026-05-15
---

# 核心发现

该研究开发PromoterAtlas，一个基于1.8M参数Transformer模型的跨物种细菌启动子预测与注释工具，在3371种γ-变形菌的900万条调控序列上训练，可识别启动子、RBS、TFBS等多种调控元件；模型嵌入向量还能编码转录翻译水平信息并反映跨物种进化关系。

# 摘要

Recent advances in deep learning, particularly transformer architectures, have improved computational approaches for biological sequence analysis. Despite these advances, computational models for bacterial promoter prediction have remained limited by small datasets, species-specific training, and binary classification approaches rather than comprehensive annotation frameworks. We present PromoterAtlas, a 1.8 M parameter transformer model trained on 9 M regulatory sequences from 3371 gammaproteobacterial species. The model demonstrates recognition of various regulatory elements across different species, including ribosomal binding sites, various types of bacterial promoters, transcription factor binding sites, and terminators. Using this model, we developed a whole-genome promoter annotation tool for Gammaproteobacteria, with various levels of validation that support the predictions of promoters associated with different sigma (σ) factors. Furthermore, we show that the model embeddings reflect cross-species evolutionary relationships, clustering promoters by σ factor identity rather than species-specific sequence features. Finally, we show that model embeddings encode regulatory sequence information that enables effective prediction of transcription and translation levels. PromoterAtlas can contribute to our understanding of and ability to engineer bacterial regulatory sequences with potential applications in bacterial biology, synthetic biology, and comparative genomics.

# 关键词

bacterial genomics; gene expression; gene regulation; machine learning; sequence annotation; Gammaproteobacteria; transformer; promoter prediction; sigma factor; transcription factor binding site; ribosome binding site; synthetic biology

# 检索来源

WebSearch

# 研究方向

核心方向 #10 - 启动子元件 & Ⅲ型启动子挖掘

# 期刊信息

- 期刊: Nature Communications
- 影响因子: 15.7
- JCR分区: Q1
- 发表日期: 2026-05-15

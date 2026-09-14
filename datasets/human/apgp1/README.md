# Asian Pan-Genome Project Phase 1（APGp1）

[返回首页](../../../README.md) · [人类数据目录](../README.md) · [所属分类：人类](../../../catalog/real/human.md)

## 简介

Asian Pan-Genome Project Phase 1 面向东亚人群构建的群体组装和泛基因组资源。项目报告生成 160 个个体的 320 个 de novo near-T2T 单倍型组装，并提供 Minigraph-Cactus、Minigraph 以及跨 APGp1/HPRC/HGSVC 的组合图。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | Asian Pan-Genome project phase 1，APGp1 |
| 发布者 | Asian-Pan-Genome collaboration |
| 数据性质 | 东亚人群二倍体、单倍型分相组装和泛基因组图 |
| 当前规模 | 160 个个体、320 个 haplotype assemblies |
| assembly BioProject | PRJCA030428 |
| 原始测序数据 | HRA010014 |
| 仓库组装级别 | 项目称 near-T2T；本仓库不归为 T2T |
| 公开状态 | assemblies/raw reads 为 controlled access；部分图和注释提供公开下载入口 |

## 适用研究

- 东亚人群内 MGA、单倍型组装比较和泛基因组构建。
- 直接使用 320-haplotype APGp1 图，或使用与 HPRC Year 1/HGSVC3 合并的 540-haplotype 图。
- 复杂区域、结构变异、centromere、rDNA、MHC/SMN 和 annotation 研究。

## 组装级别

项目使用 **near-T2T** 描述 320 个组装。near-T2T 与 T2T 不等价，本仓库不把这些组装计入 T2T；需要逐条提供版本、未解决区域和明确 T2T 证据后才能重新分类。

## 下载与访问入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 项目主页与资源总表 | Phase 1 | 文档、metadata、资源链接 | [Asian-Pan-Genome/APGp1](https://github.com/Asian-Pan-Genome/APGp1) | 公开 |
| 样本 metadata | 160 individuals | CSV | [APGp1_metadata.csv](https://github.com/Asian-Pan-Genome/APGp1/blob/main/APGp1_metadata.csv) | 公开去标识信息 |
| Assemblies | 320 haplotypes | FASTA | [PRJCA030428](https://ngdc.cncb.ac.cn/bioproject/browse/PRJCA030428) | controlled access；需向 APG DAC 申请 |
| Raw reads | Phase 1 | HRA data | [HRA010014](https://ngdc.cncb.ac.cn/gsa-human/browse/HRA010014) | controlled access；需申请；本次直接访问超时 |
| Pangenome graphs | APGp1 及组合图 | GFA/图配套文件 | [图资源入口](https://genome.zju.edu.cn/APG) | 公开页面；逐文件条件以站点为准 |
| 分析与注释仓库 | Phase 1 | scripts、BED、GFF 等 | [GitHub 仓库](https://github.com/Asian-Pan-Genome/APGp1) | 公开 |

## 图资源范围

项目资源表提供 320-haplotype APGp1 的 Minigraph-Cactus 图（T2T-CN1 和 T2T-CHM13 reference）、Minigraph 图，以及 APGp1 + HPRCy1 + HGSVC3 的 540-haplotype 组合图。不同方法、reference 和 haplotype 集合不能视为同一图版本；使用时记录 method、software version、reference 和 sample set。

## 真值与限制

APGp1 提供丰富的 assembly、graph、SV 和 annotation 资源，但没有一个适用于所有 MGA 或 graph evaluation 的统一真值。公开图不意味着受控 assembly 和 reads 可以匿名下载；申请条件必须按 NGDC/APG 当前政策执行。

项目旗舰研究在官方仓库中仍标为 unpublished，因此当前条目以项目资源说明为主要依据，后续论文发布后应补充正式引用和固定版本。

## 引用与核验

- GitHub 项目、metadata 和 BioProject 于 2026-09-14 检查可访问；HRA010014 由项目官方 README 明确列出，但本次直接访问超时。图资源使用官方项目给出的入口，未逐文件测试。
- 访问条件来自项目官方 README；受控数据需遵守参与者同意和 Data Access Committee 要求。

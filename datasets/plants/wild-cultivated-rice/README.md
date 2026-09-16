# 野生—栽培水稻泛基因组

[返回首页](../../../README.md) · [植物数据目录](../README.md) · [所属分类：植物](../../../catalog/real/plants.md)

## 简介

本条目收录 Nature 2025 论文 A pangenome reference of wild and cultivated rice 对应的固定发布集。完整组装归档、基因泛基因组与图泛基因组的规模分别记录。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 发布者与版本 | Guo、Li、Lu 等；论文 2025-04-16；Figshare v1 |
| 集合标识 | 10.25452/figshare.plus.25697817.v1；PRJEB73710、PRJCA024131 |
| 物种与比较范围 | *Oryza sativa*、*O. rufipogon*，另有 *O. longistaminata*、*O. meridionalis* 外群；种内与种间 |
| 数据性质 | 真实组装、基因及碱基层面泛基因组 |
| 测序与组装规模 | 149 份材料：133 份 HiFi、16 份 ONT；归档提供 149 份原始 contig 和染色体级组装 |
| 基因泛基因组 | 145 份：129 份普通野生稻 + 16 份栽培稻；其余 4 份为外群 |
| 图泛基因组 | 联合图 144 份：129 份野生稻 + 15 份栽培稻；另提供野生、栽培各自的图 |
| 格式与覆盖范围 | 全基因组序列、注释、VCF、基因与图泛基因组压缩归档；包内格式未解包核验 |
| 数据体积 | 染色体包 18,044,960,816 bytes；图包 21,815,908,181 bytes，来自官方 API |

## 适用研究

| 用途 | 依据类型 | 使用方式 |
| --- | --- | --- |
| Pangenome | 原研究 | 野生—栽培比较、基因存在缺失和图结构变异分析 |
| MGA | 潜在用途 | 从固定发布选择种内/种间组装；保留外群及测序平台标签 |

## 组装与质量

- **仓库组装级别**：Chromosome 149（选择 chromosome_level 包时）；原始 contig、Hi-C 包是同批材料的不同表示，不重复计数。
- **来源原始级别**：归档 README 明确 chromosome-level 149、Hi-C 30；未逐数据库 accession 核查。
- **构建差异**：30 份有 Hi-C 支持，其余染色体锚定使用共线性方法；结构重排评测需保留此差异。
- **质量信息**：论文报告 ONT 和 HiFi 组装平均 QV 分别为 24.55 和 57.92。
- **T2T 证据与限制**：本集不归为 T2T；多数组装缺少第 9 号染色体短臂端粒。参考 T2T-NIP 不等同于本研究的 Nipponbare 重组装。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 完整发布 | Figshare v1，18 个文件 | 文件清单 | [固定版本](https://doi.org/10.25452/figshare.plus.25697817.v1) | 公开，CC BY 4.0 |
| 文件解释 | 各包范围 | TXT | [README](https://ndownloader.figshare.com/files/49715187) | 公开 |
| 原始 contig | 149 份 | TAR.GZ | [raw_assembly_contig](https://ndownloader.figshare.com/files/47002003) | 公开 |
| 染色体级组装 | 149 份 | TAR.GZ | [chromosome_level](https://ndownloader.figshare.com/files/46868638) | 公开 |
| Hi-C 组装 | 30 份 | TAR.GZ | [hic_assembly](https://ndownloader.figshare.com/files/49689012) | 公开 |
| 染色体级注释 | 149 份 | TAR.GZ | [chromosome_level_annotation](https://ndownloader.figshare.com/files/46667536) | 公开 |
| 图泛基因组 | 三个构图结果 | TAR.GZ | [graph_pan](https://ndownloader.figshare.com/files/46884886) | 公开 |
| 基因泛基因组 | 三个分析结果 | TAR.GZ | [gene_pan](https://ndownloader.figshare.com/files/45875037) | 公开 |
| 变异、TE、功能注释 | 各方法对应包 | VCF 等压缩归档 | [Figshare 文件清单](https://doi.org/10.25452/figshare.plus.25697817.v1) | 公开 |
| 原始测序 | PRJEB73710 | 测序记录 | [ENA](https://www.ebi.ac.uk/ena/browser/view/PRJEB73710) | 论文提供；本次未逐文件核验 |
| 分析流程 | 论文关联项目 | 代码 | [官方 GitHub](https://github.com/dongling-hub/Wild-rice-Pangenome-Project) | 论文提供；代码许可另查 |

## 配套资源

归档含基因、TE、功能注释，多个方法的变异包及基因/图泛基因组。样本对应关系见论文补充表。功能注释为两个分卷，按官方 README 处理。

- **真值状态**：未明确；未确认统一 MGA 真值。
- **评测限制**：SyRI、SVIM-asm、cuteSV、pbsv、longshot 等结果属于方法产物，不能直接合并作为真值。

## 使用注意

明确 149/145/144 三个范围。alternate contigs 不代表额外独立材料，也不等于完整二倍体分相组装；30 份 Hi-C 包不能再加到总数中。图、注释及序列固定到同一归档版本。

## 引用与核验

- **论文**：Guo, D., Li, Y., Lu, H. et al. [A pangenome reference of wild and cultivated rice](https://doi.org/10.1038/s41586-025-08883-6). Nature 642, 662–671 (2025).
- **数据引用与许可**：Figshare v1 DOI；该归档元数据为 CC BY 4.0，其他入口按自身条款。

| 检查对象 | 检查日期 | 入口核验结果 | 说明 |
| --- | --- | --- | --- |
| Nature 论文 | 2026-09-16 | 可读取 | 核对分析范围和质量 |
| Figshare API、README | 2026-09-16 | HTTP 200 | 核对 18 个文件、文件 ID、体积、版本、许可 |
| 数据包链接 | 2026-09-16 | 官方 API 列出 | 未请求包内容，不等于完整性验证 |

**尚未核实的信息**：包内图格式、逐材料 accession、逐条组装缺失区域。

**文件内容验证**：未验证（未下载）。

## 更新记录

- 2026-09-16：首次收录论文发布集与官方资源入口；仅核验网页和元数据。

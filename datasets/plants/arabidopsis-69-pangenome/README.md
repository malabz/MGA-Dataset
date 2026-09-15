# 69 个拟南芥品系泛基因组

[返回首页](../../../README.md) · [数据目录](../../../catalog/README.md) · [植物分类](../../../catalog/real/plants.md) · [植物数据集](../README.md)

所属目录：[植物基因组资源](../../../catalog/real/plants.md)。

## 简介

该固定研究集合对应论文 *A pan-genome of 69 Arabidopsis thaliana accessions reveals a conserved genome structure throughout the global species range*。研究团队从全球分布范围选择 72 个拟南芥品系，生成长读长和短读长数据；其中 69 个确认的自交系进入主要比较和泛基因组分析，Lu-1、Pa-1 和 Istisu-1 因显示杂合性而退出后续分析。

核心资源包括 69 个染色体级基因组组装、基因与转座元件注释、SNP、结构变异、泛基因组矩阵和 orthogroups。论文进行了以 Col-PEK 为参照的成对全基因组比对和 69 个品系的综合比较，但没有提供可以作为通用多基因组比对真值的碱基对应关系。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | A pan-genome of 69 Arabidopsis thaliana accessions reveals a conserved genome structure throughout the global species range |
| 维护方式 | 固定研究集合；数据仓库记录允许版本更新 |
| 发布机构或项目 | Max Planck Institute for Plant Breeding Research、Max Planck Genome Centre Cologne、INRAE 等论文作者机构 |
| 版本或发布日期 | 论文 Version of Record：2024-04-11；Edmond 当前元数据版本：V3.0，更新于 2026-07-09 |
| 集合标识 / accession | NCBI BioProject：`PRJNA1033522`；ENA：`PRJEB62038`（`ERP147129`）；Edmond DOI：`10.17617/3.AEOJBL` |
| 物种与学名 | 拟南芥，*Arabidopsis thaliana* |
| 比较范围 | 种内；品系来自欧洲、亚洲、非洲、马德拉和北美等全球分布区域 |
| 数据性质 | 真实长读长组装，以及派生的注释、变异和基因泛基因组资源 |
| 规模与计数单位 | 72 个测序品系；69 个进入主要分析的自交品系和 69 个染色体级组装；48 个品系使用 PacBio HiFi、24 个使用 Oxford Nanopore |
| 格式与覆盖范围 | NCBI 提供组装序列及标准批量下载；ENA 提供原始读段；Edmond V3.0 元数据记录 7 个 gzip 文件，内容覆盖组装、注释、变异和泛基因组结果 |
| 数据体积 | Edmond V3.0 的 7 个文件合计 4,555,362,574 bytes，约 4.56 GB；NCBI 组装和 ENA 原始读段体积未在本仓库计算 |
| 原始集合或派生关系 | 72 个品系经过组装和质量评估后，3 个显示杂合性的品系未进入主要分析；NCBI BioProject 收录核心 69 个组装，Edmond 还包含 Lu-1、Pa-1 和 Istisu-1 的组装资源 |

## 样本与分析范围

| 阶段 | 数量与单位 | 说明 |
| --- | --- | --- |
| 初始选择与测序 | 72 个品系 | 48 个使用 PacBio HiFi，平均深度 45×；24 个使用 Oxford Nanopore，平均深度 67×；均配有短读长数据 |
| 核心组装集合 | 69 个品系、69 个组装 | 确认为自交系，进入后续组装比较、结构变异和泛基因组分析 |
| 未进入主要分析 | 3 个品系 | Lu-1、Pa-1 和 Istisu-1 显示杂合性；其组装仍由 Edmond 提供 |
| 最完整子集 | 46 个组装 | 依据组装与 k-mer 基因组大小估计之比、着丝粒重复组装与读段估计之比选出；不代表 46 个 T2T 组装 |
| NCBI 当前记录 | 69 个组装 | `PRJNA1033522` 下 69 个 assembly accession，NCBI 均登记为 Chromosome |

“72”表示初始测序和组装的品系数，“69”表示论文主要分析及 NCBI BioProject 中的核心染色体级组装数，“46”是用于部分基因组大小分析的最完整子集。这三个数字不能互换。

## 适用研究

| 用途 | 依据类型 | 使用方式、来源或判断理由 |
| --- | --- | --- |
| Pangenome | 原研究 | 对 69 个拟南芥组装进行基因家族分析，发布泛基因组矩阵和 orthogroups；论文报告 32,986 个至少出现在一个核心品系中的基因家族 |
| 结构变异与共线性 | 原研究 | 使用 minimap2 将 69 个组装分别与 Col-PEK 比对，并用 SyRI 和 SURVIVOR 检测与合并结构变异，分析染色体臂和着丝粒区域的结构动态 |
| 群体与系统发育 | 原研究 | 提供 SNP、基因 presence–absence 信息和单拷贝 orthogroups，用于群体结构、共线性与系统发育分析 |
| MGA | 潜在用途 | 69 个同物种染色体级组装适合评估种内多基因组比对的规模、结构变异保留和共线性结果；原研究没有定义通用 MGA 评测真值 |

## 组装与质量

- **仓库组装级别**：69 个核心组装均为 Chromosome；未归为 T2T。
- **来源原始级别**：NCBI `PRJNA1033522` 当前关联 69 个组装，assembly level 均为 Chromosome。论文也称其为 chromosome-level assemblies。
- **T2T 证据**：未发现论文或 NCBI 针对这 69 个具体组装版本给出完整端粒到端粒证据。论文将它们的质量与 Col-0 参考和 T2T 组装比较，并提到着丝粒和端粒重复评估，但这些表述不能把集合判定为 T2T。
- **判定对象与范围**：仓库级别适用于 `PRJNA1033522` 当前列出的 69 个核心组装；Edmond 中额外三个杂合品系组装没有计入该汇总。
- **组装流程**：HiFi 数据分别使用 Canu、Flye 和 Hifiasm 组装并合并；ONT 数据使用 SMARTdenovo 和 Flye。流程使用 RaGOO 基于 Col-CEN 的全基因组比对进行参考辅助排序和定向，再经人工检查、纠错、补洞和 polishing。
- **连续性与大小**：69 个 contig assemblies 的 N50 为 6.1–21.3 Mb，平均 13.3 Mb；染色体级组装大小为 128–148 Mb，平均 135 Mb。
- **已公布质量信息**：平均 BUSCO/compleasm 完整度 99.8%；基于 k-mer 的平均 QV 为 53.4、平均完整度为 98.5%；参考蛋白编码基因的平均完整组装比例为 97.3%（同源搜索）和 98.4%（Liftoff）；平均 LAI 为 22；估计的着丝粒重复平均完整度为 96%。
- **已知缺失或范围限制**：部分 ONT 组装短于 k-mer 估计的基因组大小，论文认为其 rDNA arrays 和 centromeres 没有完全组装；23 个组装未进入最完整的 46 个组装子集。参考辅助 scaffolding 也需要在研究大尺度重排时纳入方法学考虑。

## 下载入口

### 基因组组装与研究数据

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| NCBI BioProject | 核心 69 个染色体级组装；`PRJNA1033522` | BioProject、Assembly records | [项目主页](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA1033522) | 公开 |
| NCBI Assembly 集合 | `PRJNA1033522` 下的 assembly accession 列表和批量入口 | FASTA 及 NCBI 标准配套文件 | [Assembly 检索结果](https://www.ncbi.nlm.nih.gov/assembly/?term=PRJNA1033522%5BBioProject%5D) | 公开 |
| Edmond 研究数据 | DOI 固定集合；当前元数据 V3.0；包括 69 个核心组装及 Lu-1、Pa-1、Istisu-1 | 7 个 gzip 文件；内部格式按数据记录说明 | [`10.17617/3.AEOJBL`](https://doi.org/10.17617/3.AEOJBL) | 公开；CC0 1.0 |
| ENA 原始测序项目 | 72 个品系的 PacBio HiFi、ONT 和 Illumina 数据；`PRJEB62038` / `ERP147129` | FASTQ、ENA run records | [项目主页](https://www.ebi.ac.uk/ena/browser/view/PRJEB62038) | 公开 |

### 论文、代码与补充材料

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 论文主页 | Version of Record | HTML、补充材料 | [Nature Genetics](https://www.nature.com/articles/s41588-024-01715-9) | 公开文章；CC BY 4.0，第三方材料以页面说明为准 |
| 开放全文 | PMCID `PMC11096106` | HTML、XML、补充材料 | [PubMed Central](https://pmc.ncbi.nlm.nih.gov/articles/PMC11096106/) | 公开 |
| 分析代码 | 当前可浏览仓库 | GitHub | [`qclian/Pan_Ath`](https://github.com/qclian/Pan_Ath) | 公开；仓库页面未提供独立许可证文件 |
| 代码归档 | v1.0；论文发布版本 | ZIP | [Zenodo `10.5281/zenodo.10567419`](https://doi.org/10.5281/zenodo.10567419) | 公开；CC BY 4.0 |
| 补充表与 Source Data | 与论文 Version of Record 对应 | XLSX、PDF | [PMC 论文及关联数据](https://pmc.ncbi.nlm.nih.gov/articles/PMC11096106/) | 公开；具体文件条款随论文页面 |

## 配套资源

| 资源 | 提供情况 | 内容、版本对应与下载表中的资源名称 |
| --- | --- | --- |
| 样本清单 | 已提供 | 论文 Supplementary Table 1 记录 72 个品系；NCBI 和 ENA 分别提供 assembly、BioSample 与 run 对应关系 |
| 基因与 TE 注释 | 已提供 | Edmond 研究数据包含 gene and TE annotations |
| SNP 与结构变异 | 已提供 | Edmond 研究数据包含 SNPs and SVs；论文说明了基于 Col-PEK 的检测流程 |
| 泛基因组矩阵与 orthogroups | 已提供 | Edmond 研究数据包含 pan-genome matrix and orthogroups |
| 泛基因组图 | 未明确 | 论文和数据可用性声明没有明确列出可下载的图泛基因组文件 |
| 已有比对结果 | 部分提供 | 论文提供成对全基因组比对派生的共线性与 SV 结果；尚未确认是否发布完整原始 alignment 文件 |
| 真值 | 无统一 MGA 真值 | 已有组装间比对、共线性和 SV 结果均是分析产物，不能自动作为碱基级同源关系真值 |

- **真值状态**：无统一多基因组比对真值。
- **真值类型、来源与覆盖**：论文对部分大倒位使用长读段比对支持，但没有发布覆盖全部 69 个组装的已知同源关系真值；这类局部支持也不能推广为全基因组 MGA 真值。
- **可评测对象与限制**：适合比较运行规模、资源消耗、共线性结构和不同方法结果的一致性。需要精确率、召回率或 F1 时，应另行确定与评测任务匹配的可靠真值。

## 使用注意

- **72 与 69 的范围**：ENA 原始测序项目覆盖 72 个品系；论文核心分析和 NCBI BioProject 组装集合为 69 个品系。不要把 72 个原始测序样本报告成 72 个核心染色体级组装。
- **三个杂合品系**：Lu-1、Pa-1 和 Istisu-1 的组装由 Edmond 提供，但没有进入论文后续核心分析。构造实验输入时应明确是否纳入它们。
- **T2T 标签**：高 QV、高 BUSCO 完整度、着丝粒重复评估、与 T2T 参考的质量比较以及“最完整”子集都不是逐组装 T2T 证据。本仓库统一保留 Chromosome 级别。
- **参考辅助 scaffolding**：69 个组装使用 Col-CEN 进行排序和定向。评估结构重排、参考偏倚或完全 reference-free 的 MGA 方法时，应记录这一输入特征。
- **最完整子集**：46 个组装用于更严格的基因组大小与着丝粒完整性分析；该子集不能被解释为论文唯一可用集合或 T2T 子集。
- **变异和比对结果**：SV 以 Col-PEK 为参照、由 minimap2、SyRI 和 SURVIVOR 流程产生，不是独立真值。使用时应保持参考版本和参数口径一致。
- **版本匹配**：论文发布时的数据范围与当前 Edmond V3.0 记录可能存在文件更新。复现实验时应记录 Edmond 版本、NCBI assembly accession 完整版本和下载日期。

## 引用与核验

- **论文**：Lian, Q. et al. *A pan-genome of 69 Arabidopsis thaliana accessions reveals a conserved genome structure throughout the global species range*. Nature Genetics 56, 982–991 (2024). [DOI: 10.1038/s41588-024-01715-9](https://doi.org/10.1038/s41588-024-01715-9)。
- **数据引用**：Lian, Q., Schneeberger, K. & Mercier, R. *A pan-genome of 69 Arabidopsis thaliana accessions reveals a conserved genome structure throughout the global species range*. Edmond, V3 (2024). [DOI: 10.17617/3.AEOJBL](https://doi.org/10.17617/3.AEOJBL)。
- **代码引用**：Lian, Q. *qclian/Pan_Ath: Published version of the paper*, v1.0. Zenodo (2024). [DOI: 10.5281/zenodo.10567419](https://doi.org/10.5281/zenodo.10567419)。
- **数据许可**：DataCite 当前元数据将 Edmond V3.0 标为 CC0 1.0 和 open access；Zenodo 代码归档标为 CC BY 4.0。NCBI、ENA、GitHub 及论文配套资源遵循各自页面和发布方条款，不能由本仓库文档许可替代。

| 检查对象（与下载表对应） | 检查日期 | 入口核验结果 | 说明 |
| --- | --- | --- | --- |
| NCBI `PRJNA1033522` | 2026-09-15 | 可访问；69 个 Assembly records | 通过 NCBI BioProject 页面和 E-utilities 核验数量；69 个均登记为 Chromosome |
| ENA `PRJEB62038` | 2026-09-15 | 可访问；公开项目 | ENA API 记录 secondary accession `ERP147129`，项目描述覆盖 72 个品系和三类测序技术 |
| Edmond DOI 与 DataCite 元数据 | 2026-09-15 | DOI 可解析；V3.0、7 个 gzip 文件 | 核验版本、更新日期、许可、文件数量和总大小；Edmond 文件列表页面未稳定读取 |
| Nature Genetics 与 PubMed Central | 2026-09-15 | 可访问 | 核验论文正文、方法、质量指标、数据可用性声明和补充材料入口 |
| GitHub 与 Zenodo 代码归档 | 2026-09-15 | 可访问 | Zenodo 固定版本为 v1.0，归档文件 `qclian-Pan_Ath-v1.0.zip` |

**文件内容验证**：未验证（未下载）。本次只读取网页、API 元数据和开放论文文本，没有下载基因组组装、原始读段或 Edmond 数据包。

**尚未核实的信息**：Edmond V3.0 七个压缩文件的逐文件名称、内部文件格式和逐组装对应关系；是否提供可独立下载的完整原始 whole-genome alignment 文件；GitHub 当前分支与 Zenodo v1.0 之间的完整差异。

## 更新记录

- 2026-09-15：首次收录 69 个核心拟南芥品系组装及相关泛基因组资源；核验论文、NCBI、ENA、Edmond DOI/DataCite、GitHub 和 Zenodo 入口；未下载数据文件。

# 1,086 个 near-T2T 酿酒酵母基因组

[返回首页](../../../README.md) · [数据目录](../../../catalog/README.md) · [真菌分类](../../../catalog/real/fungi.md) · [真菌数据集](../README.md)

所属目录：[真菌基因组资源](../../../catalog/real/fungi.md)。

## 简介

该固定发布集对应论文 *From genotype to phenotype with 1,086 near telomere-to-telomere yeast genomes*，覆盖 1,086 个自然酿酒酵母（*Saccharomyces cerevisiae*）分离株。发布内容包括主组装、备选组装、注释、CDS、结构变异、基因型泛基因组、图泛基因组、8,391 个分子或个体层面性状，以及生成和分析代码。

论文把整个资源描述为 near telomere-to-telomere，但同时明确说明组装并不总是覆盖完整的 telomere-to-telomere 序列。因此，本仓库保留 near-T2T 原文标签，不把该集合整体归为 T2T。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | From genotype to phenotype with 1,086 near telomere-to-telomere yeast genomes |
| 数据记录名称 | Code and data for the analysis of 1,086 near telomere-to-telomere yeast genomes |
| 维护方式 | 固定发布集 |
| 发布机构或项目 | Université de Strasbourg、Genoscope、University of Washington 等论文作者团队 |
| 版本或发布日期 | Zenodo 记录发布日期：2025-06-19；论文 Version of Record：2025-10-15；数据记录未填写独立版本号 |
| 集合标识 / accession | Zenodo DOI：`10.5281/zenodo.15698884`；ENA：`PRJEB77686`、`PRJEB81147` |
| 物种与学名 | 酿酒酵母，*Saccharomyces cerevisiae* |
| 比较范围 | 种内；覆盖不同地理、生态、倍性和杂合状态的自然分离株 |
| 数据性质 | 真实长读长组装及其派生的注释、变异、泛基因组和表型资源 |
| 规模与计数单位 | 1,086 个分离株；1,482 个主组装；另有 1,329 个 second-best assemblies 用于 SV 流程；图构建输入为 500 个 haplotypes |
| 格式与覆盖范围 | Zenodo 以 `tar.gz` 发布；内部包括组装和注释、CDS、TSV、FNA、FAA、VCF、PLINK、GFA、GBZ 及 vg 索引文件 |
| 数据体积 | Zenodo 7 个文件合计 31,462,983,263 bytes，约 31.46 GB；其中组装包约 16.78 GB，图泛基因组包约 14.37 GB |
| 原始集合或派生关系 | 989 个新 ONT 样本加 38 个复用长读长样本形成 1,027 个组装流程输入；再加入参考组装面板的 71 个分离株形成 1,086 个分离株集合 |

## 样本、组装与图的计数关系

| 阶段 | 数量与单位 | 说明 |
| --- | --- | --- |
| 本研究新产生的 ONT 长读长 | 989 个分离株 | `PRJEB77686` 记录 986 个，`PRJEB81147` 记录 3 个 |
| 复用的 ONT 长读长 | 38 个分离株 | 14 个 beer isolates 与 24 个 Taiwanese isolates，来源为先前研究 |
| 进入组装流程的长读长样本 | 1,027 个分离株 | 989 + 14 + 24；论文要求原始覆盖度超过 10× |
| 达到 chromosome-scale 的新组装 | 1,015 个分离株 | 论文对 1,027 个流程输入的结果描述 |
| 复用的参考面板组装 | 71 个分离株 | 来自先前发布的 *S. cerevisiae* reference assembly panel |
| 最终研究集合 | 1,086 个分离株 | 1,015 + 71；其余 12 个流程输入未进入最终 chromosome-scale 集合 |
| Haplotype-resolved isolates | 396 个分离株 | 在 456 个 non-polyploid heterozygous isolates 中有 396 个成功分相，每个贡献两个 haplotype assemblies |
| 主组装 | 1,482 个组装 | 1,086 个分离株加上分相产生的额外 396 个组装 |
| Second-best assemblies | 1,329 个组装，来自 959 个分离株 | 使用其他组装器得到，论文用于支持 singleton SV 判定；Zenodo 组装包说明包含备选组装 |
| 图泛基因组输入 | 500 个 haplotypes | 包含参考基因组和为最大化 SV 覆盖而选择的 499 个组装 |

这些数字不能互换。“1,086”是分离株数，“1,482”是主组装数，“500”是图构建路径输入数；Zenodo 组装包还包含 second-best assemblies，因此压缩包内文件数量也不会等于上述任一数字。

## 适用研究

| 用途 | 依据类型 | 使用方式、来源或判断理由 |
| --- | --- | --- |
| Pangenome | 原研究 | 发布 8,541 个基因家族构成的 gene-based pangenome，以及基于 500 个 haplotypes 的 Minigraph 和 Minigraph-Cactus 图 |
| 结构变异研究 | 原研究 | 提供 1,086 个样本的 SV 矩阵；论文报告 6,587 个非冗余 SV 事件 |
| 图上变异分型与映射 | 原研究 | 发布 GFA、GBZ 及 vg giraffe 所需的 `.dist`、`.min` 和 `.snarls.pb` 文件 |
| 基因型—表型关联 | 原研究 | 发布 8,391 个分子和个体层面性状，并用于 SNP、indel、SV 与 CNV 关联分析 |
| MGA | 潜在用途 | 1,482 个高连续性主组装及 500-haplotype 图输入适合种内多基因组比对；论文没有提供统一 MGA 真值 |

## 组装与质量

- **仓库组装级别**：集合整体保留 near-T2T 描述，不归为 T2T。论文明确报告 1,015 个新组装分离株达到 chromosome-scale；71 个复用参考面板组装的逐文件 T2T 对应关系尚未核实，因此不在本条目汇总为 T2T 数量。
- **来源原始级别**：论文使用 near telomere-to-telomere、chromosome-scale 和 high-quality assemblies 等表述；Zenodo 没有为每个文件提供统一的数据库 assembly-level 字段。
- **T2T 证据**：论文明确写明组装“do not always encompass the entire telomere-to-telomere sequence”，因此 near-T2T 不能等同于 T2T。97.2% 染色体为单 contig 也不能替代逐组装的端粒到端粒证据。
- **判定对象与范围**：论文统计覆盖 1,086 个分离株和 1,482 个主组装；不同质量指标的对象以论文相应统计为准。
- **已公布质量信息**：染色体平均每条 1.06 个 contigs，97.2% 的染色体组装为单 contig；组装长度 11.17–12.95 Mb，平均 11.90 ± 0.17 Mb；平均 Merqury QV 41.5；平均 BUSCO 完整度 99.1%。
- **已知缺失或范围限制**：部分组装没有覆盖完整 T2T 序列；组装流程最后使用 Ragout 参考辅助 scaffolding，发生错误融合时保留未 scaffolding 版本；集合包含不同倍性、杂合状态以及 collapsed 与 phased 组装。

## 下载入口

### 处理后数据与代码

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| Zenodo 数据记录 | 固定记录 `15698884`；全部7个文件 | 数据集页面 | [记录主页](https://zenodo.org/records/15698884) | 公开；CC BY 4.0 |
| 数据说明 | 文件组成和内部主要文件名 | Markdown | [`README.md`](https://zenodo.org/records/15698884/files/README.md?download=1) | 公开；约 2 KB |
| 基因组组装与注释 | 1,086 个分离株的主组装、second-best assemblies、注释和 CDS | `tar.gz` | [`GenomeAssemblies.tar.gz`](https://zenodo.org/records/15698884/files/GenomeAssemblies.tar.gz?download=1) | 公开；16,778,015,358 bytes |
| 基因型泛基因组 | 8,541 个代表基因、CNV 矩阵、CDS、蛋白序列和完全相同区域表 | `tar.gz` | [`GeneBasedPangenome.tar.gz`](https://zenodo.org/records/15698884/files/GeneBasedPangenome.tar.gz?download=1) | 公开；203,407,270 bytes |
| 图泛基因组 | 500-haplotype Minigraph、Minigraph-Cactus 图及 vg giraffe 索引 | `tar.gz` | [`GraphBasedPangenomes.tar.gz`](https://zenodo.org/records/15698884/files/GraphBasedPangenomes.tar.gz?download=1) | 公开；14,370,825,487 bytes |
| 结构变异 | SV VCF 和二值化 gene-CNV PLINK 矩阵 | `tar.gz` | [`SVcalls.tar.gz`](https://zenodo.org/records/15698884/files/SVcalls.tar.gz?download=1) | 公开；30,773,357 bytes |
| 表型 | 论文使用的 8,391 个性状 | `tar.gz` | [`Phenotypes_8391Traits.tar.gz`](https://zenodo.org/records/15698884/files/Phenotypes_8391Traits.tar.gz?download=1) | 公开；79,610,736 bytes |
| 分析脚本 | 组装、SV、泛基因组和 GWAS 流程 | `tar.gz` | [`1000ONT_Scripts.tar.gz`](https://zenodo.org/records/15698884/files/1000ONT_Scripts.tar.gz?download=1) | 公开；348,969 bytes |
| 代码仓库 | 与论文对应的可浏览代码 | GitHub | [`HaploTeam/1086YeastGenomes`](https://github.com/HaploTeam/1086YeastGenomes) | 公开；GitHub 页面未见独立数据下载发布 |

### 原始测序数据与论文

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| ONT 长读长项目 | 986 个新测序分离株；secondary accession `ERP162047` | ENA read runs | [`PRJEB77686`](https://www.ebi.ac.uk/ena/browser/view/PRJEB77686) | 公开 |
| ONT 长读长项目 | 3 个新测序分离株；secondary accession `ERP165003` | ENA read runs | [`PRJEB81147`](https://www.ebi.ac.uk/ena/browser/view/PRJEB81147) | 公开 |
| 论文主页 | Version of Record | HTML、补充材料 | [Nature](https://www.nature.com/articles/s41586-025-09637-0) | 公开文章；第三方材料以页面说明为准 |
| 开放全文 | PMCID `PMC12711572` | HTML | [PubMed Central](https://pmc.ncbi.nlm.nih.gov/articles/PMC12711572/) | 公开 |
| 数据 DOI | Zenodo 固定记录 | DOI | [`10.5281/zenodo.15698884`](https://doi.org/10.5281/zenodo.15698884) | 公开 |

14 个 beer isolates 和 24 个 Taiwanese isolates 是复用的既有长读长数据，分别见[啤酒酵母研究](https://doi.org/10.1016/j.cub.2022.01.068)和[台湾分离株研究](https://doi.org/10.1101/gr.276286.121)。当前论文的数据可用性声明只列出本研究相关的两个 ENA 项目；本条目不猜测这 38 个样本的逐样本 run accession。

## 官方校验值

以下文件大小、MD5 和许可来自 Zenodo 记录 API 元数据。本仓库没有下载这些压缩包，也没有自行重算校验值。

| 文件 | 大小（bytes） | Zenodo MD5 |
| --- | ---: | --- |
| `README.md` | 2,086 | `cad96833e0be4dafd3f2c27a03f2a7cd` |
| `1000ONT_Scripts.tar.gz` | 348,969 | `3a39dfb954fa92b8fd4d1dfee8b3f15c` |
| `SVcalls.tar.gz` | 30,773,357 | `4a1efe5f848159dbbe4f62d3405b0c95` |
| `Phenotypes_8391Traits.tar.gz` | 79,610,736 | `4c68fa5452ef4f20c8be8690e7459efb` |
| `GeneBasedPangenome.tar.gz` | 203,407,270 | `253445bc07f81c1bd21dd20bd6f4d487` |
| `GenomeAssemblies.tar.gz` | 16,778,015,358 | `afd3702d10933a5869acb54531fc32d7` |
| `GraphBasedPangenomes.tar.gz` | 14,370,825,487 | `5b8ecae581d0c0f81feb0ffe89c94724` |

## 配套资源

| 资源 | 提供情况 | 内容、版本对应与下载表中的资源名称 |
| --- | --- | --- |
| 样本清单 | 已提供 | 包含在组装资源及图输入清单中；逐项内容未下载核验 |
| 注释 | 已提供 | `GenomeAssemblies.tar.gz` 包含注释和 CDS |
| 基因型泛基因组 | 已提供 | `GeneBasedPangenome.tar.gz` 包含 1,086 和 3,048 规模的 CNV 矩阵及 8,541 个代表基因 |
| 图泛基因组 | 已提供 | `GraphBasedPangenomes.tar.gz` 包含 500-haplotype Minigraph 与 Minigraph-Cactus 图和 vg 索引 |
| 结构变异 | 已提供 | `SVcalls.tar.gz` 包含 VCF 和 PLINK CNV 矩阵 |
| 表型 | 已提供 | `Phenotypes_8391Traits.tar.gz` 包含 8,391 个性状 |
| 已有比对结果 | 部分提供 | 图构建结果包含多组装整合关系；没有发布可直接作为通用 MGA 真值的比对 |
| 真值 | 无统一 MGA 真值 | 论文以短读段独立检查 500 个 SV，其中 95% 支持 sequence disruption；这不是全基因组比对真值 |

- **真值状态**：无统一多基因组比对真值；结构变异只有部分独立验证。
- **真值类型、来源与覆盖**：500 个 SV 的短读段支持评估，论文报告 95% 的 calls 获得 sequence disruption 支持。该结果不能推广为全部 6,587 个 SV 或任意 MGA 碱基对应关系的真值。
- **可评测对象与限制**：可用于性能、规模和结果一致性比较；精度评测需要另行构造或选择与任务对应的可靠真值。

## 使用注意

- **分离株与组装单位**：1,086 是分离株数，1,482 是主组装数；396 个分相分离株各贡献两个 haplotype assemblies。实验报告必须说明按 isolate 还是 assembly 计数。
- **原始数据覆盖范围**：两个 ENA 项目合计 989 个新测序分离株，并不覆盖全部 1,086 个最终分离株。38 个长读长样本和 71 个参考面板组装来自既有研究。
- **near-T2T 标签**：论文明确指出并非所有组装都覆盖完整 T2T 序列。本仓库不把标题中的 near-T2T 转写为 T2T。
- **参考辅助 scaffolding**：组装流程使用 S288c 参考进行 Ragout scaffolding；分析倒位、易位或其他大尺度结构变化时应考虑这一处理步骤。
- **图子集**：图泛基因组只使用 500 个 haplotypes，不代表全部 1,482 个主组装都进入图构建。
- **SV 文件命名**：Zenodo README 列出 `SV.1087Samples.vcf.gz`，而论文研究规模为 1,086 个分离株。未检查压缩包内容前，不推断额外样本的身份；使用时应核对 VCF header 和样本清单。
- **版本匹配**：组装、图、SV、CNV 和表型应使用同一 Zenodo 固定记录；不要把之后可能更新的 GitHub 代码状态自动视为论文归档版本。
- **大文件下载**：组装包和图包合计超过 31 GB。当前已核验入口与元数据，没有测试完整下载或解压。

## 引用与核验

- **论文**：Loegler, V. et al. *From genotype to phenotype with 1,086 near telomere-to-telomere yeast genomes*. Nature 648, 649–658 (2025). [DOI: 10.1038/s41586-025-09637-0](https://doi.org/10.1038/s41586-025-09637-0)。
- **数据引用**：Loegler, V. et al. *Code and data for the analysis of 1,086 near telomere-to-telomere yeast genomes*. Zenodo (2025). [DOI: 10.5281/zenodo.15698884](https://doi.org/10.5281/zenodo.15698884)。
- **复用参考面板**：O’Donnell, S. et al. *Telomere-to-telomere assemblies of 142 strains characterize the genome structural landscape in Saccharomyces cerevisiae*. Nature Genetics 55, 1390–1399 (2023). [DOI: 10.1038/s41588-023-01459-y](https://doi.org/10.1038/s41588-023-01459-y)。
- **数据许可**：Zenodo 记录元数据标注为 CC BY 4.0、open access。ENA 原始读段和外部复用数据遵循各自仓库与来源条款；论文正文许可不能代替数据记录许可。

| 检查对象（与下载表对应） | 检查日期 | 入口核验结果 | 说明 |
| --- | --- | --- | --- |
| Zenodo 固定记录与7个文件入口 | 2026-09-14 | 可访问 | 页面和文件入口返回成功；文件元数据通过 Zenodo API 核验 |
| Zenodo `README.md` | 2026-09-14 | 已读取说明文件 | 仅读取约 2 KB 的清单说明，没有下载数据压缩包 |
| ENA `PRJEB77686` | 2026-09-14 | 可访问、PUBLIC | ENA 元数据记录 986 个分离株，首次公开日期 2025-09-02 |
| ENA `PRJEB81147` | 2026-09-14 | 可访问、PUBLIC | ENA 元数据记录 3 个分离株，首次公开日期 2025-02-28 |
| Nature、PMC 与 GitHub | 2026-09-14 | 可访问 | 核验论文、开放全文、数据可用性声明和代码入口 |

**文件内容验证**：除 Zenodo 的小型 `README.md` 外，其余文件内容未验证；未下载任何组装、图、变异、表型或测序数据。文件大小和 MD5 来自 Zenodo 元数据，不代表本地完整性检查。

**尚未核实的信息**：1,482 个主组装和 1,329 个 second-best assemblies 在压缩包内的逐文件映射；71 个参考面板组装与具体 T2T 版本的对应；38 个复用长读长样本的逐 run accession；`SV.1087Samples.vcf.gz` 中额外样本的身份。

## 更新记录

- 2026-09-14：首次收录论文数据资源；核验 Zenodo、ENA、Nature、PMC 和 GitHub 入口及公开元数据；未下载大型数据文件。

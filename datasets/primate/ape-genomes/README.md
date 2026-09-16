# T2T Apes：猿类组装与人类联合比对

[返回首页](../../../README.md) · [灵长目持续集合](../README.md) · [所属分类：跨类群集合](../../../catalog/real/cross-group.md)

## 简介

本条目收录 Nature 2025 论文 Complete sequencing of ape genomes 对应的六种非人猿类组装，以及配套的人类参考和跨物种比对。由于联合分析含人类，主要分类为跨类群集合。它是固定论文资源，与维护者的灵长目持续清单分别维护，不覆盖后者的实验快照。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 发布者 | T2T consortium primates project；Makova、Phillippy、Eichler 等团队 |
| 版本 | 论文 2025-04-09；官方 v2.0/v2.1 发布，文件日期与 NCBI accession 版本分别记录 |
| 物种 | *Pan troglodytes*、*P. paniscus*、*Gorilla gorilla*、*Pongo abelii*、*P. pygmaeus*、*Symphalangus syndactylus*；联合分析另含 *Homo sapiens* |
| 比较范围与性质 | 种间；真实二倍体组装、primary 表示、联合比对与隐式泛基因组 |
| 规模 | 六种非人猿类各有二倍体发布；六份 primary 表示不能与两套单倍型再次相加作为新增个体 |
| 人类参考 | CHM13v2.0、HG002v1.0；不是六种新组装的一部分 |
| 联合比对 | CGL 发布 8-way primary progressive alignment，并有其他子集/构图版本；8-way 不表示八个物种 |
| 格式与体积 | FASTA、HAL、MAF、Chains；8-way HAL 官方标注约 17 GB；图表示须按对应分析项目说明 |

## 适用研究

| 用途 | 依据类型 | 使用方式 |
| --- | --- | --- |
| MGA | 原研究 | 使用组装、Cactus HAL/MAF 与链文件研究猿类种间同源关系 |
| Pangenome | 原研究 | all-to-all 比对、隐式图以及 CGL 发布的构图子集；不同结果分别记录 |

## 组装与质量

官方说明 primary 组装达到 T2T 状态，但明确保留大型 rDNA 阵列等例外。下表的 T2T 标签仅适用于该发布范围，不自动扩展到全部 alternate/hap2 序列。

| 物种 | 官方 README 所列 primary accession | 仓库级别与具体例外 | 与现有灵长目清单关系 |
| --- | --- | --- | --- |
| 黑猩猩 | GCA_028858775.2 | T2T；rDNA 例外 | 清单为 GCF_028858775.2；GCA/GCF 不按字符串视为同一 accession |
| 倭黑猩猩 | GCA_029289425.2 | T2T；rDNA，chr22_pat_hsa21 另有 gap | 当前清单未列该物种 |
| 大猩猩 | GCA_029281585.2 | T2T；rDNA 例外 | 清单为 GCA_029281585.3，版本不同 |
| 苏门答腊猩猩 | GCA_028885655.2 | T2T；rDNA，chr18_hap1_hsa16 与 chr1_hap1_hsa1 另有 gap | 清单为 GCF_028885655.2 |
| 婆罗洲猩猩 | GCA_028885625.2 | T2T；rDNA，chr21_hap1_hsa20 缺一个端粒 | 当前清单未列该物种 |
| 合趾猿 | GCA_028878055.3 | T2T；rDNA 例外；v2.1 调整 chr12/19 标签 | 清单为 GCF_028878055.3 |

- **判定依据**：官方 marbl/Primates 的 v2 发布说明；六份 primary 的 T2T 分类包含上述声明的例外，不表示六份完全无缺口。
- **来源原始级别**：本次未逐条查询 NCBI assembly level；现有清单中的 Chromosome 保留原核验范围，不在本次批量改标签。
- **版本边界**：论文数据声明列合趾猿 .2，当前官方 README 列 .3；按所用版本记录，不能把后续版本静默替代论文比对输入。
- **质量与分相**：大猩猩、倭黑猩猩使用家系分相，其余使用 Hi-C；hap1/hap2 不等于跨染色体已知父/母来源。逐组装 QV 和全部 alternate 缺失范围待整理。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 六种猿类组装及 reads | 官方 v2.0/v2.1；含 GenomeArk 逐物种目录 | FASTA 等 | [marbl/Primates 发布表](https://github.com/marbl/Primates#assembly-releases) | 公开；项目声明 CC0 |
| NCBI primary 入口 | accession 对照见上表 | FASTA、metadata | [官方项目的数据导航](https://github.com/marbl/Primates#data-availability) | 公开；下载时固定 accession 版本 |
| CHM13 参考 | CHM13v2.0 | FASTA | [仓库内 CHM13 详情](../../human/t2t-chm13/README.md) | 公开；版本需匹配 |
| HG002 历史输入 | HG002v1.0；不是仓库 Q100 v1.2 | FASTA、浏览器 tracks | [T2T Browser](https://github.com/marbl/T2T-Browser) | 公开；依论文输入版本选择 |
| Cactus 比对与图发布说明 | February 2024；多个子集 | HAL、MAF、图、树和 README | [CGL 发布页](https://cglgenomics.ucsc.edu/february-2024-t2t-apes/) | 公开；本次直接连接失败，检索内容可见 |
| Cactus 数据目录 | t2t-apes 固定子目录 | 文件目录 | [CGL 文件列表](https://cgl.gi.ucsc.edu/data/cactus/t2t-apes/) | 可读取目录 |
| 8-way primary 比对 | 8-t2t-apes-2023v2 | HAL，约 17 GB | [HAL](https://cgl.gi.ucsc.edu/data/cactus/t2t-apes/8-t2t-apes-2023v2/8-t2t-apes-2023v2.hal) | 官方页面列出；未请求数据内容 |
| 8-way 复现说明 | 同一版本 | Markdown | [README](https://cgl.gi.ucsc.edu/data/cactus/t2t-apes/8-t2t-apes-2023v2/8-t2t-apes-2023v2.README.md) | 官方页面列出 |
| MAF 浏览器资源 | 三个比对的 primary reference tracks | hub/MAF tracks | [MAF hub](https://cgl.gi.ucsc.edu/data/cactus/t2t-apes/hubs/t2t-apes-2023v2-cactus-hub.txt) | 官方页面列出；未逐 track 核验 |
| 链文件与隐式泛基因组 | 论文关联分析 | Chains、all-to-all 比对与 impg 说明 | [ape_pangenome](https://github.com/T2T-apes/ape_pangenome) | 公开说明；不能假定全部为可下载 GFA |

## 配套资源

官方 Browser 提供 CAT 注释、比对和其他 tracks；隐式泛基因组仓库按 alignment、impg 等组织。图的表示与 Cactus 子集版本不同，不混为同一图包。

- **真值状态**：未明确；没有确认统一 MGA 真值发布。
- **评测限制**：HAL、MAF、Chains 是分析结果，可作对照，但不是独立真值。

## 使用注意

官方发布中 dip、analysis-dip、pri、alt、mat/pat、hap1/hap2 含义不同。analysis-dip 含额外序列类别，选取全基因组比对输入前应按发布说明明确范围；不要自动将目录全部 FASTA 拼为一个样本。人类参考与非人猿类分别计数。现有清单与本条目仅建立关系，不改变已有选样版本。

## 引用与核验

- **论文**：Yoo, D., Rhie, A., Hebbar, P. et al. [Complete sequencing of ape genomes](https://doi.org/10.1038/s41586-025-08816-3). Nature 641, 401–418 (2025).
- **数据引用**：注明官方版本、文件日期、accession 及 Cactus 具体目录；v1 性染色体发布与 v2 全基因组发布区分。
- **数据许可**：marbl/Primates 声明其数据 CC0；其他派生资源按各发布说明，不从本仓库文档许可推定。

| 检查对象 | 检查日期 | 入口核验结果 | 说明 |
| --- | --- | --- | --- |
| marbl/Primates、ape_pangenome | 2026-09-16 | 官方网页可读取 | 版本、primary 例外、数据表示和许可 |
| CGL 发布页 | 2026-09-16 | 检索内容可见，直接访问失败 | 保留官方入口与明确列出的文件地址 |
| CGL 数据目录 | 2026-09-16 | 可读取 | 未下载比对或序列 |
| 原有灵长目清单 | 2026-09-16 | 本地核对 | 记录四种的 GCA/GCF 或版本差异 |

**尚未核实的信息**：各 HAL/图的完整输入清单、全部单倍型质量与例外、逐 NCBI 原始级别、链文件及图文件逐项可用性。

**文件内容验证**：未验证（未下载）。

## 更新记录

- 2026-09-16：首次收录论文发布集与官方资源入口；仅核验网页和元数据。

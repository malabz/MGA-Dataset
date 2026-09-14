# 灵长目基因组集合

[返回首页](../../README.md) · [数据目录](../../catalog/README.md) · [所属分类：跨类群集合](../../catalog/real/cross-group.md)

## 简介

持续收录人类及其他灵长类的组装基因组、来源和下载入口，可补充新物种、同一物种的其他组装和新版本。集合使用稳定标识 `primates`，名称与目录不随收录数量变化。

首批资源来自维护者的多基因组比对实验清单，当前收录 72 个组装。初始清单覆盖 72 个不同属标签；这描述首批选样，不限制后续同属、同种的多组装收录。尚未按统一分类体系核算灵长目总属数或覆盖率。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 条目名称 | 灵长目基因组集合 |
| 条目标识 | primates |
| 维护方式 | 持续更新；当前清单见 assemblies.tsv，初始输入与核验记录保留日期范围 |
| 集合来源 | 仓库维护者提供的实验清单；单个组装由各原始提交者发布于 NCBI |
| 清单收录日期 | 2026-09-14；不代表实验日期或组装发布日期 |
| 版本范围 | 每条记录保留完整 accession 与版本；后续可追加版本，不静默替换 |
| 物种与比较范围 | 灵长目，种间比较；72 个清单分类单元，包含亚种名称，不将其表述为已核实的 72 个独立物种 |
| 数据性质 | 真实组装 |
| 规模 | 72 个不同组装 accession、72 个不同属标签；60 个 GCA、12 个 GCF；个体数和单倍型数未明确 |
| 文件与覆盖范围 | 目标资源为组装基因组序列，NCBI 页面可选择基因组数据包；实验实际采用全组装、染色体子集还是区域子集未明确 |
| 数据体积 | 未核实 |
| 原始集合或派生关系 | 跨来源手工选样；未提供统一 BioProject 或已发表基准集引用 |

## 适用研究

| 用途 | 依据类型 | 使用方式、来源或判断理由 |
| --- | --- | --- |
| MGA | 维护者实验使用 | 提供者明确说明该集合用于其多基因组比对实验；具体软件、预处理与实验结果未随清单提供 |
| Pangenome（潜在） | 潜在用途 | 可作为跨物种图构建的数据候选；跨度、组装质量及方法适用性需另行评估，尚未提供该集合的泛基因组实验记录 |

模拟对象与场景：不适用。

## 组装与质量

截至 2026-09-14，按本仓库展示级别统计如下。T2T 作为独立级别，已归为 T2T 的记录不重复计入染色体级或 Complete Genome。

| 仓库组装级别 | 当前组装数 |
| --- | --- |
| T2T | 1 |
| Chromosome | 28 |
| Scaffold | 34 |
| Contig | 9 |

恒河猴 `GCA_049350105.2` 在本仓库列为 **T2T**：发布者的 [T2T-MMU8 项目](https://github.com/zhang-shilong/T2T-MMU8)将此 accession 明确对应到 T2T-MMU8v2.0，并说明其完整组装范围。NCBI 原始级别仍保留为 Complete Genome；提供者初始清单则写作 Chromosome，三者分别记录。

当前已核实 1 条 T2T，其他记录的 T2T 证据尚未逐项审核，暂按 NCBI 级别展示。因此表中的 Chromosome 不表示已经证明非T2T，T2T 数量也不是完整普查结论。后续证据支持重新分类时，更新仓库级别并保留来源原始级别。规则见[数据指南](../../docs/data-guide.md)。

## 下载入口

[NCBI 官方下载说明](https://www.ncbi.nlm.nih.gov/datasets/docs/v2/how-tos/genomes/download-genome/)说明可从单个组装记录页面下载数据包。下列入口固定到提供的 accession 版本；打开后核对版本并选择所需的基因组序列文件。本次只检查元数据，不下载序列。

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 当前组装清单 | 随收录更新，逐条固定 accession 版本 | TSV | [assemblies.tsv](assemblies.tsv) | 仓库内公开元信息 |
| 初始输入快照 | 2026-09-14 首批清单 | TSV | [初始清单](sources/2026-09-14-initial.tsv) | 仓库内公开元信息 |
| 组装基因组序列 | 下表各固定版本 accession | 基因组 FASTA，数据包依页面选择 | 下表逐组装官方入口 | NCBI 公开记录；未实际请求序列下载 |
| 官方下载指南 | NCBI Datasets | HTML | [下载说明](https://www.ncbi.nlm.nih.gov/datasets/docs/v2/how-tos/genomes/download-genome/) | 公开 |

### 组装列表

下表展示仓库级别，T2T 单独列出；NCBI 原始级别、来源字段和 T2T 证据保留在[当前 TSV 清单](assemblies.tsv)。初始行序与学名沿用输入，后续可追加组装。列号仅用于浏览，不是稳定样本标识。

| # | 清单学名 | NCBI 组装记录与下载入口 | 仓库组装级别 | 说明 |
| --- | --- | --- | --- | --- |
| 1 | Homo sapiens | [GCA_000001405.29](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_000001405.29/) | Chromosome | — |
| 2 | Pan troglodytes | [GCF_028858775.2](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_028858775.2/) | Chromosome | — |
| 3 | Gorilla gorilla | [GCA_029281585.3](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_029281585.3/) | Chromosome | NCBI 学名：Gorilla gorilla gorilla |
| 4 | Pongo abelii | [GCF_028885655.2](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_028885655.2/) | Chromosome | — |
| 5 | Symphalangus syndactylus | [GCF_028878055.3](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_028878055.3/) | Chromosome | — |
| 6 | Hoolock leuconedys | [GCA_047372625.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_047372625.1/) | Chromosome | — |
| 7 | Hylobates pileatus | [GCA_021498465.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_021498465.1/) | Chromosome | — |
| 8 | Nomascus leucogenys | [GCA_040113105.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_040113105.1/) | Chromosome | — |
| 9 | Erythrocebus patas | [GCA_023783455.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_023783455.1/) | Contig | — |
| 10 | Chlorocebus sabaeus | [GCA_047676025.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_047676025.1/) | Chromosome | — |
| 11 | Cercopithecus mona | [GCA_014849445.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_014849445.1/) | Scaffold | — |
| 12 | Allenopithecus nigroviridis | [GCA_963574245.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963574245.1/) | Scaffold | — |
| 13 | Miopithecus talapoin | [GCA_028551445.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_028551445.1/) | Chromosome | — |
| 14 | Allochrocebus lhoesti | [GCA_963574325.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963574325.1/) | Scaffold | — |
| 15 | Macaca mulatta | [GCA_049350105.2](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_049350105.2/) | T2T | NCBI：Complete Genome；[T2T 依据](https://github.com/zhang-shilong/T2T-MMU8) |
| 16 | Papio anubis | [GCA_008728515.2](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_008728515.2/) | Chromosome | — |
| 17 | Lophocebus aterrimus | [GCA_023783235.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_023783235.1/) | Contig | — |
| 18 | Theropithecus gelada | [GCA_003255815.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_003255815.1/) | Chromosome | — |
| 19 | Cercocebus atys | [GCA_000955945.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_000955945.1/) | Scaffold | — |
| 20 | Mandrillus leucophaeus | [GCA_023783495.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_023783495.1/) | Scaffold | — |
| 21 | Colobus guereza | [GCA_030247045.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_030247045.1/) | Chromosome | — |
| 22 | Piliocolobus tephrosceles | [GCF_002776525.5](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_002776525.5/) | Chromosome | — |
| 23 | Pygathrix nigripes | [GCA_047655245.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_047655245.1/) | Chromosome | — |
| 24 | Semnopithecus entellus | [GCA_047655295.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_047655295.1/) | Contig | — |
| 25 | Trachypithecus shortridgei | [GCA_054345695.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_054345695.1/) | Scaffold | — |
| 26 | Presbytis melalophos mitrata | [GCA_963575215.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963575215.1/) | Scaffold | — |
| 27 | Rhinopithecus roxellana | [GCA_007565055.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_007565055.1/) | Chromosome | — |
| 28 | Nasalis larvatus | [GCA_000772465.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_000772465.1/) | Chromosome | — |
| 29 | Simias concolor | [GCA_047496735.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_047496735.1/) | Scaffold | — |
| 30 | Aotus nancymaae | [GCA_030222135.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_030222135.1/) | Contig | — |
| 31 | Alouatta palliata | [GCA_004027835.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_004027835.1/) | Scaffold | — |
| 32 | Ateles hybridus | [GCA_916098195.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_916098195.1/) | Scaffold | — |
| 33 | Lagothrix lagotricha | [GCA_963574225.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963574225.1/) | Scaffold | — |
| 34 | Brachyteles arachnoides | [GCA_047496155.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_047496155.1/) | Contig | — |
| 35 | Callimico goeldii | [GCA_963573925.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963573925.1/) | Scaffold | — |
| 36 | Callithrix jacchus | [GCF_049354715.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_049354715.1/) | Chromosome | — |
| 37 | Cebuella niveiventris | [GCA_963575025.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963575025.1/) | Scaffold | — |
| 38 | Leontopithecus rosalia | [GCA_054824955.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_054824955.1/) | Chromosome | — |
| 39 | Mico argentatus | [GCA_963573565.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963573565.1/) | Scaffold | — |
| 40 | Saguinus oedipus | [GCA_031835075.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_031835075.1/) | Chromosome | — |
| 41 | Cebus albifrons | [GCA_023783575.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_023783575.1/) | Contig | — |
| 42 | Leontocebus nigricollis | [GCA_963575265.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963575265.1/) | Scaffold | — |
| 43 | Saimiri boliviensis | [GCF_048565385.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_048565385.1/) | Chromosome | — |
| 44 | Sapajus apella | [GCA_022120495.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_022120495.1/) | Scaffold | — |
| 45 | Cacajao ayresi | [GCA_963573425.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963573425.1/) | Scaffold | — |
| 46 | Cheracebus lugens | [GCA_963574535.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963574535.1/) | Scaffold | — |
| 47 | Chiropotes israelita | [GCA_963573965.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963573965.1/) | Scaffold | NCBI 学名：Chiropotes chiropotes |
| 48 | Pithecia pithecia | [GCA_028551515.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_028551515.1/) | Chromosome | — |
| 49 | Plecturocebus cupreus | [GCA_040437455.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_040437455.1/) | Chromosome | — |
| 50 | Tarsius lariang | [GCA_963574405.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963574405.1/) | Scaffold | — |
| 51 | Cephalopachus bancanus | [GCA_027257055.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_027257055.1/) | Contig | — |
| 52 | Carlito syrichta | [GCF_000164805.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_000164805.1/) | Scaffold | — |
| 53 | Daubentonia madagascariensis | [GCA_044048945.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_044048945.1/) | Scaffold | — |
| 54 | Cheirogaleus medius | [GCA_008086735.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_008086735.1/) | Scaffold | — |
| 55 | Mirza coquereli | [GCA_004024645.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_004024645.1/) | Scaffold | — |
| 56 | Microcebus murinus | [GCF_040939455.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_040939455.1/) | Chromosome | — |
| 57 | Lepilemur ruficaudatus | [GCA_963574885.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963574885.1/) | Scaffold | — |
| 58 | Eulemur rufifrons | [GCF_041146395.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_041146395.1/) | Chromosome | — |
| 59 | Hapalemur meridionalis | [GCA_963575175.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963575175.1/) | Scaffold | — |
| 60 | Prolemur simus | [GCA_003258685.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_003258685.1/) | Scaffold | — |
| 61 | Lemur catta | [GCF_020740605.2](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_020740605.2/) | Chromosome | — |
| 62 | Varecia variegata | [GCA_028533085.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_028533085.1/) | Chromosome | — |
| 63 | Avahi laniger | [GCA_963575035.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963575035.1/) | Scaffold | — |
| 64 | Indri indri | [GCA_004363605.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_004363605.1/) | Scaffold | — |
| 65 | Propithecus coquereli | [GCF_000956105.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_000956105.1/) | Scaffold | — |
| 66 | Galago moholi | [GCA_023783435.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_023783435.1/) | Contig | — |
| 67 | Galagoides demidoff | [GCA_963574575.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963574575.1/) | Scaffold | — |
| 68 | Otolemur garnettii | [GCA_000181295.3](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_000181295.3/) | Scaffold | — |
| 69 | Arctocebus calabarensis | [GCA_963573935.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963573935.1/) | Scaffold | — |
| 70 | Loris tardigradus | [GCA_023783135.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_023783135.1/) | Contig | — |
| 71 | Nycticebus coucang | [GCF_027406575.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCF_027406575.1/) | Chromosome | — |
| 72 | Perodicticus potto | [GCA_963574655.1](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_963574655.1/) | Scaffold | — |

## 配套资源

| 资源 | 提供情况 | 说明 |
| --- | --- | --- |
| 组装清单 | 有 | 当前 TSV 提供来源字段、NCBI 级别、仓库级别及核验信息；初始输入另存快照 |
| 注释 | 未明确 | 未逐组装确认具体注释文件及版本 |
| 泛基因组图 | 未明确 | 本次未提供 |
| 已有比对结果 | 未明确 | 本次未提供 |
| 真值 | 未明确 | 本次未提供真值文件或定义 |

真值类型、覆盖范围和可评测对象尚未明确。首批数据来自实验输入，后续新增组装不自动继承“已用于实验”的使用记录。

## 使用注意

- 固定使用清单中的 accession 及版本后缀；GCA 与 GCF 不自动互换，也不自动升级至未来版本。
- 组装数量不等于个体数或单倍型数量；完整组装可能包含非主染色体序列，实验实际预处理范围尚未记录。
- 该集合同时包含人类与其他动物，因此按仓库导航规则归入“跨类群集合”；这不表示它跨越灵长目。
- 科和属沿用提供者记录，尚未完成权威分类学核对。原表同时出现 `Callithrichidae` 与 `Callitrichidae`，`Cercopithecu` 与对应学名的属拼写也不一致；`Leontocebus` 的科归属待核实。保留这些字段，不据此统计规范化科数。
- 三条 NCBI 差异及处理方式见[核验记录](verification.md)。学名差异不自动证明选错组装，需结合命名历史和原始项目判断。
- 初始输入快照仅清理字段首尾空白和引号内换行；当前 TSV 的前六列保留来源字段（其中 Level 为来源清单级别），NCBI_Level、Catalog_Level 分别保存官方原始级别与仓库展示级别；缺失常用名保持为空。
- 尚未提供论文子集与完整发布的映射、实验软件及参数、引用论文或处理后的输入清单。

## 引用与核验

- **集合引用**：暂未提供正式论文或集合 DOI；可引用本仓库条目及其实际 Git 版本，并列明使用的组装 accession。
- **单组装引用与许可**：查看各官方记录中的原始研究和提交者要求；未逐项核实，不将仓库文档许可套用于基因组数据。
- **核验日期**：2026-09-14。
- **元数据核验**：2026-09-14 首批 72 个版本均返回匹配 accession，且当时均标记为 current；未来新增项按各自行级核验日期记录。
- **网页入口核验**：抽查人类及恒河猴记录可访问，其余网页未逐页打开；首批组装存在性通过 NCBI API 验证。未逐一测试页面下载功能。
- **文件内容验证**：未验证（未下载）。
- **尚未核实**：规范化分类及总属覆盖率、逐组装 T2T、质量指标、真实文件内容、实验子集、配套资源与引用许可细节。

详情见[元数据核验记录](verification.md)。

## 持续更新

新增组装时追加当前 TSV 和上方列表，并同步数量、级别统计及分类页。以带版本 accession 去重，允许同一物种多个组装。追加新的核验日期与记录，不将历史批次的 current 状态或实验用途推广到新条目。

初始输入快照保留原实验选样范围；以后实际用于实验的子集应保存具体清单或引用确定的 Git 提交。集合持续扩充时不更改 `primates` 路径。

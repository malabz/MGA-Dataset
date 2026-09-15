# 1KCP：1000 Chinese Pangenome

[返回首页](../../../README.md) · [人类数据目录](../README.md) · [所属分类：人类](../../../catalog/real/human.md)

## 简介

1000 Chinese Pangenome（1KCP）是面向中国人群医学与群体遗传学的大规模二倍体组装和泛基因组资源。项目第一阶段招募 1,379 名参与者，其中 1,144 人同时进行了长读长与短读长全基因组测序；质控后得到 1,116 个二倍体组装，包括 55 个 hifiasm de novo 组装和 1,061 个 pangenome-informed genome assembly（PIGA），共计 2,232 个单倍型基因组。

论文报告多数参与者在主成分分析中与汉族参考人群聚类，但未采集自报祖源信息。因此，本条目将其描述为“中国人群队列”，不将它解释为覆盖中国所有民族或地域人群。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | The 1000 Chinese Pangenome empowers medical and population genetics；1000 Chinese Pangenome（1KCP） |
| 维护方式 | 论文对应的第一阶段固定发布集；门户可能继续更新文件 |
| 发布机构或项目 | 1KCP project；Westlake University 等机构 |
| 论文发布日期 | 2026-04-01 |
| 集合标识 / accession | PRJCA036466、PRJCA039156；HRA011269（已确认的 GSA-Human 入口） |
| 物种与学名 | 人，*Homo sapiens* |
| 比较范围 | 种内 |
| 数据性质 | 真实测序、二倍体组装、单倍型组装、泛基因组图、变异与表达关联资源 |
| 队列与测序规模 | 1,379 名参与者；其中 1,144 人具有长读长与短读长 WGS |
| 组装规模 | 1,116 个二倍体组装：55 个 hifiasm + 1,061 个 PIGA；共 2,232 个单倍型基因组 |
| 格式与覆盖范围 | 全基因组 FASTA；按染色体拆分的 GFA、TSV.GZ、VCF.GZ 和 eQTL summary files |
| 公开汇总数据体积 | 门户当前列出 82 个文件，共约 15.90 GB；不含个体级 reads、assemblies 与 genotypes |
| 原始集合或派生关系 | 1KCP pangenome 从 1KCP、HPRC、CPC、GRCh38 和 CHM13 的整合图中提取，包含 2,232 条 1KCP haplotype paths 及 GRCh38、CHM13 两条参考路径 |

## 适用研究

| 用途 | 依据类型 | 使用方式、来源或判断理由 |
| --- | --- | --- |
| Pangenome | 原研究 | 论文发布 3.74 Gb 的 1KCP pangenome，并在其中分析非参考序列、复杂变异和功能注释 |
| 变异与群体遗传学 | 原研究 | 提供 small variants、SV、TR、nested variants、HLA、eQTL 汇总统计和 pan-variant imputation 资源 |
| MGA | 潜在用途 | 2,232 个单倍型组装和按染色体发布的 GFA 可用于大规模人类种内比对、图构建与图比较；论文未提供通用 MGA 真值 |
| 组装方法评测 | 原研究中的局部基准 | 3 个重叠样本用于 PIGA 下游评估，10 个重叠样本用于 PIGA 流程各步骤评测；不能代表整个队列的统一真值 |

这是一个真实数据集，不涉及模拟对象或模拟生成模型。

## 组装与质量

- **仓库组装级别**：Contig。已核验的两个 BioProject 的 GWH 组装记录均使用来源原始级别“Draft genome in contig level”；本次未逐一枚举 2,232 个单倍型记录的级别。
- **来源原始级别**：GWH 的 PRJCA036466 样例 GWHFTKM00000000.1 与 PRJCA039156 样例 GWHGDHK00000000.1 均标为 contig level。
- **T2T 证据**：未发现与这些 accession 和发布版本对应的 T2T 声明，本仓库不将 1KCP 归为 T2T。
- **判定对象与范围**：仓库级别用于 1KCP 发布的单倍型组装集合；GWH 原始级别核验范围限于上述两个代表记录。
- **组装连续性**：论文报告多数组装的 contig NG50 超过 40 Mb。
- **碱基准确度**：PIGA 组装平均 QV 46，hifiasm 组装平均 QV 54；两种生成方法和测序深度不同，使用时应保留方法标签。
- **结构准确度**：在 3 个重叠样本中，Inspector 检测到每个 hifiasm 组装平均 31 个结构错误、每个 PIGA 组装平均 616 个结构错误。PIGA 的不可靠区域主要位于 satellites 和 segmental duplications，论文据此定义 53.7 Mb 的 GRCh38 common unreliable regions。
- **已知范围限制**：55 个高覆盖样本使用 hifiasm de novo 组装，1,061 个 modest-coverage 样本使用群体信息辅助的 PIGA；两类组装不能在忽略生成流程的情况下作为完全同质的输入集合。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 1KCP 数据门户 | 第一阶段汇总资源与在线工具 | 网页 | [1KCP portal](https://yanglab.westlake.edu.cn/1kcp/home/) | 公开 |
| 汇总资源下载页 | Pangenome、Annotation、Variants、eQTL | GFA.GZ、TSV.GZ、VCF.GZ、summary.gz | [Download](https://yanglab.westlake.edu.cn/1kcp/download) | 公开；页面逐文件下载 |
| Pangenome 校验清单 | chr1–22、X、Y、M，共 25 个 GFA.GZ | MD5 | [1kcp.gfa.md5](https://yanglab.westlake.edu.cn/resources/1kcp/pangenome/1kcp.gfa.md5) | 公开 |
| Pangenome annotation 校验清单 | 25 个按染色体拆分的 annotation TSV.GZ | MD5 | [1kcp.annotation.md5](https://yanglab.westlake.edu.cn/resources/1kcp/annotation/1kcp.annotation.md5) | 公开 |
| Variant 校验清单 | small、SV、TR length、TR motif、nested、HLA VCF.GZ | MD5 | [1kcp.variant.md5](https://yanglab.westlake.edu.cn/resources/1kcp/variant/1kcp.variant.md5) | 公开 |
| eQTL 校验清单 | chr1–22 summary files | MD5 | [1kcp.eqtl.md5](https://yanglab.westlake.edu.cn/resources/1kcp/eqtl/1kcp.eqtl.md5) | 公开 |
| NGDC BioProject | PRJCA036466 | 项目记录；关联 reads、assemblies、genotypes | [PRJCA036466](https://ngdc.cncb.ac.cn/bioproject/browse/PRJCA036466) | 项目页公开；个体级数据按具体记录申请或访问 |
| NGDC BioProject | PRJCA039156 | 项目记录；关联 reads、assemblies、genotypes | [PRJCA039156](https://ngdc.cncb.ac.cn/bioproject/browse/PRJCA039156) | 项目页公开；个体级数据按具体记录申请或访问 |
| GSA-Human | HRA011269；PRJCA036466 | 原始测序数据记录 | [HRA011269](https://ngdc.cncb.ac.cn/gsa-human/browse/HRA011269) | Controlled；需提交数据访问申请 |
| GWH 受控组装样例 | GWHFTKM00000000.1；PRJCA036466 | FASTA 记录 | [GWH record](https://ngdc.cncb.ac.cn/gwh/Assembly/96085/show) | Controlled；需按 BioProject 申请 |
| GWH 公开组装样例 | GWHGDHK00000000.1；PRJCA039156 | FASTA.GZ | [GWH record](https://ngdc.cncb.ac.cn/gwh/Assembly/93611/show) | 公开；说明访问条件在个体记录间并不相同 |
| 分析代码 | 论文发布快照 | ZIP | [Zenodo 10.5281/zenodo.18659653](https://doi.org/10.5281/zenodo.18659653) | 公开；CC BY 4.0 |
| 分析仓库 | 持续维护版本 | scripts | [JianYang-Lab/1KCP-analysis](https://github.com/JianYang-Lab/1KCP-analysis) | 公开；MIT |
| PIGA workflow | 持续维护版本 | workflow、scripts | [JianYang-Lab/PIGA](https://github.com/JianYang-Lab/PIGA) | 公开；MIT |

门户 API 在本次核验时列出 26 个 pangenome 条目（25 个 GFA 文件和 1 个 MD5 清单，约 4.56 GB）、26 个 annotation 条目（约 1.24 GB）、7 个 variant 条目（约 2.11 GB）和 23 个 eQTL 条目（约 7.99 GB）。这里链接门户下载页和官方校验清单，不猜测未列出的批量下载地址。

## 配套资源

| 资源 | 提供情况 | 内容、版本对应与下载表中的资源名称 |
| --- | --- | --- |
| 样本清单 | 有 | 论文 Supplementary Tables 与 NGDC 项目记录；个体级 metadata 的访问条件需按对应记录确认 |
| 注释 | 有 | 按染色体拆分的 pangenome annotation TSV.GZ |
| 泛基因组图 | 有 | 25 个按 chr1–22、X、Y、M 拆分的 GFA.GZ；图总大小由论文报告为 3.74 Gb |
| 变异 | 有 | 35.4 million small variant sites、110,530 SV sites、485,575 polymorphic TR sites 和 0.86 million nested variant sites；门户另提供 HLA VCF |
| 表达关联 | 有 | chr1–22 的 eQTL summary files；论文报告 3,256 个涉及复杂变异的 eQTL |
| 已有比对结果 | 有 | GFA 表示整合后的泛基因组关系；不能自动视为 MGA 真值 |
| 真值 | 部分有 | 3 个样本的 PIGA variant calling 与 phasing 局部评测；没有覆盖 2,232 个 haplotypes 的统一 MGA 真值 |

- **真值状态**：部分有。
- **真值类型、来源与覆盖**：论文在 3 个重叠样本上报告 PIGA 的 SNV、indel 与 SV 平均 F1 分别为 0.9881、0.8576 和 0.9669；以 hifiasm haplotypes 评估 PIGA 局部分相时，平均 switch error rate 为 0.50%，correctly phased block N50 为 618 kb。
- **可评测对象与限制**：这些值评估 PIGA 组装/变异恢复的局部性能，不能作为全队列、全区域或任意 MGA 工具的 ground truth。公开 GFA 是研究产物，不等同于独立真值。

## 使用注意

- **论文子集与完整发布**：项目名中的“1000”不是精确样本数。实验设计涉及 1,379 名参与者、1,144 个 WGS 样本、1,116 个二倍体组装和 2,232 个单倍型组装，引用规模时必须带计数单位。
- **人群描述**：论文称多数参与者通过 PCA 与汉族参考人群聚类，但没有 self-reported ancestry；不要据此宣称覆盖中国所有人群。
- **版本匹配**：使用 GFA、annotation、variant 和 eQTL 时，保留门户发布日期或文件校验值；使用个体组装时同时记录 BioProject、GWH accession、组装方法和版本。
- **图的组成**：1KCP pangenome 含 2,232 条 1KCP haplotype paths，并包含 GRCh38 和 CHM13 参考路径；将路径数作为输入规模时不要遗漏两条参考路径。
- **访问与使用限制**：门户汇总资源公开；个体级 reads、assemblies 和 genotypes 的访问条件并不统一。PRJCA036466 中已核验的 GSA-Human 与 GWH 记录为受控访问，申请前检查当前 Data Access Committee 要求。
- **组装异质性**：55 个 hifiasm de novo 组装与 1,061 个 PIGA 组装有不同测序深度、构建方法和误差特征；比较算法时应分层报告。

## 引用与核验

- **论文**：Wang, Y., Duan, Z., Chen, D. et al. [The 1000 Chinese Pangenome empowers medical and population genetics](https://doi.org/10.1038/s41586-026-10315-y). *Nature* **654**, 121–130 (2026).
- **数据引用**：引用论文，并记录使用的 1KCP portal 文件名与校验清单，或 NGDC BioProject/GWH/GSA-Human accession。
- **分析代码归档**：Wang, Y. [Code for the 1000 Chinese Pangenome (1KCP) analysis](https://doi.org/10.5281/zenodo.18659653), Zenodo (2026)。
- **数据许可**：门户汇总数据和 NGDC 个体数据的统一数据许可尚未在已核验入口中明确；遵守各入口当前条款和人类遗传资源访问要求。分析 GitHub 仓库为 MIT，Zenodo 软件归档为 CC BY 4.0；软件许可不替代数据许可。
- **发布审批**：论文 Data availability 声明列出人类遗传资源管理审批号 2025BAT00888 和 2025BAT00720。

| 检查对象（与下载表对应） | 检查日期 | 入口核验结果 | 说明 |
| --- | --- | --- | --- |
| Nature 论文与 Data availability | 2026-09-15 | 可访问 | 核对论文、规模、质量、数据类型、BioProject 与代码入口 |
| 1KCP portal、下载页与四类 MD5 清单 | 2026-09-15 | 可访问 | API 列表与清单入口响应正常；未下载数据文件 |
| PRJCA036466、PRJCA039156 | 2026-09-15 | 可访问 | BioProject 页面响应正常 |
| HRA011269 | 2026-09-15 | 页面本次直接请求不稳定 | accession 与受控状态已由项目记录确认；使用前建议重新检查 |
| GWHFTKM00000000.1、GWHGDHK00000000.1 | 2026-09-15 | 可访问 | 均标为 contig level；前者 Controlled，后者提供公开 DNA 下载 |
| Zenodo 与两个 GitHub 代码仓库 | 2026-09-15 | 可访问 | Zenodo 记录为公开软件归档，列出 3 个文件及 MD5 |

**文件内容验证**：未验证（按仓库约定未下载数据；仅检查页面、API 文件列表、MD5 清单入口和代表性 GWH 记录）。

**尚未核实的信息**：2,232 个单倍型组装逐条 accession、级别和访问条件尚未枚举；门户汇总数据的统一许可未明确；个体级 GVM accession 未从两个 BioProject 中逐条整理。

## 更新记录

- 2026-09-15：首次收录 Nature 论文对应的 1KCP 第一阶段资源；核验公开汇总下载、两个 NGDC BioProject、代表性受控/公开 GWH 组装记录和代码归档。

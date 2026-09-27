# 野猪与家猪古老渐渗基因组集合

[返回首页](../../../README.md) · [哺乳动物内容目录](../README.md) · [其他动物分类](../../../catalog/real/other-animals.md)

所属目录：[其他动物](../../../catalog/real/other-animals.md)。

## 简介

收录 Science 2026 论文 *Ancient introgression drives wild boar expansion and phenotypic diversification of domestic pigs* 的公开组装与关联群体分析资源。作者项目 README 明确关联正式论文和 Zenodo 数据记录；已确认记录描述提供三个基因组的从头组装、基因注释及重复序列/转座元件注释。

本条目以三份组装为核心，附带群体分析与 Hi-C 入口。研究所述 745 份基因组数据不等于 745 份新组装。Science 正文在本次环境中返回 403，尚未直接读取最终 Data and materials availability；以下下载证据来自作者项目和 Zenodo 公开元数据。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | Ancient introgression drives wild boar expansion and phenotypic diversification of domestic pigs |
| 发布者 | Jian-Hai Chen 等；华中农业大学及合作团队；作者托管数据 |
| 维护方式 | 固定论文研究集合；不同数据记录分别保留 |
| 论文版本 | Science 393, 1335–1341 (2026)；2026 年 9 月正式发表 |
| 集合标识 | 论文 DOI 10.1126/science.adq7553；数据系列 DOI 10.5281/zenodo.10529159 |
| 物种与比较范围 | 三份核心组装为野猪与家猪（Sus scrofa）；种内。关联群体数据还包含猪科外群，具体清单待核实 |
| 数据性质 | 真实从头组装、群体基因型及派生分析；非古 DNA 组装集合 |
| 核心组装规模 | 3 个基因组：尼泊尔 Bampudke p1、尼泊尔 Bampudke p2、wild boar p3；不将 p1/p2 自行解释为同一个体的两个单倍型 |
| 群体规模 | 研究团队说明共 745 份数据、58 个群体，其中 256 份新测序；这些计数不作为新组装数 |
| 数据格式 | genomes.zip 组装/注释包；PLINK BED/BIM/FAM；Hi-C .hic 及 .assembly.gz；文本和 ZIP 分析结果 |
| 数据体积 | genomes.zip 元数据大小 7,806,816,025 bytes（约 7.81 GB）；不代表全部群体资源体积 |
| 版本关系 | 组装和分析数据分散在同一 Zenodo 系列多个固定记录中；最新记录仅含 Hi-C 相关文件 |

## 适用研究

| 用途 | 依据类型 | 使用方式、来源或判断理由 |
| --- | --- | --- |
| 群体基因组与渐渗分析 | 原研究 | 群体结构、重组、谱系关系和古老渐渗研究；作者公开 PLINK 与部分分析结果 |
| Pangenome | 原研究相关分析 | 团队研究说明提及从头组装与图形基因组分析；本次尚未确认独立图文件或最终图输入清单 |
| MGA | 潜在用途 | 可将三份真实组装作为野猪与家猪序列比较候选；需要先核定组装版本和质量，不是已确认的 MGA 标准基准集 |

模拟对象与场景：核心收录不适用。代码仓库包含模拟分析目录，不将其自动视为单独发布且有真值的模拟基准。

## 组装与质量

- **仓库组装级别**：未明确，三份组装均暂不计为 T2T 或 Chromosome。
- **来源原始级别**：Zenodo 描述为 de novo assembly，尚未核定与 p1/p2/p3 对应的 NCBI/GWH accession 及数据库 assembly level。
- **T2T 证据**：未确认。存在 Hi-C 联系矩阵不能证明组装达到染色体级或 T2T。
- **判定对象与范围**：固定组装记录中的 p1、p2、p3；尚未下载解包确认内部 FASTA、注释文件名与版本。
- **已公布质量信息**：本次可读取的元数据没有提供足以逐项核对的 N50、BUSCO、QV 或无缺口统计，保留待核实。
- **范围限制**：不能仅凭包名或 p1/p2 命名推定倍性、分相或相互关系；原始测序项目与最终论文补充样本表待核实。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 正式论文 | Science 2026；adq7553 | 论文与补充材料入口 | [Science DOI](https://doi.org/10.1126/science.adq7553) | 本次直接访问 403；未读取最终正文数据声明 |
| 作者项目 | README 已更新关联 Science 论文 | 说明与分析代码 | [GitHub 项目](https://github.com/JianhaiChen/South-Asian-Wild-boar-and-pig) | 公开；动态更新 |
| 组装、注释及部分分析 | 固定记录 10934580；2024-04-06 | genomes.zip 及配套文件 | [Zenodo 10934580](https://doi.org/10.5281/zenodo.10934580) | 公开；CC BY 4.0 |
| 三份组装包 | 上述记录的 genomes.zip | ZIP；包内格式未解包验证 | [官方文件入口](https://zenodo.org/api/records/10934580/files/genomes.zip/content) | 官方 API 列出的入口；文件内容未下载 |
| 作者 README 原始链接 | 固定记录 10529160；2024-01-18 | 组装、重组率、PLINK 等 | [Zenodo 10529160](https://doi.org/10.5281/zenodo.10529160) | 公开；作为旧记录保留，不重复计算组装 |
| 群体基因型 | 固定记录 11100498；2024-05-01 | 745sample.bed、745sample.bim.zip、745sample.fam | [Zenodo 11100498](https://doi.org/10.5281/zenodo.11100498) | 公开；CC BY 4.0；不是原始 FASTQ |
| 筛选后的 SNP 子集 | 固定记录 13858073；2024-09-29 | PLINK BED/BIM/FAM | [Zenodo 13858073](https://doi.org/10.5281/zenodo.13858073) | 公开；CC BY 4.0；非全量基因型 |
| Hi-C 相关文件 | 固定记录 15253420；2025-04-20 | p1/p2/p3.final.hic 与 .final.assembly.gz | [Zenodo 15253420](https://doi.org/10.5281/zenodo.15253420) | 公开；CC BY 4.0；不替代 genomes.zip |
| 版本目录 | 数据系列全部记录 | JSON 元数据 | [Zenodo versions API](https://zenodo.org/api/records/10529160/versions) | 公开；仅用于核对版本和文件列表 |

## 配套资源

| 资源 | 提供情况 | 内容与边界 |
| --- | --- | --- |
| 基因与重复序列注释 | 发布者说明有 | genomes.zip 描述包含 gene annotation、repeat/transposon annotation；未解包检查 |
| 群体基因型 | 有 | 11100498 的完整 PLINK 文件与 13858073 的筛选子集分别记录；PLINK BED 不等于基因组区间 BED |
| 重组与渐渗结果 | 有 | 组装记录同时包含 50k.zip、Recombination rates-decile.zip、NepalWild-qpgraph.zip 与 f3 文本结果 |
| Hi-C 矩阵 | 有 | 15253420 包含 p1/p2/p3 的 .hic 和配套 .assembly.gz；后者不能当作 FASTA |
| 泛基因组图/已有全基因组比对 | 文件入口未明确 | 有图形基因组分析的研究说明，不据此宣称已提供 GFA、HAL 或 MAF |
| 真值 | 未明确 | 群体变异和渐渗推断均不自动等同于独立比对/结构变异真值 |

## 使用注意

- **版本不是累积全集**：截至 2026-09-27，API 的 latest 指向 15253420，该记录只有 Hi-C 相关文件；要找组装须使用 10934580 或作者所链接的 10529160，不能只提供 latest。
- **过时结果**：同系列 [11212670](https://doi.org/10.5281/zenodo.11212670) 的描述明确标为 obsolete version。本条目不将其 GWAS 等结果列为默认下载资源。
- **日期**：2024/2025 是数据记录日期，2026 是正式论文发表年份，不因数据提前归档而改变论文年份。
- **样本与外群**：11100498 描述提及多个猪科外群。745sample 文件名不是完整物种/样本清单的替代，核心三份组装与群体外群不能混算。
- **最终论文一致性**：作者 README 把既有数据系列关联到正式发表论文，但尚未逐项核对最终补充表、参考坐标与全部发布文件的一致性。
- **古老渐渗含义**：题名研究历史基因交流，不代表组装包提供已灭绝供体的古基因组。

## 引用与核验

- **论文**：Chen, J.-H., Du, X., Zheng, Z. et al. Ancient introgression drives wild boar expansion and phenotypic diversification of domestic pigs. Science 393, 1335–1341 (2026). [DOI](https://doi.org/10.1126/science.adq7553)。
- **数据引用**：Chen, Jian-Hai. 同名 Zenodo 数据集；按实际使用的固定记录分别引用 DOI，组装推荐明确写 10.5281/zenodo.10934580 / genomes.zip，而非只写总系列。
- **数据许可**：上述已检查的组装、PLINK、筛选 SNP 和 Hi-C 记录均为 CC BY 4.0；不自动覆盖其他来源的原始测序或 GitHub 代码。
- **研究范围佐证**：[华中农业大学研究团队报道](https://news.hzau.edu.cn/info/1010/86398.htm)说明 745 份数据、256 份新测序和 3 份新组装；组装发布本身以作者 Zenodo 描述和文件元数据为证据。

| 检查对象 | 检查日期 | 核验结果与范围 |
| --- | --- | --- |
| 作者 GitHub README | 2026-09-27 | 可访问，明确链接数据系列与正式 Science 论文 |
| Science 正文 | 2026-09-27 | HTTP 403；未确认最终数据声明及补充表 |
| Zenodo 10529160、10934580 | 2026-09-27 | API 可访问；列出三份组装；10934580 的 genomes.zip 文件入口 HEAD 返回 200，Content-Length 为 7,806,816,025；未读取文件内容 |
| 11100498、13858073、15253420 | 2026-09-27 | API 可访问；分别确认群体 PLINK、筛选子集及 Hi-C 文件清单与许可 |
| 版本目录与 11212670 | 2026-09-27 | 确认 latest 指向 Hi-C 记录，且另一记录被标为 obsolete |

**文件内容验证**：未验证（未下载）。仅读取网页与 API 元数据，未获取组装、基因型或 Hi-C 文件内容。

**尚未核实的信息**：三份组装 accession/version、组装级别与 T2T 证据、包内 FASTA/注释文件及格式、原始 FASTQ 项目号、完整样本映射、最终论文补充材料与数据版本的一致性、独立图或比对文件。

## 更新记录

- 2026-09-27：首次收录三份猪基因组组装及分散于多个固定记录的关联资源；区分 745 份群体数据与 3 份新组装，标记过时记录及未核实项。

# 番茄 T2T 超级泛基因组

[返回首页](../../../README.md) · [植物数据目录](../README.md) · [所属分类：植物](../../../catalog/real/plants.md)

## 简介

本条目收录 Nature Genetics 2026 论文 A tomato telomere-to-telomere super-pangenome empowers stress resilience breeding 对应的固定发布集，以 Zenodo 固定记录提供组装与注释导航。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 发布者与版本 | Shi、Chen、Wang 等；论文 2026-02-18；数据归档发布于 2025-12-10 |
| 集合标识 | 10.5281/zenodo.17878268；PRJCA030093、PRJNA1201608 |
| 物种与比较范围 | 番茄及近缘野生类群，*Solanum*；论文超级泛基因组覆盖 16 个物种；种内与种间 |
| 数据性质 | 真实组装、注释及超级泛基因组研究资源 |
| 论文规模 | 20 个新 T2T 组装 + 27 个既有 Chromosome 组装；各分析子集需按论文表格匹配 |
| 归档文件 | 21 个 FASTA.GZ + 21 个 GFF.GZ；含 SL6.0 的 v1、v2，不能计为 21 份独立材料 |
| 格式与范围 | 全基因组 FASTA.GZ、GFF.GZ；该固定数据归档未列出 GFA 或独立图包 |
| 数据体积 | 以 Zenodo 逐文件 size 为准；未下载测量 |

## 适用研究

| 用途 | 依据类型 | 使用方式 |
| --- | --- | --- |
| Pangenome | 原研究 | 超级泛基因组、结构变异与着丝粒比较 |
| MGA | 潜在用途 | 近缘植物种内/种间比对，可按物种和完整度分层 |

## 组装与质量

- **仓库组装级别**：论文范围为 T2T 20、Chromosome 27，互斥计数；不是 47 个 T2T。
- **T2T 来源与范围**：论文对 20 个新组装的声明；固定归档提供材料名。逐 GWH accession 与归档版本的映射尚未完成，不能把 T2T 标签无条件继承给 SL6.0 的所有版本。
- **来源原始级别**：27 个既有组装在论文中称 chromosome-scale；未逐数据库记录枚举。
- **质量与缺失**：逐材料 QV、端粒、gap 和缺失区域见论文补充表，未逐文件复核；不推定所有组装同等质量。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 组装与注释 | 固定记录 17878268，42 个文件 | FASTA.GZ、GFF.GZ | [Zenodo 数据归档](https://doi.org/10.5281/zenodo.17878268) | 公开，CC BY 4.0 |
| 文件清单与校验值 | 同一记录，含逐文件下载链接 | JSON | [Zenodo API](https://zenodo.org/api/records/17878268) | 公开 |
| 测序与组装项目 | PRJCA030093 | 项目及关联记录 | [CNCB BioProject](https://ngdc.cncb.ac.cn/bioproject/browse/PRJCA030093) | 论文提供；逐文件条件待核实 |
| 配套重测序与功能数据 | PRJNA1201608 | 项目及测序记录 | [NCBI BioProject](https://www.ncbi.nlm.nih.gov/bioproject/PRJNA1201608) | 论文提供；未逐文件核验 |
| 分析代码 | 论文关联仓库 | scripts | [官方 GitHub](https://github.com/ChunmeiShi02/TomatoT2Tsuperpangenome) | 公开，MIT |
| 代码归档 | 17935735 | 以记录为准 | [Zenodo 代码](https://doi.org/10.5281/zenodo.17935735) | 论文提供；许可另查 |

## 配套资源

已确认归档包含序列与基因注释，未列出单独图或 VCF 文件。论文开展图和 SV 分析不等于已公开对应文件。27 个既有组装的来源须从补充清单进入，不能假定全部在这个 Zenodo 记录内。

- **真值状态**：未明确；未确认统一 MGA 真值。
- **评测限制**：特定 SV 和功能验证不能推广为全基因组碱基对应真值。

## 使用注意

选择 SL6.0 时明确 v1/v2 并匹配同版本 GFF，不能作为两个个体。新组装、既有组装与分析子集分别计数。图文件当前标为入口未确认，代码仓库不当作图数据包。

## 引用与核验

- **论文**：Shi, C., Chen, S., Wang, J. et al. [A tomato telomere-to-telomere super-pangenome empowers stress resilience breeding](https://doi.org/10.1038/s41588-026-02508-y). Nature Genetics 58, 630–642 (2026).
- **数据引用与许可**：固定 Zenodo DOI 与具体文件版本；该数据归档为 CC BY 4.0，GitHub 代码为 MIT。

| 检查对象 | 检查日期 | 入口核验结果 | 说明 |
| --- | --- | --- | --- |
| 官方论文检索内容 | 2026-09-16 | 已核对 | 论文规模和数据声明 |
| Zenodo 数据 API | 2026-09-16 | HTTP 200 | 文件数、版本、开放状态和许可 |
| GitHub | 2026-09-16 | HTTP 200 | 分析代码，MIT |
| BioProject 与代码归档 | 尚未直接核验 | 论文给出入口 | 不宣称逐文件可访问 |

**尚未核实的信息**：GWH accession 与归档版本的对应、SL6.0 两版本差异、27 个既有组装清单、独立图/VCF 下载入口、逐材料质量与缺口。

**文件内容验证**：未验证（未下载）。

## 更新记录

- 2026-09-16：首次收录论文发布集与官方资源入口；仅核验网页和元数据。

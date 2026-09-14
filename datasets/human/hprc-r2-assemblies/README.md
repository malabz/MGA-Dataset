# HPRC Release 2 组装

[返回首页](../../../README.md) · [人类数据目录](../README.md) · [所属分类：人类](../../../catalog/real/human.md)

## 简介

Human Pangenome Reference Consortium 的第二批群体单倍型组装资源。官方 `assemblies_release2_v1.0.index.csv` 是当前固定入口索引，逐行提供样本、haplotype、phasing、assembly method、GenBank accession、FASTA、FAI、GZI 和 MD5 的 S3 地址。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | HPRC Release 2 assemblies，index v1.0 |
| 发布者 | Human Pangenome Reference Consortium |
| 索引版本 | v1.0，变更记录日期 2025-10-01 |
| 数据性质 | 人类群体单倍型分相组装及参考/合作项目条目 |
| 当前规模 | 234 个样本、466 条 haplotype/index records |
| 来源构成 | 216 HPRC、14 HPP collaboration、4 extramural samples |
| 组装方法 | 官方索引当前为 452 hifiasm、12 Verkko、2 个参考条目未填方法 |
| 仓库组装级别 | 混合；不作整批 T2T 声明 |

以上数量于 2026-09-14 直接统计官方 v1.0 索引。后续索引更新时需重新统计，不能把这里的数量当作永久规模。

## 适用研究

- 大规模人类单倍型 MGA、组装比较及泛基因组构建。
- 按样本、phasing 或 assembly method 选择子集。
- 作为 HPRC Release 2 泛基因组图的主要输入来源；实际入图集合与完整索引并不完全等同。

## 组装与质量

本条目不把 Release 2 整体标为 T2T。官方索引包含多种来源和组装方法；T2T 必须逐 assembly/version 查证。HPRC 的 `assembly` 列是直接 FASTA 地址，`genbank_accession` 可用于固定公开版本；二者的命名和序列排序可能因发布处理而不同。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| HPRC Data Explorer | 当前门户数据 | 交互表 / TSV | [Assemblies](https://data.humanpangenome.org/assemblies) | 公开 |
| Release 2 组装索引 | v1.0，466 条 | CSV | [官方索引](https://raw.githubusercontent.com/human-pangenomics/hprc_intermediate_assembly/main/data_tables/assemblies_release2_v1.0.index.csv) | 公开；S3 可匿名访问 |
| 索引说明与变更记录 | Release 2 | Markdown | [data_tables README](https://github.com/human-pangenomics/hprc_intermediate_assembly/blob/main/data_tables/README.md) | 公开 |
| 样本构成说明 | Release 2 | Markdown | [sample README](https://github.com/human-pangenomics/hprc_intermediate_assembly/blob/main/data_tables/sample/README.md) | 公开 |
| UCSC HPRC assembly hub | 已纳入 UCSC 的组装 | 浏览器与单组装下载 | [Assembly hub](https://hgdownload.cse.ucsc.edu/hubs/HPRC/index.html) | 公开 |

## 配套资源与使用注意

索引提供 MD5、FAI 和 GZI 地址，适合批量选择和核验。Release 2 历史中曾修正 FASTA 排序和 haplotype swap，必须使用带版本的索引并保留下载时的索引快照。234 个样本、466 条记录包括外部参考级条目，不能简化为“234 个 HPRC 新个体”或“466 个独立个体”。

## 引用与核验

- 官方 v1.0 CSV、说明页、数据门户和 UCSC hub 于 2026-09-14 检查可访问。
- 只读取索引元数据并统计行数，未下载任何组装 FASTA。
- 使用前阅读 [HPRC Data Use Protocol](https://humanpangenome.org/data-use/)；引用应匹配 Release 2 论文/预印本及实际 assembly accession。

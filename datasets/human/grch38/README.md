# GRCh38.p14

[返回首页](../../../README.md) · [人类数据目录](../README.md) · [所属分类：人类](../../../catalog/real/human.md)

## 简介

Genome Reference Consortium 维护的人类参考基因组 GRCh38 的第 14 个 patch release。这里固定记录 GenBank accession `GCA_000001405.29`；其配对 RefSeq 版本为 `GCF_000001405.40`，两者内容并非完全相同，使用时不要只写“hg38”。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | Genome Reference Consortium Human Build 38 patch release 14，GRCh38.p14 |
| 发布者 | Genome Reference Consortium |
| accession | GCA_000001405.29；配对 RefSeq GCF_000001405.40 |
| 发布日期 | 2022-02-03（NCBI assembly metadata） |
| 数据性质 | 单一参考组装，含 alternate loci、patches 及未定位/未放置序列 |
| 组装类型 | haploid-with-alt-loci |
| 仓库组装级别 | Chromosome |
| NCBI 原始级别 | Chromosome |

## 适用研究

- 人类组装与序列比对的传统参考坐标。
- 泛基因组图的参考路径；具体图通常只选择染色体序列，需核对是否包含 alt、patch 和 unplaced contigs。
- 与 T2T-CHM13、HG002 或群体组装比较时，必须注明 p14、GCA/GCF 及序列命名版本。

## 组装与质量

本仓库列为 **Chromosome**，不列为 T2T。NCBI 描述中仍包含未定位、未放置及 patch 相关序列；染色体级不能作为 T2T 证据。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| NCBI Assembly 页面 | GCA_000001405.29 | HTML / data package | [官方记录](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_000001405.29/) | 公开 |
| GenBank genomic FASTA | GRCh38.p14 | FASTA.gz | [直接下载](https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/000/001/405/GCA_000001405.29_GRCh38.p14/GCA_000001405.29_GRCh38.p14_genomic.fna.gz) | 公开 |
| GenBank 版本目录 | GRCh38.p14 | FASTA、GFF、GBFF 等 | [目录](https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/000/001/405/GCA_000001405.29_GRCh38.p14/) | 公开 |
| RefSeq 版本目录 | GCF_000001405.40 | FASTA、GFF、GBFF 等 | [目录](https://ftp.ncbi.nlm.nih.gov/genomes/all/GCF/000/001/405/GCF_000001405.40_GRCh38.p14/) | 公开 |

## 配套资源与使用注意

NCBI 版本目录提供注释、序列报告和校验文件。GenBank 与 RefSeq 有差异；UCSC `hg38`、Ensembl GRCh38 及分析流程中的自定义 FASTA 也可能采用不同的 contig 集或命名方式。比对或构图前保存 FASTA 文件名、checksum 和 `.fai`，不能仅凭版本别名推定输入相同。

## 引用与核验

- NCBI accession 页面和两个 FTP 入口于 2026-09-14 检查可访问。
- 组装元数据通过 NCBI Datasets API 核对；文件未下载，内容未验证。
- 数据使用与引用要求以 NCBI/GRC 记录为准。

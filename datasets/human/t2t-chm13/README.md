# T2T-CHM13v2.0

[返回首页](../../../README.md) · [人类数据目录](../README.md) · [所属分类：人类](../../../catalog/real/human.md)

## 简介

Telomere-to-Telomere Consortium 发布的完整人类参考组装，GenBank accession 为 `GCA_009914755.4`。v2.0 在 CHM13v1.1 核基因组基础上加入来自 HG002 的已完成 Y 染色体，因此不是单一供体的完整二倍体组装。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | T2T-CHM13v2.0（T2T-CHM13+Y） |
| 发布者 | T2T Consortium |
| accession | GCA_009914755.4；配对 RefSeq GCF_009914755.1 |
| 组装日期 | 2022-01-24（NCBI assembly metadata） |
| 数据性质 | 组合单参考；CHM13 常染色体与 X，加 HG002 Y |
| 仓库组装级别 | T2T |
| NCBI 原始级别 | Complete Genome |

## 适用研究

- 以完整人类染色体和复杂重复区为基础的 MGA、泛基因组、注释及变异研究。
- 作为 HPRC、HGSVC 等泛基因组图的参考路径。
- CHM13 组装评测通常应使用无 Y 的 v2.0/noY（等同 v1.1 核序列），避免把 HG002 Y 当成 CHM13 来源。

## 组装与质量

发布者明确将 v2.0 定义为完整 T2T reconstruction，本仓库因此列为 **T2T**。T2T 范围和供体组成必须与版本一起引用；NCBI 的 Complete Genome 原始级别另行保留。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 项目主页 | v2.0 及历史版本 | 文档与下载目录 | [marbl/CHM13](https://github.com/marbl/CHM13) | 公开，项目声明 CC0 |
| NCBI Assembly 页面 | GCA_009914755.4 | HTML / data package | [官方记录](https://www.ncbi.nlm.nih.gov/datasets/genome/GCA_009914755.4/) | 公开 |
| GenBank genomic FASTA | GCA_009914755.4 | FASTA.gz | [直接下载](https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/009/914/755/GCA_009914755.4_T2T-CHM13v2.0/GCA_009914755.4_T2T-CHM13v2.0_genomic.fna.gz) | 公开 |
| NCBI 版本目录 | GCA_009914755.4 | FASTA、GFF、GBFF 等 | [目录](https://ftp.ncbi.nlm.nih.gov/genomes/all/GCA/009/914/755/GCA_009914755.4_T2T-CHM13v2.0/) | 公开 |
| T2T analysis set | v2.0，多种 Y/PAR 与 mtDNA 处理版本 | FASTA、BED、索引 | [AWS 目录](https://s3-us-west-2.amazonaws.com/human-pangenomics/index.html?prefix=T2T/CHM13/assemblies/analysis_set/) | 公开 |

## 配套资源与使用注意

项目主页同时提供 repeat、centromere/satellite、segmental duplication、gene annotation、variant call、liftover chain 和 PAF。`chm13v2.0.fa.gz`、`noY`、`maskedY`、`maskedY.rCRS` 的适用场景不同；记录具体文件名与 checksum。图构建时还要核对是否移除 Y、线粒体及重复掩蔽方式。

## 引用与核验

- 项目主页、NCBI 页面、GenBank FASTA 和目录于 2026-09-14 检查可访问。
- T2T 证据来自发布者项目；文件未下载，内容未验证。
- 项目列出的核心引用包括 Nurk et al., *Science* (2022) 和 Rhie et al., *Nature* (2023)；按实际使用版本选择引用。

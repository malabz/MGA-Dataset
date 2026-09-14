# HG002 Q100 v1.2

[返回首页](../../../README.md) · [人类数据目录](../README.md) · [所属分类：人类](../../../catalog/real/human.md)

## 简介

T2T Consortium、HPRC 与 Genome in a Bottle 共同维护的 HG002（NA24385）完整二倍体基因组。当前记录 v1.2（2026-08），将父系和母系的 46 条染色体放在一个 FASTA 中，可用于组装质量评测和基于完整基因组的变异基准。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | HG002 “Q100” project assembly v1.2 |
| 样本 | HG002 / NA24385 / GM24385 |
| 发布者 | T2T Consortium、HPRC、GIAB |
| 版本 | v1.2，2026-08-06 |
| 数据性质 | 二倍体、单倍型分相组装 |
| 规模 | 46 条父系/母系染色体；另有线粒体及相关资源 |
| 仓库组装级别 | T2T，但 9/10 rDNA arrays 仍以 N gap scaffold |

## 适用研究

- 人类二倍体 MGA、单倍型分相和组装质量评测。
- Genome in a Bottle 小变异与结构变异基准的组装基础；基准文件须另行选择并匹配版本。
- 泛基因组输入和评测保留样本；使用 HPRC 提供的 evaluation graph 时核对是否排除了 HG002。

## 组装与质量

发布者把 v1.2 描述为 46 条染色体的 T2T reconstruction，同时明确 10 个 rDNA arrays 中有 9 个仍包含 N gap，其余部分 otherwise T2T，估计 Merqury QV 为 69.2。本仓库列为 **T2T（带 rDNA 缺口限定）**，不能将它表述为无任何 gap 的完全组装。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 项目主页 | 当前和历史版本 | 文档与资源目录 | [marbl/HG002](https://github.com/marbl/HG002) | 公开，组装数据声明 CC0 |
| 二倍体组装 | v1.2 | FASTA.gz | [直接下载](https://s3-us-west-2.amazonaws.com/human-pangenomics/T2T/HG002/assemblies/hg002v1.2.fasta.gz) | 公开 |
| 组装目录 | v0.7–v1.2 及配套文件 | FASTA、patch、图等 | [AWS 目录](https://s3-us-west-2.amazonaws.com/human-pangenomics/index.html?prefix=T2T/HG002/assemblies/) | 公开 |
| 评测资源 | v1.2 | GQC resource bundle | [GQC 项目](https://github.com/marbl/GQC) | 公开 |

## 配套资源与使用注意

v1.1 的父系和母系 GenBank accession 分别为 `GCA_018852605.3` 和 `GCA_018852615.3`；v1.2 是面向 GQC 的后续修订 FASTA，不能把 v1.1 accession 当作 v1.2 的等价版本。项目还提供补丁、rDNA morph、组装图、注释和测序数据入口。

“真值”依赖具体任务：高质量组装不自动成为所有比对关系的真值；GIAB variant benchmark 也必须记录版本、参考坐标和 confident regions。

## 引用与核验

- 项目主页和 v1.2 FASTA 入口于 2026-09-14 检查可访问；未下载文件。
- 版本、T2T 限定和 QV 来自发布者项目。当前引用为 Hansen et al., *Cell* (2026)，并按所用基准补充 GIAB 引用。

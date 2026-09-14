# HGSVC Phase 3

[返回首页](../../../README.md) · [人类数据目录](../README.md) · [所属分类：人类](../../../catalog/real/human.md)

## 简介

Human Genome Structural Variation Consortium Phase 3 发布的 65 个多样本人类样本的单倍型分相、近完整组装及派生泛基因组和结构变异资源。主分析采用 Verkko assemblies；同时归档了 hifiasm assemblies。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | HGSVC Phase 3 |
| 发布者 | Human Genome Structural Variation Consortium |
| 版本范围 | Assembly_Info v2.0；正式 release 下的各版本资源 |
| 数据性质 | 65 人、130 个 phased haplotypes；人类种内多样性 |
| 主组装方法 | Verkko，结合 long reads 与 Strand-seq phasing；另有 hifiasm set |
| assembly BioProject | Verkko `PRJEB76276`；hifiasm `PRJEB83624` |
| 仓库组装级别 | 近完整、级别和 gap 状态需逐组装核对；不统一归为 T2T |

## 适用研究

- 单倍型分相人类基因组的 MGA、组装质量和复杂区域分析。
- 构建或扩展人类泛基因组；Phase 3 论文构建了包含 65 个 HGSVC 与 42 个 HPRC 个体的 214-haplotype Minigraph-Cactus graph。
- assembly-based structural variant discovery、genotyping 及群体比较。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| HGSVC 资源页 | Phase 2/3 导航 | 文档与数据入口 | [hgsvc.org](https://www.hgsvc.org/resources) | 公开 |
| Phase 3 发布根目录 | 正式 release | 目录索引 | [IGSR FTP](https://ftp.1000genomes.ebi.ac.uk/vol1/ftp/data_collections/HGSVC3/release/) | 公开 |
| Assembly_Info | v2.0 | accession、QV、manifest | [目录](https://ftp.1000genomes.ebi.ac.uk/vol1/ftp/data_collections/HGSVC3/release/Assembly_Info/v2.0/) | 公开 |
| Verkko assembly accession 项目 | PRJEB76276 | ENA records / assembly files | [ENA BioProject](https://www.ebi.ac.uk/ena/browser/view/PRJEB76276) | 公开 |
| hifiasm assembly accession 项目 | PRJEB83624 | ENA records / assembly files | [ENA BioProject](https://www.ebi.ac.uk/ena/browser/view/PRJEB83624) | 公开 |
| Graph Genomes | release 1.0 | graph resources | [目录](https://ftp.1000genomes.ebi.ac.uk/vol1/ftp/data_collections/HGSVC3/release/Graph_Genomes/1.0/) | 公开 |
| 项目分析与引用仓库 | Phase 3 paper | 文档与代码 | [hgsvc/phase3-main-pub](https://github.com/hgsvc/phase3-main-pub) | 公开 |

## 配套资源与使用注意

release 还包含 Variant_Calls、Centromeres、Segmental_Duplications、Mobile_Elements、chrY analyses 和 1kGP genotyping。`working/` 可包含未正式发布的文件；优先使用 `release/` 和版本化目录。

Assembly_Info v2.0 明确指出 HG00514 的旧 Verkko assembly 存在数据损坏，`20240201_verkko_batch3` 版本不应继续分析；新分析必须使用 `20241001_verkko_HG00514_fix` 对应版本。任何镜像或旧清单都应检查这一例外。

## 真值与限制

该集合适合 assembly-based SV 分析，但 assembly 或整合 callset 不自动成为 MGA 同源关系真值。需要按评测任务选择参考坐标、truth regions 和版本。论文称 nearly complete，不表示 130 个 haplotypes 已逐条满足本仓库 T2T 判定。

## 引用与核验

- 官方 HGSVC 页面、IGSR release、Assembly_Info v2.0、两个 ENA BioProject 和 GitHub 仓库于 2026-09-14 检查可访问。
- 文件未下载；只检查目录、README 和 accession 入口。
- 主要引用：Logsdon, Ebert, Audano, Loftus et al., “Complex genetic variation in nearly complete human genomes,” *Nature* (2025), DOI [10.1038/s41586-025-09140-6](https://doi.org/10.1038/s41586-025-09140-6)。

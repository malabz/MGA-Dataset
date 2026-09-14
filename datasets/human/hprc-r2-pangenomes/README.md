# HPRC Release 2 泛基因组

[返回首页](../../../README.md) · [人类数据目录](../README.md) · [所属分类：人类](../../../catalog/real/human.md) · [关联组装](../hprc-r2-assemblies/README.md)

## 简介

Human Pangenome Reference Consortium 基于 Release 2 组装构建的泛基因组资源，官方页面集中提供 Minigraph、Minigraph-Cactus v2.1、PGGB、IMPG 以及配套图索引、HAL、MAF、PAF 和 VCF。资源页面明确标记这些数据尚未完成全部 QC、尚未正式发表且可能存在已知问题。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | HPRC Pangenome Resources from Release 2 / year 2 data |
| 发布者 | Human Pangenome Reference Consortium |
| 当前主要版本 | Minigraph-Cactus v2.1；PGGB/IMPG Release 2 |
| 数据性质 | 人类群体泛基因组图、多序列比对、all-vs-all alignment 和变异表示 |
| 图构建输入 | 232 个 assembled samples 中排除 HG00272，再加入 GRCh38 与 CHM13，共 464 haplotypes |
| 参考路径 | 按产品提供 GRCh38、CHM13 或 GRCh37 版本 |
| 组装级别 | 输入组装级别混合；图资源本身不使用 T2T/Chromosome 标签 |

## 适用研究

- 直接使用 GFA/GBZ 进行人类泛基因组分析、短读长或长读长映射。
- 使用 HAL、MAF、PAF 或 IMPG TPA 进行多基因组比对分析。
- 比较 reference-progressive 的 Minigraph/Minigraph-Cactus 与 all-vs-all 的 PGGB/IMPG。
- 使用评测图进行 GIAB 样本测试时，应选择排除目标样本的专用版本。

## 主要下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 官方资源总表 | Release 2 | 文档、索引与全部链接 | [hpp_pangenome_resources](https://github.com/human-pangenomics/hpp_pangenome_resources) | 公开 |
| Minigraph-Cactus GRCh38 图 | v2.1 | GFA.gz | [直接下载](https://s3-us-west-2.amazonaws.com/human-pangenomics/pangenomes/freeze/release2/minigraph-cactus/v2.1/hprc-v2.1-mc-grch38/hprc-v2.1-mc-grch38.gfa.gz) | 公开 |
| Minigraph-Cactus CHM13 图 | v2.1 | GFA.gz | [直接下载](https://s3-us-west-2.amazonaws.com/human-pangenomics/pangenomes/freeze/release2/minigraph-cactus/v2.1/hprc-v2.1-mc-chm13/hprc-v2.1-mc-chm13.gfa.gz) | 公开 |
| GRCh38 多序列比对 | v2.1 full | HAL | [直接下载](https://s3-us-west-2.amazonaws.com/human-pangenomics/pangenomes/freeze/release2/minigraph-cactus/v2.1/hprc-v2.1-mc-grch38/hprc-v2.1-mc-grch38.full.hal) | 公开 |
| CHM13 多序列比对 | v2.1 full | HAL | [直接下载](https://s3-us-west-2.amazonaws.com/human-pangenomics/pangenomes/freeze/release2/minigraph-cactus/v2.1/hprc-v2.1-mc-chm13/hprc-v2.1-mc-chm13.full.hal) | 公开 |
| GRCh38 多序列比对 | v2.1 full | MAF.gz + TAI | [MAF](https://s3-us-west-2.amazonaws.com/human-pangenomics/pangenomes/freeze/release2/minigraph-cactus/v2.1/hprc-v2.1-mc-grch38/hprc-v2.1-mc-grch38.full.maf.gz) · [索引](https://s3-us-west-2.amazonaws.com/human-pangenomics/pangenomes/freeze/release2/minigraph-cactus/v2.1/hprc-v2.1-mc-grch38/hprc-v2.1-mc-grch38.full.maf.gz.tai) | 公开 |
| CHM13 多序列比对 | v2.1 full | MAF.gz + TAI | [MAF](https://s3-us-west-2.amazonaws.com/human-pangenomics/pangenomes/freeze/release2/minigraph-cactus/v2.1/hprc-v2.1-mc-chm13/hprc-v2.1-mc-chm13.full.maf.gz) · [索引](https://s3-us-west-2.amazonaws.com/human-pangenomics/pangenomes/freeze/release2/minigraph-cactus/v2.1/hprc-v2.1-mc-chm13/hprc-v2.1-mc-chm13.full.maf.gz.tai) | 公开 |
| PGGB whole-genome graph | Release 2，p98-k311 | GFA.zst | [直接下载](https://s3-us-west-2.amazonaws.com/human-pangenomics/pangenomes/freeze/release2/pggb/gfas/whole-genome/20250930_hprc25272.p98-k311.tmp.fix.gfa.zst) | 公开 |
| IMPG all-vs-all alignment | Release 2 | PAF.gz | [直接下载](https://s3-us-west-2.amazonaws.com/human-pangenomics/pangenomes/freeze/release2/impg/pafs/hprc25272.aln.paf.gz) | 公开 |
| GIAB evaluation graphs | 排除 HG002、HG005、NA19240 的版本 | 图与索引目录 | [目录](https://s3-us-west-2.amazonaws.com/human-pangenomics/index.html?prefix=pangenomes/freeze/release2/minigraph-cactus/v2.1/benchmark-graphs/) | 公开 |

## 配套资源与版本边界

官方总表还提供 GBZ、VG indexes、VCF、PanGenie VCF、chromosome graphs、excluded-region BED 和 reference-gap BED。默认图、full graph、AF-filtered graph 的序列范围不同；Minigraph-Cactus 会裁剪不能可靠放入图的 contig/区段，不能把图覆盖率等同于输入 FASTA 总长度。

CHM13 图、GRCh38 图和 evaluation graph 对 Y 染色体、参考序列及留出样本的处理不同。MGA 或准确率评测必须记录具体资源名、参考路径、v2.1、过滤版本和留出集合。

## 真值与限制

资源包含针对 HG002、HG005 和 NA19240 的留出评测图，但图本身不构成通用真值。需要结合 GIAB 或其他任务特定 truth set，并确认坐标参考。官方当前警告尚未全部 QC 和正式发表，因此不能把 Release 2 结果直接视为最终基准。

## 引用与核验

- 官方 README 和上述直接链接于 2026-09-14 检查可访问；未下载数据文件。
- Release 2 页面链接预印本 “HPRC2: A human pangenome reference with near-complete coverage of common genetic variation”（2026）。
- 使用前阅读 [HPRC Data Use Protocol](https://humanpangenome.org/data-use/)。

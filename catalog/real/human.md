# 人类基因组资源

[返回首页](../../README.md) · [返回真实数据目录](README.md)

收录可用于人类多基因组比对、泛基因组构建及相关评测的参考组装、群体单倍型组装和已构建泛基因组。组装集合与由其产生的图或多序列比对分别列出，便于选择输入或直接使用现成结果。

| 数据集 | 物种与比较范围 | 当前规模 | 组装级别 | 用途 | 真值 |
| --- | --- | --- | --- | --- | --- |
| [APGp1](../../datasets/human/apgp1/README.md) | 东亚人群；种内 | 160 人、320 个单倍型组装 | 项目称 near-T2T；未归为 T2T | MGA、Pangenome | 无统一比对真值 |
| [GRCh38.p14](../../datasets/human/grch38/README.md) | 人类参考组装 | 1 个参考组装 | Chromosome | MGA/Pangenome 参考、坐标体系 | 不适用 |
| [HG002 Q100 v1.2](../../datasets/human/hg002-q100/README.md) | HG002 二倍体 | 46 条单倍型染色体 | T2T（9/10 rDNA 阵列仍含 N gap） | MGA、组装评测、变异基准 | 部分有；需匹配具体基准版本 |
| [HGSVC Phase 3](../../datasets/human/hgsvc3/README.md) | 全球多样性人群；种内 | 65 人、130 个 phased haplotypes | 近完整；未统一归为 T2T | MGA、Pangenome、结构变异 | 无统一比对真值 |
| [HPRC Release 2 组装](../../datasets/human/hprc-r2-assemblies/README.md) | 全球多样性人群；种内 | 234 个样本、466 条索引记录 | 混合；未统一归为 T2T | MGA、Pangenome | 无统一比对真值 |
| [HPRC Release 2 泛基因组](../../datasets/human/hprc-r2-pangenomes/README.md) | 全球多样性人类单倍型；种内 | 图构建输入共 464 个 haplotypes | 输入级别混合 | Pangenome、MGA、映射和变异分析 | 提供排除样本的评测图，不是通用真值 |
| [T2T-CHM13v2.0](../../datasets/human/t2t-chm13/README.md) | 人类单参考；CHM13 与 HG002 chrY | 1 个组合参考组装 | T2T | MGA/Pangenome 参考、复杂区域分析 | 不适用 |

列表按数据集名称排序。T2T 仅在有版本对应的发布者或论文证据时使用；near-T2T、近完整和 Complete Genome 不自动并入 T2T。具体下载入口、版本边界和限制见各详情页。

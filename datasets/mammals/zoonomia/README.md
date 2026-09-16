# Zoonomia 哺乳动物比较基因组集合

[返回首页](../../../README.md) · [哺乳动物内容目录](../README.md) · [跨类群分类](../../../catalog/real/cross-group.md)

所属目录：[跨类群集合](../../../catalog/real/cross-group.md)，因为包含人类和其他动物；这不表示哺乳动物本身不是一个类群。

## 简介

收录 Zoonomia 的 240 种哺乳动物比较基因组资源及明确命名的 Cactus 发布版本。项目提供组装、全基因组比对与保守性资源，适用于跨物种 MGA 和比较基因组研究。以官方项目和 CGL 发布目录为来源，版本差异保留在本条目中。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | Zoonomia；A comparative genomics multitool for scientific discovery and conservation |
| 维护方式 | 论文集合及其明确版本；不自动纳入整个下载服务器的新数据 |
| 发布机构或项目 | Zoonomia Consortium；Cactus / UCSC CGL |
| 版本 | Nature 2020 集合；下载表区分 2020v2 与 2020v2.1 |
| 集合标识 | DOI 10.1038/s41586-020-2876-6；241-mammalian-2020v2 |
| 物种与比较范围 | 240 种哺乳动物，包含 Homo sapiens；种间 |
| 数据性质 | 真实组装与计算推断的多基因组比对 |
| 规模与计数单位 | 项目 240 个物种；原研究 242 份组装；本次读取的 2020v2.genomes 有 241 个基因组名称，不能把这些数字视为同一版本的相同计数 |
| 格式与覆盖范围 | 全基因组组装；HAL、MAF、Newick、bigWig |
| 数据体积 | 目录显示 2020v2 HAL 805G、MAF 1.0T；2020v2.1 HAL 725G，为服务器显示值 |
| 原始集合或派生关系 | 2020v2.1 对猫和犬类等输入进行了更新；不可仅按相似文件名视为同一比对 |

## 适用研究

| 用途 | 依据类型 | 使用方式、来源或判断理由 |
| --- | --- | --- |
| MGA | 原研究 | Cactus 全基因组比对，跨物种序列同源性与保守性分析 |
| 比较基因组 | 后续研究 | 2023 年 Science 的哺乳动物进化约束研究 |
| Pangenome | 潜在用途 | 可作为跨物种图方法的输入来源；本条目未确认独立发布的通用 GFA 图 |

模拟对象与场景：不适用。

## 组装与质量

- **仓库组装级别**：未明确（多来源集合，尚未按 accession 逐条汇总 Chromosome、Scaffold、Contig 等级别）。
- **来源原始级别**：需在论文清单与对应组装数据库核定。
- **T2T 证据**：未确认适用于全体输入的 T2T 声明；不将其整体归为 T2T，也不把未核实写成确定非 T2T。
- **判定范围**：各发布版本的输入清单；项目物种数不能代替比对输入数。
- **质量与缺失**：各输入组装连续性与缺失不同；HAL 中的重建祖先不是新测序个体，亦不是可额外计入样本数的真实组装。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 项目数据主页与组装导航 | Zoonomia 论文集合 | 网页、关联组装入口 | [The data](https://zoonomiaproject.org/the-data/) | 公开；具体组装按清单选择 |
| 论文与补充材料 | 原始研究 | HTML、补充表 | [Nature 2020](https://www.nature.com/articles/s41586-020-2876-6) | 公开页面 |
| 版本与文件总清单 | CGL 发布目录，包含其他项目 | HTML | [CGL Cactus data](https://cgl.gi.ucsc.edu/data/cactus/) | 公开；只选本条目所列前缀 |
| 输入名称清单 | 2020v2；241 行 | 文本 | [2020v2.genomes](https://cgl.gi.ucsc.edu/data/cactus/241-mammalian-2020v2.genomes) | 公开；名称清单不是完整 accession/version 表 |
| 全基因组比对 | 2020v2 | HAL | [2020v2 HAL](https://cgl.gi.ucsc.edu/data/cactus/241-mammalian-2020v2.hal) | 公开目录已列出；大文件未下载 |
| 比对导出 | 2020v2 | MAF.gz | [2020v2 MAF](https://cgl.gi.ucsc.edu/data/cactus/241-mammalian-2020v2.maf.gz) | 公开目录已列出；同目录 v2b 文件不可静默替换 |
| 比对树 | 2020v2 | Newick | [2020v2.nh](https://cgl.gi.ucsc.edu/data/cactus/241-mammalian-2020v2.nh) | 公开目录已列出 |
| 人类坐标保守性分数 | 2020v2 | bigWig | [phyloP Homo sapiens](https://cgl.gi.ucsc.edu/data/cactus/241-mammalian-2020v2.phylop-Homo_sapiens.bigWig) | 公开目录已列出 |
| 更新版比对 | 2020v2.1 | HAL | [2020v2.1 HAL](https://cgl.gi.ucsc.edu/data/cactus/241-mammalian-2020v2.1.hal) | 公开目录已列出；不可与 v2 混用 |
| 更新说明 | 2020v2.1 | Markdown | [版本 README](https://cgl.gi.ucsc.edu/data/cactus/241-mammalian-2020v2.1.README.md) | 公开；说明猫和犬类更新 |

## 配套资源

| 资源 | 提供情况 | 内容与范围 |
| --- | --- | --- |
| 样本/组装清单 | 有 | 论文补充表、项目导航及版本 .genomes；后者只提供名称 |
| 注释与保守性 | 有关联资源 | 官方主页提供注释导航；下载表列人类坐标 phyloP |
| 泛基因组图 | 未明确 | HAL 是已有比对，不视为已发布的通用 GFA 文件 |
| 已有比对结果 | 有 | Cactus HAL 与 MAF |
| 独立真值 | 未明确 | Cactus 比对、祖先重建和保守性分数均为计算结果 |

**真值状态**：未明确。可比较结果一致性与覆盖度；不能自动把 Cactus 输出当作碱基层面真值。

## 使用注意

- 项目的 240 个物种、原始论文组装数、2020v2 输入名称数分别记录。更改下载版本时重新核定输入，而非沿用旧数量。
- 2020v2.1 README 明确描述一份新猫和五份新犬类相关更新；具体替换、增加及祖先重算按该说明解释，不据文件前缀推定输入总数。
- 配套 MAF 存在 v2、v2b 等导出；变体之间的详细差别尚未逐一核实，复现实验应固定完整文件名。
- 不把后续单物种 T2T 版本替换进旧 HAL 的输入并宣称完全对应；序列、坐标和注释需要版本匹配。

## 引用与核验

- **主论文**：Zoonomia Consortium. A comparative genomics multitool for scientific discovery and conservation. Nature (2020). [DOI](https://doi.org/10.1038/s41586-020-2876-6)。
- **比对方法**：Armstrong et al. Progressive Cactus is a multiple-genome aligner for the thousand-genome era. Nature (2020). [DOI](https://doi.org/10.1038/s41586-020-2871-y)。
- **后续研究**：Evolutionary constraint and innovation across hundreds of placental mammals. Science (2023). [DOI](https://doi.org/10.1126/science.abn3943)。
- **数据引用**：注明项目、完整 HAL/MAF 文件名、下载时所用版本及输入清单。
- **数据许可**：具体组装及派生文件条款未统一核实；公开访问不等于整套数据采用同一个开放许可。

| 检查对象 | 检查日期 | 入口核验结果 | 说明 |
| --- | --- | --- | --- |
| 官方项目数据页 | 2026-09-16 | 已读取 | 确认数据导航 |
| CGL 文件目录 | 2026-09-16 | HTTP 200，已读取文件名与显示大小 | HAL/MAF/bigWig 本体未请求 |
| 2020v2.genomes | 2026-09-16 | HTTP 200，241 行名称 | 仅读取元数据 |
| 2020v2.1 README | 2026-09-16 | HTTP 200，已读取更新说明 | 不等于验证更新版 HAL 内容 |

**文件内容验证**：未验证（未下载）。仅检查页面和小型元数据。

**尚未核实的信息**：逐组装 accession/version、级别统计、原始与各更新版本的完整映射、v2b 导出差异、各数据许可。

## 更新记录

- 2026-09-16：首次收录 Zoonomia 及具名 Cactus 版本入口。

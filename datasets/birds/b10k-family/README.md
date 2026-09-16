# B10K 鸟类科级比较基因组集合

[返回首页](../../../README.md) · [鸟类内容目录](../README.md) · [其他动物分类](../../../catalog/real/other-animals.md)

所属目录：[其他动物](../../../catalog/real/other-animals.md)。

## 简介

收录 Nature 2024 论文 **Complexity of avian evolution revealed by family-level genomes** 的 363 种鸟类研究集合。其组装和全基因组比对沿用 Nature 2020 的鸟类资源；2024 年另发布筛选后的序列比对、基因树、物种树及分析材料。此条目固定于这组论文资源，不代表不断扩展的整个 B10K 项目。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 维护方式 | 固定论文发布集；相关文件版本在本条目中区分 |
| 发布机构或项目 | B10K 团队；哥本哈根大学 ERDA、UCSC CGL 托管 |
| 版本 | 2020 组装/全基因组比对；2024 科级演化分析 |
| 集合标识 | DOI 10.1038/s41586-024-07323-1；ERDA DOI 10.17894/ucph.85624f66-c8e5-4b89-8e8a-fe984ca89e4a |
| 物种与比较范围 | Aves；种间，363 个物种、218 个科（2024 研究范围） |
| 数据性质 | 真实组装、已有比对及推断系统发育结果 |
| 规模与计数单位 | 363 个物种；2020 CGL 清单有 363 个基因组名称；2024 主分析含 63,430 个基因间区比对片段 |
| 格式与覆盖范围 | 全基因组 HAL/MAF；区域 FASTA 比对、Newick 树及分析表 |
| 数据体积 | CGL 目录显示 HAL 389G、修订 MAF 222G、修订单拷贝 MAF 217G；ERDA 为多个分析文件组成的独立归档 |
| 原始集合或派生关系 | 2024 研究复用 2020 组装/比对并筛选片段；不能称为 2024 年新生成 363 份组装 |

## 适用研究

| 用途 | 依据类型 | 使用方式、来源或判断理由 |
| --- | --- | --- |
| MGA | 原研究 | 大规模跨鸟类全基因组比对，提取不同类别的同源区域 |
| 系统发育与比较基因组 | 原研究 | 比较基因间区、外显子、内含子与 UCE 等位点的树和演化信号 |
| Pangenome | 潜在用途 | 可用于跨物种图方法研究；本次未确认配套通用 GFA 图发布 |

模拟对象与场景：不适用。

## 组装与质量

- **仓库组装级别**：未明确（多来源输入，未逐 accession 汇总各级别）。
- **来源原始级别**：逐条数据库记录待核实；不是统一 T2T 集合。
- **T2T 证据**：未确认针对该完整集合的 T2T 声明，不将染色体/支架级来源自动归为 T2T。
- **判定范围**：2020 输入组装及所用比对版本；2024 的片段筛选不会改变原始组装级别。
- **质量与限制**：物种间组装连续性、缺失与区域覆盖不同；不同片段的物种覆盖不一定达到 363。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 论文、物种和 accession 信息 | 2024 研究及 Supplementary Data | HTML、补充材料 | [Nature 2024](https://www.nature.com/articles/s41586-024-07323-1) | 公开页面；具体组装按补充表定位 |
| 原始组装发布依据 | 2020 鸟类集合 | HTML、补充材料及数据仓库链接 | [Nature 2020](https://www.nature.com/articles/s41586-020-2873-9) | 公开页面；未逐 accession 核验 |
| 全基因组发布目录 | 363-avian-2020 前缀 | 文件清单 | [CGL Cactus data](https://cgl.gi.ucsc.edu/data/cactus/) | 公开；同目录还包含其他项目 |
| 输入名称清单 | 2020，363 行 | 文本 | [363-avian-2020.genomes](https://cgl.gi.ucsc.edu/data/cactus/363-avian-2020.genomes) | 公开；不是完整 accession 表 |
| 全基因组比对 | 363-avian-2020 | HAL | [HAL](https://cgl.gi.ucsc.edu/data/cactus/363-avian-2020.hal) | 公开目录已列出；未下载 |
| 修订比对导出 | 目录日期 2024-06-28 | MAF.gz | [fix MAF](https://cgl.gi.ucsc.edu/data/cactus/363-avian-2020.fix.maf.gz) | 公开目录已列出；未下载 |
| 修订单拷贝导出 | 目录日期 2024-06-30 | MAF.gz | [fix single-copy MAF](https://cgl.gi.ucsc.edu/data/cactus/363-avian-2020.fix.single-copy.maf.gz) | 公开目录已列出；未下载 |
| 比对树 | 2020 | Newick | [363-avian-2020.nh](https://cgl.gi.ucsc.edu/data/cactus/363-avian-2020.nh) | 公开目录已列出 |
| 2024 研究数据归档 | 固定 DOI 记录 | FASTA 比对、Newick、压缩包、表格与脚本 | [ERDA DOI](https://doi.org/10.17894/ucph.85624f66-c8e5-4b89-8e8a-fe984ca89e4a) | 公开；页面逐文件访问 |
| 归档文件清单 | 与 DOI 落地记录一致 | JSON | [published-files.json](https://erda.ku.dk/archives/341f72708302f1d0c461ad616e783b86/published-files.json) | 公开 |
| 归档说明 | 2024 分析资源 | TXT | [README](https://erda.ku.dk/archives/341f72708302f1d0c461ad616e783b86/B10K/data_upload/README.txt) | 公开；含目录解释和作者提供的访问入口 |

## 配套资源

| 资源 | 提供情况 | 内容与范围 |
| --- | --- | --- |
| 物种和组装清单 | 有 | 论文补充材料与 CGL 名称清单；需进一步匹配 accession/version |
| 区域注释与分析表 | 有 | ERDA 位点特征、GC 含量、模型分析等；不等同于完整全物种基因注释包 |
| 泛基因组图 | 未明确 | 未确认独立图文件 |
| 已有比对 | 有 | 全基因组 HAL、MAF，以及筛选后的区域比对 |
| 基因树与物种树 | 有 | ERDA 包含基因树、物种树、时间树、子集与多分叉测试结果 |
| 独立真值 | 未明确 | 树和比对均由分析推断，不是已知演化历史 |

**真值状态**：未明确。文件中的 gene trees / GTs 指基因树，不应解读成 ground truth。

## 使用注意

- 2020 集合与 2024 分析属于相关但不同层次的发布；保留两篇论文的引用和各自版本。
- 63,430 是主分析基因间区片段数，不能写作物种数或组装数。ERDA 还含 94K、80K 等子集及其他区域类型，应按 README 选择。
- CGL 修订 MAF 的目录时间晚于 2024 年 4 月论文发表，不宣称它们就是论文当时的逐字节输入。
- HAL 包括重复序列与祖先表示；单拷贝 MAF 是另一个导出范围，不可认为覆盖范围相同。
- 复现实验需同时固定区域筛选、物种名称映射、参考坐标和树处理步骤；下载表中的 README 仅作为说明，本仓库不运行其命令。

## 引用与核验

- **研究论文**：Stiller, J. et al. Complexity of avian evolution revealed by family-level genomes. Nature 629, 851–860 (2024). [DOI](https://doi.org/10.1038/s41586-024-07323-1)。
- **组装来源**：Feng, S. et al. Dense sampling of bird diversity increases power of comparative genomics. Nature 587, 252–257 (2020). [DOI](https://doi.org/10.1038/s41586-020-2873-9)。
- **数据引用**：引用 ERDA 固定 DOI，并注明使用的 CGL 文件名、区域子集和组装版本。
- **数据许可**：各来源的具体再分发许可未统一确认；不以论文开放许可代替数据条款。

| 检查对象 | 检查日期 | 入口核验结果 | 说明 |
| --- | --- | --- | --- |
| 2024 论文 | 2026-09-16 | 已读取数据可用性说明 | 组装和全基因组比对复用 2020 资源 |
| CGL 文件目录 | 2026-09-16 | HTTP 200，文件名与显示大小可读 | 未请求 HAL/MAF 本体 |
| 363-avian-2020.genomes | 2026-09-16 | HTTP 200，363 行名称 | 小型元数据 |
| ERDA DOI、文件清单、README | 2026-09-16 | HTTP 200，已读取 | 确认区域比对、树和分析目录；未下载压缩包 |

**文件内容验证**：未验证（未下载）。仅检查页面和小型元数据。

**尚未核实的信息**：逐组装 accession/version 和级别、全部序列下载入口、修订 MAF 与论文输入的精确差异、各数据许可。

## 更新记录

- 2026-09-16：首次收录 363 种鸟类论文集合，分列 2020 全基因组资源和 2024 分析归档。

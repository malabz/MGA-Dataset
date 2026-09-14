# Alignathon 模拟灵长类与哺乳动物基准集

[返回首页](../../../README.md) · [数据目录](../../../catalog/README.md) · [模拟数据目录](../../../catalog/simulated/README.md) · [模拟数据集](../README.md)

所属目录：[模拟数据与模拟基准集](../../../catalog/simulated/README.md)。

## 简介

Alignathon 是一次全基因组多序列比对评测。本条目收录其中两个正式模拟场景：模拟灵长类（Primates）和模拟哺乳动物（Mammals）。二者均由 EVOLVER 从人类染色体子集构成的根基因组向前模拟，发布叶基因组序列、区域注释、完整模拟历史形成的 MAF 真值，以及用于复现实验的评测代码。

完整 Alignathon 还包含一个用于流程检查的 simulation test set 和一个由 20 个真实果蝇基因组组成的评测集。本条目仅收录论文用于正式模拟评测的 Primates 与 Mammals，不把测试包或真实果蝇数据混入当前规模和真值描述。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 正式名称 | Alignathon simulated primate and mammal datasets |
| 维护方式 | 固定发布基准集 |
| 发布机构或项目 | Alignathon；现由 UCSC Computational Genomics Lab（CGL）提供数据镜像 |
| 版本或发布日期 | 初始数据于 2011 年 12 月发布；论文发表于 2014 年；当前下载脚本建立 `version_3` 标记，但项目未给出独立的语义化版本号 |
| 集合标识 / accession | 无独立 accession；论文 DOI：`10.1101/gr.174920.114` |
| 模拟对象 | Primates：`simChimp`、`simGorilla`、`simHuman`、`simOrang`；Mammals：`simCow`、`simDog`、`simHuman`、`simMouse`、`simRat` |
| 比较范围 | 两个独立的模拟种间场景；Primates 为较近分化，Mammals 为较长进化距离 |
| 数据性质 | 模拟全基因组数据与已知比对真值 |
| 规模与计数单位 | 2 个场景；Primates 4 个叶基因组，Mammals 5 个叶基因组；共 9 个场景内叶基因组实例 |
| 格式与覆盖范围 | 叶序列为 FASTA；注释为 BED，可选 GFF；真值为 MAF；各叶基因组约 185–199 Mb |
| 数据体积 | 分文件体积见下载入口；数值采用官方页面的近似标注 |
| 原始集合或派生关系 | 属于 Alignathon 全集；不包含 simulation test set、20-genome real fly set 或参评工具提交结果 |

`simHuman` 在两个场景中分别由不同的模拟树生成，因此“9 个场景内叶基因组实例”不能写成 9 个独立物种。

## 场景与生成方式

两个场景都从人类参考基因组第 20、21、22 号染色体的子集开始。根基因组先经过总距离为 1.0 neutral substitutions per site 的 burn-in，所得 `ancestor` 再沿各自系统发育树演化。模拟保留了叶节点、内部节点和根之间的碱基对应关系，因此可以直接把预测 MAF 与模拟真值比较。

| 场景 | 叶基因组 | 单个叶基因组总长度 | 系统发育范围与难度 |
| --- | --- | --- | --- |
| Primates | 4 | 185,136,279–185,338,662 bp | 模拟人、黑猩猩、大猩猩和猩猩关系；分化距离较短，官方描述为相对简单 |
| Mammals | 5 | 190,795,996–198,921,416 bp | 模拟人、鼠、大鼠、牛和犬关系；分化距离更长，官方描述为两个模拟集中的较难场景 |

模拟参数元数据仍由 CGL 镜像提供：[Primates XML](https://cgl.gi.ucsc.edu/data/alignathon/data/simulationInfoPrimates.xml)、[Mammals XML](https://cgl.gi.ucsc.edu/data/alignathon/data/simulationInfoMammals.xml)和[burn-in XML](https://cgl.gi.ucsc.edu/data/alignathon/data/simulationInfoBurnin.xml)。生成根输入和控制 EVOLVER 的代码分别见 [`evolverInfileGeneration`](https://github.com/dentearl/evolverInfileGeneration) 与 [`evolverSimControl`](https://github.com/dentearl/evolverSimControl)。

## 适用研究

| 用途 | 依据类型 | 使用方式、来源或判断理由 |
| --- | --- | --- |
| MGA 准确性评测 | 原研究 | 将工具输出的 MAF 与模拟真值的 alignment relation 比较，计算 precision、recall 和 F-score |
| 功能区域分层评测 | 原研究 | 使用随包发布的基因、重复和中性区域注释，比较不同区域中的比对质量 |
| 重复与拷贝数评测 | 原研究 | 评估工具恢复 duplicative homologies 和 copy-number coverage 的能力 |
| 新版全基因组比对工具复评 | 后续研究 | Progressive Cactus 论文重新运行两个 Alignathon 模拟集，并沿用其分析流程比较结果 |

本条目不标记 Pangenome 已有评测用途。模拟序列可以被转换为图或其他表示，但这属于潜在用途，Alignathon 原始基准评估的是全基因组多序列比对。

## 组装与质量

- **仓库组装级别**：不适用。叶序列是模拟产生的基因组，不按真实组装的 T2T、Chromosome、Scaffold 或 Contig 级别分类。
- **来源原始级别**：不适用。
- **T2T 证据**：不适用；模拟序列不能因为由染色体子集生成而标为 T2T。
- **判定对象与范围**：Primates 与 Mammals 的全部叶序列及其对应模拟真值。
- **来源依据**：Alignathon 论文、CGL 数据镜像页面、模拟参数 XML 和官方评测仓库。
- **已公布质量信息**：模拟真值来自完整生成历史；发布方同时提供含旁系同源关系和移除 paralogous blocks 的真值版本。
- **已知限制**：模拟模型不能覆盖真实基因组演化的全部复杂性；结果只能解释为相对于该 EVOLVER 模型和给定真值定义的准确性。

## 下载入口

### 总入口与批量脚本

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| CGL Alignathon 镜像 | 整个历史项目镜像 | HTML | [项目主页](https://cgl.gi.ucsc.edu/data/alignathon/) | 公开 |
| Primates 数据说明 | 正式模拟灵长类场景 | HTML | [场景与文件说明](https://cgl.gi.ucsc.edu/data/alignathon/set_primate.html) | 公开 |
| Mammals 数据说明 | 正式模拟哺乳动物场景 | HTML | [场景与文件说明](https://cgl.gi.ucsc.edu/data/alignathon/set_mammal.html) | 公开 |
| Primates 批量下载脚本 | 当前 CGL 镜像包结构 | Shell | [`downloadPrimates.sh`](https://cgl.gi.ucsc.edu/data/alignathon/downloadPrimates.sh) | 公开；运行会下载数据，本仓库未运行 |
| Mammals 批量下载脚本 | 当前 CGL 镜像包结构 | Shell | [`downloadMammals.sh`](https://cgl.gi.ucsc.edu/data/alignathon/downloadMammals.sh) | 公开；运行会下载数据，本仓库未运行 |

### Primates 文件

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 叶基因组序列 | 4 个叶基因组；官方标注约 229 MB | `tar.gz` 内含 FASTA | [`simPrimates.seqs.tar.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simPrimates.seqs.tar.gz) | 公开 |
| 区域注释 | 官方标注约 182 MB | `tar.gz` 内含 BED | [`simPrimates.annots.tar.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simPrimates.annots.tar.gz) | 公开 |
| 可选区域注释 | 官方标注约 162 MB | `tar.gz` 内含 GFF | [`simPrimates.annots.gff.tar.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simPrimates.annots.gff.tar.gz) | 公开 |
| MRCA 真值 | `ancestor`；官方标注约 143 MB | `maf.gz` | [`simPrimates.ancestor.maf.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simPrimates.ancestor.maf.gz) | 公开 |
| Root 真值 | `burnin`；官方标注约 581 MB | `maf.gz` | [`simPrimates.burnin.maf.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simPrimates.burnin.maf.gz) | 公开 |
| 去旁系同源真值 | MRCA 与 root 两份 MAF；官方标注约 472 MB | `tar.gz` 内含 MAF | [`simPrimates.noparalogyMafs.tar.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simPrimates.noparalogyMafs.tar.gz) | 公开 |

### Mammals 文件

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 叶基因组序列 | 5 个叶基因组；官方标注约 303 MB | `tar.gz` 内含 FASTA | [`simMammals.seqs.tar.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simMammals.seqs.tar.gz) | 公开 |
| 区域注释 | 官方标注约 203 MB | `tar.gz` 内含 BED | [`simMammals.annots.tar.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simMammals.annots.tar.gz) | 公开 |
| 可选区域注释 | 官方标注约 196 MB | `tar.gz` 内含 GFF | [`simMammals.annots.gff.tar.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simMammals.annots.gff.tar.gz) | 公开 |
| MRCA 真值 | `ancestor`；官方标注约 652 MB | `maf.gz` | [`simMammals.ancestor.maf.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simMammals.ancestor.maf.gz) | 公开 |
| Root 真值 | `burnin`；官方标注约 1.2 GB | `maf.gz` | [`simMammals.burnin.maf.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simMammals.burnin.maf.gz) | 公开 |
| 去旁系同源真值 | MRCA 与 root 两份 MAF；官方标注约 1.4 GB | `tar.gz` 内含 MAF | [`simMammals.noparalogyMafs.tar.gz`](https://cgl.gi.ucsc.edu/data/alignathon/data/simMammals.noparalogyMafs.tar.gz) | 公开 |

### 评测与生成代码

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| Alignathon 分析流程 | Primates、Mammals、Fly 与 test registries | Git 仓库 | [`mwgAlignAnalysis`](https://github.com/dentearl/mwgAlignAnalysis) | 公开 |
| MAF 比较工具 | 评测依赖 | Git 仓库 | [`mafTools`](https://github.com/dentearl/mafTools) | 公开 |
| 模拟输入生成 | EVOLVER 输入构建 | Git 仓库 | [`evolverInfileGeneration`](https://github.com/dentearl/evolverInfileGeneration) | 公开 |
| 模拟流程控制 | EVOLVER 分支模拟 | Git 仓库 | [`evolverSimControl`](https://github.com/dentearl/evolverSimControl) | 公开 |

## 官方校验值

以下 MD5 来自当前 CGL 批量下载脚本，用于在实际下载后识别脚本所对应的文件版本。本仓库没有下载文件，也没有自行重算校验值。

| 场景 | 文件 | 官方脚本中的 MD5 |
| --- | --- | --- |
| Primates | `simPrimates.annots.tar.gz` | `7d337b5e4f7c6eeb8eeeda95c2c21271` |
| Primates | `simPrimates.seqs.tar.gz` | `d817e8739c10a0ddfcbe37200545b7f9` |
| Primates | `simPrimates.ancestor.maf.gz` | `1e2417d2ae8b4cf2743d5e740b7c5ed3` |
| Primates | `simPrimates.burnin.maf.gz` | `4fb72a9f14cf016c0d7b906d25e4731f` |
| Primates | `simPrimates.noparalogyMafs.tar.gz` | `3fc4fcb8fa64958f2a9d655b992387f7` |
| Mammals | `simMammals.annots.tar.gz` | `bddd7ab44c51b45f79380f190fd7dfa0` |
| Mammals | `simMammals.seqs.tar.gz` | `a554a2151b3bbe269c2dcf6e07030ab7` |
| Mammals | `simMammals.ancestor.maf.gz` | `4bab2832a972a26a9a43af150096295e` |
| Mammals | `simMammals.burnin.maf.gz` | `0a4c595644a806e7342ec3be62893f39` |
| Mammals | `simMammals.noparalogyMafs.tar.gz` | `bffc18321f937a1eac183c946049d190` |

可选 GFF 注释没有被当前批量脚本下载，其页面校验值不并入这张脚本校验表。

## 配套资源与真值

| 资源 | 提供情况 | 内容、版本对应与下载表中的资源名称 |
| --- | --- | --- |
| 样本清单 | 已提供 | 两个场景页面、树和分析仓库 registry 给出全部叶基因组名称 |
| 注释 | 已提供 | BED 注释包；另有可选 GFF 包，覆盖 genes、repeats、neutral 等区域类型 |
| 泛基因组图 | 未提供 | 原始发布不包含图泛基因组 |
| 已有比对结果 | 已提供但本条目未逐项列出 | Alignathon 参评提交可从项目镜像下载；它们是待评预测结果，不是真值 |
| 真值 | 已提供 | `ancestor`、`burnin` 和去旁系同源 MAF |

- **真值状态**：有。
- **真值类型、来源与覆盖**：EVOLVER 完整模拟历史导出的碱基同源关系；覆盖两个场景的叶节点、内部节点、MRCA，root 版本还覆盖 burn-in 根。去旁系同源版本用于只评估 orthologous blocks 的情形。
- **可评测对象与限制**：预测 MAF 的 alignment relation，可计算 precision、recall、F-score，并按基因、重复和中性区域分层。真值只适用于对应场景和对应版本，不能用于真实数据或其他模拟参数。

## 使用注意

- **起始参考版本存在文字差异**：2014 年论文写作 `hg19/GRCh37` 的第 20、21、22 号染色体子集；CGL 场景页面写作 `hg18` 或 `hg18 (GRCh36)`。当前核验无法消除这一差异，复现实验时应依据实际包内 README、序列标识和模拟输入，而不能仅凭网页标签假定坐标版本。
- **去旁系同源文件扩展名**：场景网页把链接写成 `simPrimates.noparalogyMafs.maf.gz` 和 `simMammals.noparalogyMafs.maf.gz`，这两个地址在 2026-09-14 返回 404；当前批量脚本实际使用 `.tar.gz`，且对应地址可访问。本条目已链接可访问的 `.tar.gz` 文件。
- **旧主页已经迁移**：论文中的 `http://compbio.soe.ucsc.edu/alignathon/` 当前会跳转到 UCSC 工程学院通用页面。应使用本条目列出的 `cgl.gi.ucsc.edu/data/alignathon/` 镜像。
- **评测代码较旧**：`mwgAlignAnalysis` README 要求 Linux 和 Python 2.7。直接复现实验前需要评估旧依赖的可安装性，本仓库未运行代码。
- **真值选择**：`ancestor`、`burnin` 与 `noparalogy` 回答的评测问题不同；报告结果时必须写明使用哪个真值，不能混合排名。
- **参评结果不等于真值**：项目发布的各工具提交 MAF 是预测结果，只能与模拟真值比较，不能作为新的标准答案。

## 引用与核验

- **论文**：Earl, D. et al. *Alignathon: a competitive assessment of whole-genome alignment methods*. Genome Research 24, 2077–2089 (2014). [DOI: 10.1101/gr.174920.114](https://doi.org/10.1101/gr.174920.114)；[PMC 全文](https://pmc.ncbi.nlm.nih.gov/articles/PMC4248324/)。
- **后续使用示例**：Armstrong, J. et al. *Progressive Cactus is a multiple-genome aligner for the thousand-genome era*. Nature 587, 246–251 (2020). [论文页面](https://www.nature.com/articles/s41586-020-2871-y)。
- **数据引用**：数据镜像未提供独立 DOI；使用时至少引用 Alignathon 论文，并记录 Primates 或 Mammals、真值类型、文件名和官方校验值。
- **数据许可**：CGL 数据镜像页面未明确标注模拟数据文件许可，使用前应核对包内 README 或联系发布方。`mwgAlignAnalysis` 代码仓库含宽松软件许可，但该许可不能自动套用于数据文件。

| 检查对象（与下载表对应） | 检查日期 | 入口核验结果 | 说明 |
| --- | --- | --- | --- |
| CGL 项目主页、两个场景页和两个批量脚本 | 2026-09-14 | 可访问 | HTTPS 返回成功；脚本文本与直接文件名已对照 |
| Primates 六个直接数据入口 | 2026-09-14 | 可访问 | 仅检查 HTTP 响应和内容类型，没有下载文件 |
| Mammals 六个直接数据入口 | 2026-09-14 | 可访问 | 仅检查 HTTP 响应和内容类型，没有下载文件 |
| 四个 GitHub 代码仓库 | 2026-09-14 | 可访问 | 仓库页面可访问；未安装或运行代码 |
| 论文 DOI 与 PMC 全文 | 2026-09-14 | 可访问 | DOI 可解析；PMC 提供开放全文 |
| 旧 `compbio.soe.ucsc.edu` 项目主页 | 2026-09-14 | 已失效为数据入口 | 跳转到 UCSC 工程学院通用页面 |
| 场景页中的两个 `.noparalogyMafs.maf.gz` 地址 | 2026-09-14 | 失效 | 返回 404；批量脚本中的 `.tar.gz` 地址可访问 |

**文件内容验证**：未验证（未下载）。官方 MD5 仅转录自下载脚本，没有在本地重算。

**尚未核实的信息**：模拟数据文件的明确许可；下载包内 README 对 hg18 与 hg19/GRCh37 文字差异的解释；所有旧评测依赖在现代环境中的可运行性。

## 更新记录

- 2026-09-14：首次收录正式 Primates 与 Mammals 模拟场景；核验 CGL 迁移镜像、直接文件、批量脚本、代码仓库和论文入口；未下载任何数据文件。

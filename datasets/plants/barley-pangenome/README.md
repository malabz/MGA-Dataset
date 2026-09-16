# 大麦泛基因组 v2

[返回首页](../../../README.md) · [植物内容目录](../README.md) · [植物分类](../../../catalog/real/plants.md)

所属目录：[植物](../../../catalog/real/plants.md)。

## 简介

收录 Jayakodi 等发表于 Nature（2024）的 **Structural variation in the pangenome of wild and domesticated barley** 发布集合，即 Barley PanGenome v2。以 76 份野生与栽培大麦组装为核心，配套基因注释、结构变异和群体分析资源。此条目对应明确的论文发布集，不代表所有大麦数据库内容。

## 基本信息

| 字段 | 内容 |
| --- | --- |
| 维护方式 | 固定发布集；后续版本在本条目注明 |
| 发布机构或项目 | 大麦泛基因组协作团队；IPK、GrainGenes 等托管 |
| 版本 | Barley PanGenome v2；Nature 2024 |
| 集合标识 | 论文 DOI 10.1038/s41586-024-08187-1；分析数据 DOI 10.5447/ipk/2024/9 |
| 物种与比较范围 | Hordeum vulgare 及野生大麦；野生—栽培比较，分类命名以各材料元数据为准 |
| 数据性质 | 真实组装及派生分析 |
| 规模与计数单位 | 76 份组装；另有 1,315 份材料的短读长群体数据，不计为新增组装 |
| 格式与覆盖范围 | 全基因组序列、基因注释、变异矩阵及结构变异分析文件；各包格式以发布清单为准 |
| 数据体积 | 组装总量未明确；PGP 分析记录列出约 3 GB 文件，不代表全套序列体积 |
| 原始集合或派生关系 | v2 的 76 份集合；不与较早的大麦泛基因组版本混算 |

## 适用研究

| 用途 | 依据类型 | 使用方式、来源或判断理由 |
| --- | --- | --- |
| Pangenome | 原研究 | 野生与栽培材料的基因组结构变异、基因内容及群体多样性分析 |
| MGA | 潜在用途 | 76 份组装可用于大规模重复序列丰富的植物基因组比较；论文发布的成对变异结果不等同于多基因组比对真值 |

模拟对象与场景：不适用。

## 组装与质量

- **仓库组装级别**：76 份 Chromosome，依据论文的 chromosome-scale 组装说明。
- **来源原始级别**：论文称染色体级；各数据库 accession 对应级别尚未逐条核定。
- **T2T 证据**：未确认覆盖全部 76 份组装的 T2T 声明，因此不归为 T2T；染色体级不能推导为无缺口。
- **判定对象与范围**：论文 v2 组装集合；单份组装版本与质量指标以 Supplementary Table 1 为准。
- **已公布质量信息**：论文提供组装与材料信息；本次未逐条提取 contiguity、完整性等指标。
- **范围限制**：不同材料的缺口、重复区域解析能力和结构变异可比性需按具体版本判断。

## 下载入口

| 资源 | 版本或范围 | 格式 | 入口 | 访问条件 |
| --- | --- | --- | --- | --- |
| 论文与材料清单 | 2024；Supplementary Table 1 | HTML、补充表 | [Nature](https://www.nature.com/articles/s41586-024-08187-1) | 公开页面 |
| 组装与基因注释 | v2，76 份集合 | 序列与注释文件；具体后缀见清单 | [IPK Galaxy Library](https://galaxy-web.ipk-gatersleben.de/libraries/folders/Fd071e794759ab192) | 公开入口；需要 JavaScript |
| 组装浏览与资源导航 | Barley PanGenome v2 | 网页及关联文件 | [GrainGenes Pangenome](https://graingenes.org/GG3/pangenome) | 公开 |
| 长读长测序项目 | 组装相关项目 | 原始测序；按样本选择 | [PRJEB40587](https://www.ebi.ac.uk/ena/browser/view/PRJEB40587)、[PRJEB57567](https://www.ebi.ac.uk/ena/browser/view/PRJEB57567)、[PRJEB58554](https://www.ebi.ac.uk/ena/browser/view/PRJEB58554) | 论文列出的公开项目；本次未逐文件核验 |
| 群体短读长数据 | 1,315 份材料 | 原始测序 | [PRJEB53924](https://www.ebi.ac.uk/ena/browser/view/PRJEB53924) | 论文列出的公开项目；本次未逐文件核验 |
| SNP / indel 矩阵 | 群体分析 | 变异文件；见项目清单 | [PRJEB70778](https://www.ebi.ac.uk/ena/browser/view/PRJEB70778) | 论文所列 EVA 关联 accession；本次未逐文件核验 |
| 结构变异与分析数据 | 固定记录 2024/9 | Assemblytics、SyRI 输出、LD 与 k-mer 文件 | [PGP 数据记录](https://doi.org/10.5447/ipk/2024/9) | 公开；该记录标注 CC0 1.0 |

## 配套资源

| 资源 | 提供情况 | 内容与范围 |
| --- | --- | --- |
| 材料清单 | 有 | 论文 Supplementary Table 1；需据此匹配样本与 accession |
| 基因注释 | 有 | 与 v2 组装配套，IPK 与 GrainGenes 入口 |
| 泛基因组图 | 文件入口未明确 | 论文有图分析；不能据分析方法推断已有可下载 GFA |
| 已有比对/变异结果 | 有 | 相对于 Morex v3 的结构变异分析及 SyRI、Assemblytics 输出 |
| 独立真值 | 未明确 | 未确认覆盖集合的独立碱基比对或结构变异真值 |

**真值状态**：未明确。已有结构变异调用不直接用于宣称算法准确率。

## 使用注意

- 76 份组装与 1,315 份短读长材料是不同层次的资源，不能相加为组装数。
- 配套变异的参考坐标涉及 Morex v3，使用前需匹配参考版本、染色体名称和所选样本。
- Galaxy 返回可访问页面不代表已核实文件列表；本次只确认应用入口，未验证所有序列文件的直接下载。
- PGP 记录标题为 *Adaptive diversification through structural variation in barley*，与论文标题不同；按论文 Data availability 关联收录。

## 引用与核验

- **论文**：Jayakodi, M. et al. Structural variation in the pangenome of wild and domesticated barley. Nature 636, 654–662 (2024). [DOI](https://doi.org/10.1038/s41586-024-08187-1)。
- **数据引用**：注明 Barley PanGenome v2、所选材料及 accession 版本；分析数据引用 DOI 10.5447/ipk/2024/9。
- **数据许可**：PGP 分析记录标注 CC0 1.0；其余资源的具体许可未逐一确认，不将该许可扩大到所有组装、测序或注释。

| 检查对象 | 检查日期 | 入口核验结果 | 说明 |
| --- | --- | --- | --- |
| Nature、GrainGenes | 2026-09-16 | 已读取公开说明 | 确认论文范围和 v2 导航 |
| IPK Galaxy | 2026-09-16 | HTTP 200 | 返回 JavaScript 应用页，文件清单未核实 |
| PGP DOI | 2026-09-16 | HTTP 200；已读取清单 | 确认结构变异分析包和记录许可 |
| ENA 项目 | 2026-09-16 | 依据论文收录，未逐文件检查 | 不宣称所有文件均已验证可下载 |

**文件内容验证**：未验证（未下载）。

**尚未核实的信息**：每份组装 accession/version 与原始级别、全部序列文件的直接访问条件、各资源许可、可下载图文件。

## 更新记录

- 2026-09-16：首次收录 v2 论文集合及已确认的组装、注释和分析资源入口。

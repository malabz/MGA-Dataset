# 灵长目集合核验记录

[返回数据集详情](README.md) · [返回首页](../../README.md)

## 2026-09-14 初始批次

输入为[初始清单快照](sources/2026-09-14-initial.tsv)中的 72 个带版本 accession。使用 NCBI Datasets v2 的 `/genome/accession/{accessions}/dataset_report` 接口批量查询，仅读取元数据。本节只对应初始批次，后续新增组装另记核验日期和范围。

返回 72 条记录，逐项按完整 accession 匹配，无缺失或重复；72 条均为 current，current_accession 与输入版本一致。此状态仅代表核验日期，不保证未来状态。

## 差异

| accession | 原清单字段 | NCBI 字段 | 处理 |
| --- | --- | --- | --- |
| GCA_029281585.3 | Gorilla gorilla | Gorilla gorilla gorilla | TSV 保留原学名，详情注明亚种名称差异 |
| GCA_049350105.2 | Chromosome | Complete Genome | 保留来源和 NCBI 级别；仓库展示级别经项目证据核对后标为 T2T |
| GCA_963573965.1 | Chiropotes israelita | Chiropotes chiropotes | TSV 保留原学名，详情注明名称差异；分类学解释待核实 |

其余 69 条的学名和组装级别与清单一致。以下表格保留本次返回的关键字段；科、属和常用名未在本轮 API 对照范围内。

## 逐条核验

| accession 与元数据来源 | NCBI 学名 | 组装名称 | 组装级别 | 状态 |
| --- | --- | --- | --- | --- |
| [GCA_000001405.29](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_000001405.29/dataset_report) | Homo sapiens | GRCh38.p14 | Chromosome | current |
| [GCF_028858775.2](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_028858775.2/dataset_report) | Pan troglodytes | NHGRI_mPanTro3-v2.1_pri | Chromosome | current |
| [GCA_029281585.3](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_029281585.3/dataset_report) | Gorilla gorilla gorilla | NHGRI_mGorGor1-v2.1_pri | Chromosome | current |
| [GCF_028885655.2](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_028885655.2/dataset_report) | Pongo abelii | NHGRI_mPonAbe1-v2.1_pri | Chromosome | current |
| [GCF_028878055.3](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_028878055.3/dataset_report) | Symphalangus syndactylus | NHGRI_mSymSyn1-v2.1_pri | Chromosome | current |
| [GCA_047372625.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_047372625.1/dataset_report) | Hoolock leuconedys | UCONN_HLeu1 | Chromosome | current |
| [GCA_021498465.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_021498465.1/dataset_report) | Hylobates pileatus | ASM2149846v1 | Chromosome | current |
| [GCA_040113105.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_040113105.1/dataset_report) | Nomascus leucogenys | ASM4011310v1 | Chromosome | current |
| [GCA_023783455.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_023783455.1/dataset_report) | Erythrocebus patas | ASM2378345v1 | Contig | current |
| [GCA_047676025.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_047676025.1/dataset_report) | Chlorocebus sabaeus | mChlSab1.0.hap2 | Chromosome | current |
| [GCA_014849445.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_014849445.1/dataset_report) | Cercopithecus mona | KIZ_CMon_1.0 | Scaffold | current |
| [GCA_963574245.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963574245.1/dataset_report) | Allenopithecus nigroviridis | PGDP_AllNig | Scaffold | current |
| [GCA_028551445.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_028551445.1/dataset_report) | Miopithecus talapoin | Miopithecus_talapoin_HiC | Chromosome | current |
| [GCA_963574325.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963574325.1/dataset_report) | Allochrocebus lhoesti | PGDP_AllLho | Scaffold | current |
| [GCA_049350105.2](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_049350105.2/dataset_report) | Macaca mulatta | T2T-MMU8v2.0 | Complete Genome | current |
| [GCA_008728515.2](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_008728515.2/dataset_report) | Papio anubis | Panubis1.1 | Chromosome | current |
| [GCA_023783235.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_023783235.1/dataset_report) | Lophocebus aterrimus | ASM2378323v1 | Contig | current |
| [GCA_003255815.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_003255815.1/dataset_report) | Theropithecus gelada | Tgel_1.0 | Chromosome | current |
| [GCA_000955945.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_000955945.1/dataset_report) | Cercocebus atys | Caty_1.0 | Scaffold | current |
| [GCA_023783495.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_023783495.1/dataset_report) | Mandrillus leucophaeus | ASM2378349v1 | Scaffold | current |
| [GCA_030247045.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_030247045.1/dataset_report) | Colobus guereza | ASM3024704v1 | Chromosome | current |
| [GCF_002776525.5](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_002776525.5/dataset_report) | Piliocolobus tephrosceles | ASM277652v5 | Chromosome | current |
| [GCA_047655245.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_047655245.1/dataset_report) | Pygathrix nigripes | ASM4765524v1 | Chromosome | current |
| [GCA_047655295.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_047655295.1/dataset_report) | Semnopithecus entellus | SemEnt | Contig | current |
| [GCA_054345695.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_054345695.1/dataset_report) | Trachypithecus shortridgei | ASM5434569v1 | Scaffold | current |
| [GCA_963575215.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963575215.1/dataset_report) | Presbytis melalophos mitrata | PGDP_PreMit | Scaffold | current |
| [GCA_007565055.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_007565055.1/dataset_report) | Rhinopithecus roxellana | ASM756505v1 | Chromosome | current |
| [GCA_000772465.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_000772465.1/dataset_report) | Nasalis larvatus | Charlie1.0 | Chromosome | current |
| [GCA_047496735.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_047496735.1/dataset_report) | Simias concolor | ASM4749673v1 | Scaffold | current |
| [GCA_030222135.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_030222135.1/dataset_report) | Aotus nancymaae | 86718_ANA_hifiasm-v0.15.2.pri | Contig | current |
| [GCA_004027835.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_004027835.1/dataset_report) | Alouatta palliata | AloPal_v1_BIUU | Scaffold | current |
| [GCA_916098195.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_916098195.1/dataset_report) | Ateles hybridus | ORGONE_01 | Scaffold | current |
| [GCA_963574225.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963574225.1/dataset_report) | Lagothrix lagotricha | PGDP_LagLag | Scaffold | current |
| [GCA_047496155.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_047496155.1/dataset_report) | Brachyteles arachnoides | ASM4749615v1 | Contig | current |
| [GCA_963573925.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963573925.1/dataset_report) | Callimico goeldii | PGDP_CalGoe | Scaffold | current |
| [GCF_049354715.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_049354715.1/dataset_report) | Callithrix jacchus | calJac240_pri | Chromosome | current |
| [GCA_963575025.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963575025.1/dataset_report) | Cebuella niveiventris | PGDP_CebNiv | Scaffold | current |
| [GCA_054824955.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_054824955.1/dataset_report) | Leontopithecus rosalia | mLeoRos1.hap2 | Chromosome | current |
| [GCA_963573565.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963573565.1/dataset_report) | Mico argentatus | PGDP_MicSch | Scaffold | current |
| [GCA_031835075.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_031835075.1/dataset_report) | Saguinus oedipus | ASM3183507v1 | Chromosome | current |
| [GCA_023783575.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_023783575.1/dataset_report) | Cebus albifrons | ASM2378357v1 | Contig | current |
| [GCA_963575265.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963575265.1/dataset_report) | Leontocebus nigricollis | PGDP_LeoNig | Scaffold | current |
| [GCF_048565385.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_048565385.1/dataset_report) | Saimiri boliviensis | mSaiBol1.pri | Chromosome | current |
| [GCA_022120495.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_022120495.1/dataset_report) | Sapajus apella | Sape_Mango_1.1 | Scaffold | current |
| [GCA_963573425.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963573425.1/dataset_report) | Cacajao ayresi | PGDP_CacAyr | Scaffold | current |
| [GCA_963574535.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963574535.1/dataset_report) | Cheracebus lugens | PGDP_CheLug | Scaffold | current |
| [GCA_963573965.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963573965.1/dataset_report) | Chiropotes chiropotes | PGDP_ChiIsr | Scaffold | current |
| [GCA_028551515.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_028551515.1/dataset_report) | Pithecia pithecia | Pithecia_pithecia_HiC | Chromosome | current |
| [GCA_040437455.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_040437455.1/dataset_report) | Plecturocebus cupreus | PleCup_hybrid | Chromosome | current |
| [GCA_963574405.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963574405.1/dataset_report) | Tarsius lariang | PGDP_TarLar | Scaffold | current |
| [GCA_027257055.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_027257055.1/dataset_report) | Cephalopachus bancanus | ASM2725705v1 | Contig | current |
| [GCF_000164805.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_000164805.1/dataset_report) | Carlito syrichta | Tarsius_syrichta-2.0.1 | Scaffold | current |
| [GCA_044048945.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_044048945.1/dataset_report) | Daubentonia madagascariensis | DMad_hybrid | Scaffold | current |
| [GCA_008086735.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_008086735.1/dataset_report) | Cheirogaleus medius | ASM808673v1 | Scaffold | current |
| [GCA_004024645.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_004024645.1/dataset_report) | Mirza coquereli | MizCoq_v1_BIUU | Scaffold | current |
| [GCF_040939455.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_040939455.1/dataset_report) | Microcebus murinus | M.murinus_Inina_mat1.0 | Chromosome | current |
| [GCA_963574885.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963574885.1/dataset_report) | Lepilemur ruficaudatus | PGDP_LepRuf | Scaffold | current |
| [GCF_041146395.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_041146395.1/dataset_report) | Eulemur rufifrons | OSU_ERuf_1 | Chromosome | current |
| [GCA_963575175.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963575175.1/dataset_report) | Hapalemur meridionalis | PGDP_HapMer | Scaffold | current |
| [GCA_003258685.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_003258685.1/dataset_report) | Prolemur simus | Prosim_1.0 | Scaffold | current |
| [GCF_020740605.2](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_020740605.2/dataset_report) | Lemur catta | mLemCat1.pri | Chromosome | current |
| [GCA_028533085.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_028533085.1/dataset_report) | Varecia variegata | Varecia_variegata_HiC | Chromosome | current |
| [GCA_963575035.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963575035.1/dataset_report) | Avahi laniger | PGDP_AvaLan | Scaffold | current |
| [GCA_004363605.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_004363605.1/dataset_report) | Indri indri | IndInd_v1_BIUU | Scaffold | current |
| [GCF_000956105.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_000956105.1/dataset_report) | Propithecus coquereli | Pcoq_1.0 | Scaffold | current |
| [GCA_023783435.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_023783435.1/dataset_report) | Galago moholi | ASM2378343v1 | Contig | current |
| [GCA_963574575.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963574575.1/dataset_report) | Galagoides demidoff | PGDP_GalDem | Scaffold | current |
| [GCA_000181295.3](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_000181295.3/dataset_report) | Otolemur garnettii | OtoGar3 | Scaffold | current |
| [GCA_963573935.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963573935.1/dataset_report) | Arctocebus calabarensis | PGDP_ArcCal | Scaffold | current |
| [GCA_023783135.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_023783135.1/dataset_report) | Loris tardigradus | ASM2378313v1 | Contig | current |
| [GCF_027406575.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCF_027406575.1/dataset_report) | Nycticebus coucang | mNycCou1.pri | Chromosome | current |
| [GCA_963574655.1](https://api.ncbi.nlm.nih.gov/datasets/v2/genome/accession/GCA_963574655.1/dataset_report) | Perodicticus potto | PGDP_PerPot | Scaffold | current |

元数据记录存在不等于下载文件已验证。没有请求基因组序列包，没有核验序列内容、完整性或实际下载大小；上述 NCBI 元数据检查本身不构成 T2T 或真值认证。

## 2026-09-14 T2T 展示级别补充核验

| accession | NCBI 原始级别 | 仓库级别 | 证据与范围 |
| --- | --- | --- | --- |
| GCA_049350105.2 | Complete Genome | T2T | [发布者 T2T-MMU8 项目](https://github.com/zhang-shilong/T2T-MMU8)明确将该 accession 对应到 v2.0，说明完整组装包括 20 条常染色体、X、Y 及线粒体；T2T 判定针对核染色体，线粒体单独随包提供 |

发布者说明常染色体和 X 来源于 MMU2019108-1，Y 来源于另一供体 MMU1003063。因此该组装不应被当作单一个体的完整单倍型。这是对发布者证据的整理，未自行验证序列或端粒结构。

当前仅上述记录完成 T2T 证据核验；其他记录暂按 NCBI 级别展示，T2T 审核状态为待核实。本轮引入独立级别不代表其他灵长类组装均为非T2T。

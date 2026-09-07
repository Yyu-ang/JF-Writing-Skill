# 土木与隧道工程学术写作 Skill

本 Skill 由 `Ryyyyyyy233/JF-Writing-Skill` 的模块化架构改造而来，保留“主 Skill 负责路由，references 按需加载”的设计，移除 Journal of Finance、金融经济学和 JF 专用表达，改为服务于土木工程、岩土工程、隧道与地下工程、岩石力学、工程地质、TBM/盾构/EPB、现场监测、试验研究及数值模拟论文。

## 触发词

`隧道写作`、`土木写作`、`岩土写作`、`CTE-skill`、`tunnelling polish`、`geotechnical translate`

## 模块

```text
civil-tunnelling-skill-1.0.0/
├── SKILL.md
├── README-chinese.md
├── README-english.md
└── references/
    ├── sentence-templates.md      # 句子功能与段落入口
    ├── phrase-bank.md             # 专业动词、搭配、限定语与逻辑连接
    ├── paragraph-patterns.md      # 引言、方法、结果、讨论等段落结构
    ├── meta-discourse.md          # 解释边界、证据边界、模型/现场关系
    └── usage-guide.md             # 润色、翻译、全文审查流程
```

## 适用研究

- 隧道开挖、围岩响应、支护与衬砌、地表沉降、掌子面稳定；
- TBM、盾构与 EPB 施工参数和掘进性能；
- 岩土与岩石室内试验、模型试验和现场监测；
- 工程地质与不良地质条件；
- FEM、FDM、DEM、MPM、无网格方法及耦合数值模拟；
- 本构模型、参数反演、敏感性分析；
- 面向隧道/岩土问题的机器学习与数据驱动研究。

## 使用原则

1. 技术内容优先于语言风格。方程、符号、单位、数值、图表编号、引用、地质条件、机械参数、边界条件不得因润色而改变。
2. 明确区分实测量、输入量、派生量、数值输出、解释和人工标签。
3. 结果段落优先写“观察到什么—变化多大—在什么条件下—如何解释”，避免只写“显著提高”“效果良好”。
4. 数值研究区分 verification 与 validation：算法/离散是否正确，不等于模型已经得到物理验证。
5. 数据驱动论文仍以工程问题为主，保留数据来源、划分策略、泄漏防控、标签定义和工程适用边界。
6. references 是参考库，不是必须逐条套用的模板。

## 与原 JF Skill 的区别

原仓库的金融市场、因果识别、资产定价、JF ALL-CAPS 开头、金融专用 collocation 等内容全部移除或重写。原版本中围绕 GPTZero/AI detector 的固定阈值和刻意随机化句长的策略也不保留；新版本改为检查结构是否机械、论证是否重复、术语是否一致、限定语是否与证据强度匹配。

## 说明

原 JF Skill 声称其模式来自大量 JF 论文。本改造版目前是**专业规则型参考 Skill**，不虚构“已经统计分析了某个隧道期刊语料库”。若投稿 TUST、Computers and Geotechnics、Engineering Geology、RMRE 等具体期刊，仍建议结合该期刊近年的真实论文进行最终校准。

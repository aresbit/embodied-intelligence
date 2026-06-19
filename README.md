# 《具身智能导论》

> **Embodied Intelligence: An Introduction**  
> UC Berkeley CS294-291 "Robots That Learn" 中文翻译与详解  
> 主讲: Jitendra Malik | TA: Tara Sadjadpour | Spring 2026

[![GitHub Pages](https://img.shields.io/badge/在线阅读-aresbit.github.io%2Fembodied--intelligence-blue)](https://aresbit.github.io/embodied-intelligence/)

---

## 内容

将 Berkeley 机器人学习课程翻译为 **17 章中文 Markdown**，每章包含：

- **完整数学推导** — LaTeX 格式，从第一性原理出发
- **论文精读** — 23 篇核心论文的逐段解读
- **PyTorch 代码** — 50+ 个可运行代码模块，逐行中文注释
- **练习与思考** — 100+ 道题（理论推导 + 编程实践 + 开放研究）

## 目录

### 第一部分：导论与生物基础

| 章 | 标题 | 核心内容 |
|:--|------|----------|
| 01 | 导论：为什么要让机器人学习 | POMDP形式化、具身智能数学定义 |
| 02 | 生物运动力学：行走与奔跑 | CPG振荡器、DMP动力学、Tegotae |
| 03 | 机器人机构学：运动学与动力学 | 李群李代数、PoE、RNEA |
| 04 | 扩散模型入门 | DDPM/Score/NF/Flow Matching |
| 05 | 人手与灵巧操作 | 抓取矩阵、力封闭、世纪手综述 |
| 06 | 本体感觉与触觉感知 | 机械感受器模型、GelSight/BioTac |

### 第二部分：控制与学习基础

| 章 | 标题 | 核心内容 |
|:--|------|----------|
| 07 | 运动控制的发展视角 | 婴儿六条教训、跨模态蒸馏 |
| 08 | 机器人动力学与控制 | LQR/DDP/MPC、内部模型 |
| 09 | 计算神经科学 | 卡尔曼滤波↔小脑、预测编码 |
| 10 | 视频世界模型 | RSSM、World Action Models |
| 11 | 强化学习 | MDP→策略梯度→GAE→SAC |

### 第三部分：学习范式与案例

| 章 | 标题 | 核心内容 |
|:--|------|----------|
| 12 | 行为克隆 | 分布偏移、Diffusion Policy、DDIM |
| 13 | 视觉模仿学习 | UMI、SLAM、跨具身迁移 |
| 14 | 运动控制案例研究 | RMA、自我中心视觉运动 |
| 15 | 导航案例研究 | GOAT、可穿越性估计 |
| 16 | 灵巧操作案例研究 | 阻抗控制、Sim-to-Real Recipe |
| 17 | 长程规划与语言 | VLA、π0.5、MolmoSpaces |

## 学习路径

| 路径 | 章节 |
|------|------|
| 机器人学习工程师 | 01→03→08→11→12→14→15→16→17 |
| 理论研究 | 01→04→06→09→10→17 |
| 仿生机器人 | 01→02→05→06→07→14 |

## 论文清单

23 篇核心论文全文 (PDF) 位于 `raw/` 目录，含 `pdftotext` 提取的文本版本。

| 章 | 论文 |
|:--|------|
| 02 | Ramdya & Ijspeert, "Neuromechanics of animal locomotion", *Science Robotics* 2023 |
| 04 | Papamakarios et al. "Normalizing Flows" (*JMLR* 2021) + Lipman et al. "Flow Matching" (*ICLR* 2023) |
| 05 | Piazza et al., "A Century of Robotic Hands", *Annual Review* 2019 |
| 06 | Jones "Human Hand Function" + Gardner "Touch" |
| 07 | Loquercio et al. (*ICRA* 2023) + Smith & Gasser (*Artificial Life* 2005) |
| 08 | Kawato "Internal models" (1999) + Flanagan et al. "Control strategies" (2006) |
| 09 | Land et al., "Roles of vision and eye movements", *Perception* 1999 |
| 10 | Ye et al. "World Action Models" + Bharadhwaj et al. "Track2Act" |
| 12 | Chi et al., "Diffusion Policy", *RSS* 2023 |
| 13 | Chi et al., "Universal Manipulation Interface", *RSS* 2024 |
| 14 | Kumar et al. "RMA" (*RSS* 2021) + Agarwal et al. (*CoRL* 2022) |
| 15 | Chang et al. "GOAT" (*RSS* 2024) + Frey et al. (*RSS* 2023) |
| 16 | Lin et al. (*CoRL* 2025) + Choi et al. "UMI-FT" (*ICRA* 2026) |
| 17 | Physical Intelligence "π0.5" (*CoRL* 2025) + Kim et al. "MolmoSpaces" (2026) |

## 构建

本仓库通过 GitHub Pages 自动发布，源目录 `docs/`，使用 Cayman Jekyll 主题。推送 `main` 分支后约 1 分钟生效。

```
embodied-intelligence/
├── docs/          # 17章中文Markdown + 索引 + 术语表 (GitHub Pages源)
├── raw/           # 23篇论文PDF + pdftotext文本
├── task_plan.md   # 翻译规划
└── README.md
```

## 致谢

- 原课程: [Robots That Learn](https://robots-that-learn.github.io/) — Jitendra Malik, UC Berkeley
- CII 翻译项目经验参考: [aresbit/cii-code](https://github.com/aresbit/cii-code)
- 翻译引擎: paper-agent 并行翻译 + pdftotext 论文提取管线

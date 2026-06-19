# 《具身智能导论》—— 从 Robots That Learn 到中文详解

> **Embodied Intelligence: An Introduction**  
> 基于 UC Berkeley CS294-291 "Robots That Learn", Spring 2026  
> 主讲: Jitendra Malik | TA: Tara Sadjadpour  
> 中文翻译与详解: 含完整数学推导 + PyTorch 代码实现 + 23篇核心论文精读

---

## 课程概述

当深度学习席卷计算机视觉和自然语言处理之后，机器人领域终于迎来了自己的"ImageNet 时刻"。这门由 Jitendra Malik 在 UC Berkeley 开设的研究生课程，系统性地呈现了"让机器人从经验中学习"的连贯框架——从生物运动控制的基础原理，到扩散策略、世界模型和视觉-语言-动作大模型等前沿技术。

本书以课程 12 次 Lecture 为蓝本，拆分为 17 章，每章包含：
- **完整的数学推导**（LaTeX，从第一性原理出发）
- **论文精读**（23篇核心论文的逐段解读）
- **可运行的 PyTorch 代码**（逐行中文注释）
- **练习与思考**（从理论推导到编程实践）

---

## 第一部分：导论与生物基础

| 章节 | 标题 | 对应 Lecture | 核心内容 |
|:----:|------|:------------|----------|
| 01 | [导论：为什么要让机器人学习](ch01_导论.md) | L1 | POMDP形式化、具身智能数学定义、七十年历史脉络 |
| 02 | [生物运动力学：行走与奔跑](ch02_生物运动力学.md) | L2A | CPG振荡器、DMP动力学系统、Tegotae局部反馈 |
| 03 | [机器人机构学：运动学与动力学](ch03_机器人机构学.md) | L2B | 李群李代数、PoE前向运动学、RNEA逆动力学 |
| 04 | [扩散模型入门](ch04_扩散模型入门.md) | L3 | DDPM/Score/NF/Flow Matching四层范式完整推导 |
| 05 | [人手与灵巧操作](ch05_人手与机器人手.md) | L4A | 抓取矩阵、力封闭、世纪机器人手综述 |
| 06 | [本体感觉与触觉感知](ch06_本体感觉与触觉感知.md) | L4B | 机械感受器传递函数、GelSight/BioTac传感器 |

## 第二部分：控制与学习基础

| 章节 | 标题 | 对应 Lecture | 核心内容 |
|:----:|------|:------------|----------|
| 07 | [运动控制的发展视角](ch07_运动控制的发展视角.md) | L5A | 婴儿六条教训、跨模态监督蒸馏、课程学习 |
| 08 | [机器人动力学、控制与运动规划](ch08_机器人动力学与控制.md) | L5B | LQR/DDP/MPC完整推导、内部模型与反馈误差学习 |
| 09 | [计算神经科学与预测控制](ch09_计算神经科学与预测控制.md) | L6A | 卡尔曼滤波↔小脑、预测编码、主动推断 |
| 10 | [视频世界模型](ch10_视频世界模型.md) | L6B | RSSM、World Action Models、Track2Act |
| 11 | [强化学习](ch11_强化学习.md) | L7 | MDP→策略梯度→GAE→SAC完整推导 |

## 第三部分：学习范式与案例研究

| 章节 | 标题 | 对应 Lecture | 核心内容 |
|:----:|------|:------------|----------|
| 12 | [行为克隆](ch12_行为克隆.md) | L8A | 分布偏移分析、Diffusion Policy、DDIM加速 |
| 13 | [视觉模仿学习](ch13_视觉模仿学习.md) | L8B | UMI、SLAM姿态估计、跨具身策略迁移 |
| 14 | [运动控制案例研究](ch14_运动控制案例研究.md) | L9 | RMA快速运动适应、自我中心视觉运动 |
| 15 | [导航案例研究](ch15_导航案例研究.md) | L10 | GOAT多模态目标、快速可穿越性估计 |
| 16 | [灵巧操作案例研究](ch16_灵巧操作案例研究.md) | L11 | 阻抗/导纳控制、Sim-to-Real Recipe、UMI-FT |
| 17 | [长程规划与语言](ch17_长程规划与语言.md) | L12 | VLA模型、π0.5、MolmoSpaces、课程总结 |

---

## 阅读指南

### 学习路径

1. **机器人学习工程师路径**: Ch01 → Ch03 → Ch08 → Ch11 → Ch12 → Ch14-17
2. **理论研究路径**: Ch01 → Ch04 → Ch06 → Ch09 → Ch10 → Ch17
3. **仿生机器人路径**: Ch01 → Ch02 → Ch05 → Ch06 → Ch07 → Ch14

### 前置知识

- 深度学习基础 (Bishop & Bishop)
- 强化学习基础 (Sutton & Barto)
- 线性代数、概率论、优化理论
- Python/PyTorch

---

## 核心论文清单

| 章节 | 论文 |
|:----:|------|
| 02 | Ramdya & Ijspeert, "The neuromechanics of animal locomotion", *Science Robotics*, 2023 |
| 04 | Papamakarios et al., "Normalizing Flows", *JMLR*, 2021 |
| 04 | Lipman et al., "Flow Matching for Generative Modeling", *ICLR*, 2023 |
| 05 | Piazza et al., "A Century of Robotic Hands", *Annual Review*, 2019 |
| 06 | Jones, "Human Hand Function"; Gardner, "Touch", *ELS*, 2010 |
| 07 | Loquercio et al., "Learning Visual Locomotion", *ICRA*, 2023 |
| 07 | Smith & Gasser, "Six Lessons from Babies", *Artificial Life*, 2005 |
| 08 | Kawato, "Internal models for motor control", *Curr. Opin. Neurobiol.*, 1999 |
| 08 | Flanagan et al., "Control strategies in object manipulation", *Curr. Opin. Neurobiol.*, 2006 |
| 09 | Land et al., "The roles of vision and eye movements", *Perception*, 1999 |
| 10 | Ye et al., "World Action Models", *arXiv*, 2026 |
| 10 | Bharadhwaj et al., "Track2Act", *arXiv*, 2024 |
| 12 | Chi et al., "Diffusion Policy", *RSS*, 2023 |
| 13 | Chi et al., "Universal Manipulation Interface", *RSS*, 2024 |
| 14 | Kumar et al., "RMA: Rapid Motor Adaptation", *RSS*, 2021 |
| 14 | Agarwal et al., "Legged Locomotion in Challenging Terrains", *CoRL*, 2022 |
| 15 | Chang et al., "GOAT: Go to Any Thing", *RSS*, 2024 |
| 15 | Frey et al., "Fast Traversability Estimation", *RSS*, 2023 |
| 16 | Lin et al., "Sim-to-Real RL for Dexterous Manipulation", *CoRL*, 2025 |
| 16 | Choi et al., "UMI-FT: In-the-Wild Compliant Manipulation", *ICRA*, 2026 |
| 17 | Physical Intelligence, "π0.5: a VLA with Open-World Generalization", *CoRL*, 2025 |
| 17 | Kim et al., "MolmoSpaces", *arXiv*, 2026 |

---

> 本书由 AI 翻译引擎基于课程 slides + 23篇论文全文自动翻译生成，数学推导经过独立验证，代码实现为基于论文方法的原创 PyTorch 重构。

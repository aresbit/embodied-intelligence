# Task Plan: Robots That Learn → 《具身智能导论》中文翻译与详解

## Goal
将 [Robots That Learn](https://robots-that-learn.github.io/) (UC Berkeley CS294-291, Spring 2026)
全课程翻译为 **《具身智能导论》中文 Markdown 教程**，每章包含完整的数学推理、代码解释与论文精读，
输出到 `ai-robot/chapters/` 目录下供 GitHub Pages 发布。

## Reference Experience: CII 翻译项目
- 21章分 Batch 并行翻译，paper-agent 独立处理每章
- 每章统一输出格式（设计哲学 → 数据结构 → 代码注释 → 现代改进）
- 中文术语一致性检查 + 目录索引

---

## Course Structure Mapping

| Ch | Lecture | 中文标题 | 子主题 | Slides PDF | 阅读论文 |
|----|---------|---------|--------|------------|----------|
| 01 | L1 | 导论：为什么要让机器人学习 | 课程概览、具身智能历史 | ✓ | - |
| 02 | L2A | 生物运动力学：行走与奔跑 | 骨骼肌生物力学、步态周期 | ✓ | Ramdya & Ijspeert |
| 03 | L2B | 机器人机构学：运动学与动力学 | DH参数、拉格朗日/牛顿-欧拉 | ✓ | - |
| 04 | L3 | 扩散模型入门 (Kanazawa) | DDPM、流匹配、Normalizing Flows | ✓ | Papamakarios + Lipman |
| 05 | L4A | 人手与灵巧操作 + 机器人手 | 人手解剖学、灵巧手设计 | ✓ | Piazza et al. |
| 06 | L4B | 本体感觉与触觉感知 | 触觉传感器、GelSight、皮肤力学 | ✓ | Jones + Gardner |
| 07 | L5A | 运动控制的发展视角 | 发育认知、运动基元、CPG | ✓ | Loquercio + Smith & Gasser |
| 08 | L5B | 机器人动力学、控制与运动规划 | LQR、MPC、轨迹优化 | ✓ | Kawato + Flanagan |
| 09 | L6A | 计算神经科学：预测与控制 | 前向/逆向模型、小脑模型 | ✓ | Land et al. |
| 10 | L6B | 视频世界模型 | 视频预测、潜在动态模型 | ✓ | Ye et al. + Bharadhwaj |
| 11 | L7 | 强化学习 | MDP、Policy Gradient、Actor-Critic | ✓ | Haarnoja + OpenAI |
| 12 | L8A | 行为克隆 | BC、扩散策略、动作分块 | ✓ | Chi et al. |
| 13 | L8B | 视觉模仿学习 | UMI、3D表示、cross-embodiment | ✓ | UMI |
| 14 | L9 | 运动控制案例研究 | RMA、四足/双足行走 | ✓ | Kumar + Agarwal |
| 15 | L10 | 导航案例研究 (Frey) | GOAT、可穿越性估计 | ✓ | Chang + Frey |
| 16 | L11 | 灵巧操作案例研究 | Sim-to-Real、触觉操作 | ✓ | Lin + Choi |
| 17 | L12 | 长程规划与语言的作用 | VLA、MolmoSpaces、π0.5 | ✓ | Physical Intelligence + Kim |

共 **17 章** (12 lectures 中 L2/L4/L5/L6/L8 各拆为 A/B)

---

## Phases

### Phase 1: 素材采集 (pending)
- [ ] 用 WebFetch/Read 获取每章 slides PDF 内容
- [ ] 下载并阅读每章核心论文 (arXiv PDF)
- [ ] 提取关键数学公式和算法伪代码
- **Status:** pending

### Phase 2: 批量并行翻译 (pending)
- [ ] **Batch A (Ch01-06):** 导论 + 生物基础 (L1, L2A, L2B, L3, L4A, L4B)
- [ ] **Batch B (Ch07-11):** 控制与学习基础 (L5A, L5B, L6A, L6B, L7)
- [ ] **Batch C (Ch12-17):** 学习范式与案例 (L8A, L8B, L9, L10, L11, L12)
- **Status:** pending

### Phase 3: 质量审核 (pending)
- [ ] 数学公式符号一致性检查 (统一使用 LaTeX)
- [ ] 中文术语对照一致性检查
- [ ] 代码示例可执行性验证 (Python/PyTorch)
- [ ] 论文精读质量检查
- **Status:** pending

### Phase 4: 汇总输出 (pending)
- [ ] 生成 `_sidebar.md` 目录导航
- [ ] 生成术语对照表 `glossary.md`
- [ ] 生成 `index.md` 课程主页
- [ ] GitHub Pages 配置 `_config.yml`
- **Status:** pending

---

## 每章输出格式

```markdown
# 第N章: 中文标题 (English Title)
> 原课程: Robots That Learn, UC Berkeley CS294-291, Spring 2026
> 主讲: [Instructor Name]
> 本章基于 Lecture X, slides + 阅读论文 [Paper Title]

## 一、本章概要 (Overview)
- 核心问题与动机
- 与前后章节的逻辑关系

## 二、核心概念与数学基础 (Core Concepts & Math)
- 关键定义 (中英对照)
- 完整数学推导 (LaTeX, 从第一性原理出发)
- 物理直觉与几何解释

## 三、论文精读 (Paper Deep Dive)
- 方法论逐段解读
- 关键公式展开推导
- 实验设计与结果分析

## 四、算法与代码实现 (Algorithm & Code)
- 伪代码 → PyTorch/Python 实现
- 关键代码逐行注释
- 训练技巧与工程细节

## 五、核心Takeaway与延伸阅读 (Takeaways)
- 3-5个核心洞察
- 开放问题与研究方向
- 推荐延伸阅读

## 六、练习与思考 (Exercises)
- 基于本章内容的思考题
```

---

## Decisions

| Decision | Rationale |
|----------|-----------|
| 17章分3个Batch并行翻译 | 参考CII项目经验, paper-agent独立处理每章, 避免上下文超长 |
| 每章包含完整数学推导 | 用户明确要求"详细数学推理" |
| 每章包含PyTorch代码实现 | 用户要求"代码解释", 结合slides伪代码和论文方法实现 |
| 论文精读融入章节 | lecture本身以论文为核心, 不应分离为独立文档 |
| 中文输出 + 核心术语保留英文 | 参考CII模式, 便于学术引用 |
| 输出到 ai-robot/chapters/ | 与 CII 的 docs/ 对称, 便于 GitHub Pages 部署 |

---

## Technical Notes

- **PDF 读取**: 使用 Read 工具读取 arXiv PDF(通过 liteparse), slides PDF 通过 WebFetch 获取文本
- **并行策略**: 每个 paper-agent 独立获取对应 lecture 的 slides + 论文, 翻译写入 `chapters/chXX_*.md`
- **数学公式**: 统一使用 $...$ 行内, $$...$$ 行间 LaTeX 格式
- **代码格式**: 使用 ```python 代码块, 基于 PyTorch 实现
- **术语管理**: 维护 `glossary.md` 作为术语锚点, 各章引用统一术语表

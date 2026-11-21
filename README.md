<div align="center">

# 王同学

**人工智能硕士在读 · 长沙**

大模型评测工程 · 具身智能 · 半导体测试与自动化

<a href="mailto:wang2067562393@gmail.com"><img src="https://img.shields.io/badge/Gmail-wang2067562393@gmail.com-D14836?logo=gmail&logoColor=white&style=flat-square"></a>
<img src="https://img.shields.io/badge/长沙-中国-00B96B?logo=openstreetmap&logoColor=white&style=flat-square">
<img src="https://img.shields.io/badge/2027_寒假实习-求职中-FF6A00?style=flat-square">

</div>

---

**把「感觉」变成「数字」。** 评测里是 3σ 和锚点，链路里是 p95 和抖动，测试里是溯源到每一条 Log。

做的东西横跨三个领域，但方法是同一套：**先定义什么叫「对」，再让它可测量、可复现、可被别人接手。**

---

## 方向

### 01 · 大模型评测与推理效率

*怎么判断一个「提升」是真的。*

- **[evalkit](https://github.com/wang2067562393-dot/llm-inference-efficiency-notes)** — 3σ 幅度门槛、归一化评分、13 条发布前检查；附完整判定案例与四个「看起来通过但不算数」的反例。<sub>43 个测试 · 零依赖</sub>
- **评测任务构建与质检**（2026.06–）— 定可改面、冻结协议、三 seed 成对对照、证据链打包，覆盖 Prefill 与 Decode 两侧四个方向。
- 在补：投机解码的接受率—加速比实测（含「draft 太小反而变慢」的负结果）。

### 02 · 具身智能与实时链路

*延迟多少？问题在哪一段？该降级还是该修？*

- **[teleop-link-lab](https://github.com/wang2067562393-dot/teleop-link-lab)** — 控制端 → 弱网代理 → 机器人 → 视频回流，全链路打点；自研延迟/抖动/丢包注入器。<sub>60 个测试 · 六场景实验报告</sub>
- 先校准再测量：零延迟基线压到 **0.4 ms**，注入 100 ms 后往返 **203.8 ms**，六个弱网场景全部可复现。
- 下一步：双机与真机实测、H.264 串流路径。

### 03 · 半导体测试与工业自动化

*把人工翻几千行 Log 变成一条命令。*

- **[chip-test-automation](https://github.com/wang2067562393-dot/chip-test-automation)** — 日志解析、跨固件版本配对对比、3σ / MAD 异常检测；纯标准库。<sub>3 个工具 · 单元测试 + CI</sub>
- **UWB 芯片功能与可靠性测试**（2025.12–2026.08）— 固件烧录与版本管理、通过上位机 Log 定位异常、把手工分析写成脚本。
- 下一步：百万行吞吐测试、指标漂移的回归门。

### 04 · 工程地基

*每周一个能跑、能复现的交付。*

- **[ai-plan-2029](https://github.com/wang2067562393-dot/ai-plan-2029)** — GPU 基准、多镜像降级的数据获取、纯函数化的可测试分析；环境锁定、结果入库、CI 每次 push 自动跑。<sub>按周推进</sub>
- 在补：不装框架，用 NumPy 从零写「权重 → 概率 → 损失 → 梯度 → 更新」。

---

## 技能

**能独立做的**
评测协议设计 · 对照实验与统计判定 · 延迟/抖动测量 · 日志与数据自动化 · 测试与 CI

**工具**
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white&style=flat-square)
![C](https://img.shields.io/badge/C-A8B9CC?logo=c&logoColor=black&style=flat-square)
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black&style=flat-square)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white&style=flat-square)
![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white&style=flat-square)
![GitHub Actions](https://img.shields.io/badge/Actions-2088FF?logo=githubactions&logoColor=white&style=flat-square)
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white&style=flat-square)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white&style=flat-square)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white&style=flat-square)

---

## 现在

- **在找**：大模型评测、推理效率、具身智能/机器人实时链路方向的实习（长沙线下或远程）
- **在补**：深度学习地基（手写反向传播与 MLP）、推理方法的原理实测
- **短板写在明处**：没有真机经验，C++ 只到能读、能改小模块

<div align="center">

<sub><i>If you can't measure it, you can't claim it.</i></sub>

</div>

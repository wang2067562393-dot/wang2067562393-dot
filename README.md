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

做的东西横跨三个领域，方法是同一套：**先定义什么叫「对」，再让它可测量、可复现、可被别人接手。**

---

## 我在做的四个方向

<table>
<tr>
<td width="50%" valign="top">

### 🧪 大模型评测与推理效率

*怎么判断一个「提升」是真的。*

**[evalkit](https://github.com/wang2067562393-dot/llm-inference-efficiency-notes)** — 3σ 幅度门槛、归一化评分、13 条发布前检查；含四个「看起来通过但不算数」的反例。

**首组自测**：12 GB A 卡上 7B Q4 生成 **67.2 t/s**（CPU 8.3 t/s，**8.08×**），实测有效带宽 314 GB/s ≈ 标称的 72.7%；预填充只快 1.7×，长 prompt 收益远小于生成。

**评测任务构建与质检**（2026.06–）— 定可改面、冻结协议、三 seed 成对对照、证据链打包。

`Python` `统计判定` `CI`
<sub>43 个测试 · 零依赖 · 4 个评测方向</sub>

</td>
<td width="50%" valign="top">

### 🎮 具身智能与实时链路

*延迟多少？问题在哪一段？该降级还是该修？*

**[teleop-link-lab](https://github.com/wang2067562393-dot/teleop-link-lab)** — 控制端 → 弱网代理 → 机器人 → 视频回流，全链路打点；自研延迟/抖动/丢包注入器。

先校准再测量：零延迟基线 **0.4–0.9 ms**，注入 100 ms 后往返 **203.8 ms**，六个弱网场景全可复现；换台机器复跑，注入类指标偏差 ≤5%，基线差 +38%（已写进局限）。

**跨机器模式**：三进程拆分 + 用 RTT 最小样本估时钟偏移（误差 0.03 ms），LAN 实测 50 ms 单向注入 → 往返 101.9 ms。

`asyncio` `UDP` `实时测量`
<sub>67 个测试 · 六场景实验报告 · 跨机器可跑</sub>

</td>
</tr>
<tr>
<td valign="top">

### 🔬 半导体测试与工业自动化

*把人工翻几千行 Log 变成一条命令。*

**[chip-test-automation](https://github.com/wang2067562393-dot/chip-test-automation)** — 日志解析、跨固件版本配对对比、3σ / MAD 异常检测；纯标准库，clone 即用。

百万行日志实测 **23.2 万行/秒**、峰值内存 **309.5 MB**；配 `chiptest gate` 回归门，指标漂移超阈值直接 exit 1 并定位到测试项。

**UWB 芯片测试**（2025.12–2026.08）— 固件烧录与版本管理、用上位机 Log 定位异常。

`Python` `日志` `零依赖`
<sub>5 个工具 · 17 个测试 + CI</sub>

</td>
<td valign="top">

### 🗂 工程地基

*每周一个能跑、能复现的交付。*

**[ai-plan-2029](https://github.com/wang2067562393-dot/ai-plan-2029)** — GPU 基准、多镜像降级的数据获取、纯函数化的可测试分析；环境锁定、结果入库、CI 自动跑。

正在补：不装框架，用 NumPy 从零写「权重 → 概率 → 损失 → 梯度 → 更新」。

`uv` `PyTorch` `CI`
<sub>按周推进 · 结果可复算</sub>

</td>
</tr>
</table>

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

- **在找**：大模型评测、推理效率、具身智能 / 机器人实时链路方向的实习（长沙线下或远程）
- **在补**：深度学习地基（手写反向传播与 MLP）、推理方法的原理实测
- **短板写在明处**：没有真机经验，C++ 只到能读、能改小模块

<div align="center">

<sub><i>If you can't measure it, you can't claim it.</i></sub>

</div>

<div align="center">

# 王同学

**人工智能硕士在读 · 长沙**

大模型评测工程 · 半导体与嵌入式系统（在学）

<a href="mailto:wang2067562393@gmail.com"><img src="https://img.shields.io/badge/Gmail-wang2067562393@gmail.com-D14836?logo=gmail&logoColor=white&style=flat-square"></a>
<img src="https://img.shields.io/badge/长沙-中国-00B96B?logo=openstreetmap&logoColor=white&style=flat-square">
<img src="https://img.shields.io/badge/2027_寒假实习-求职中-FF6A00?style=flat-square">

</div>

---

**把「感觉」变成「数字」。** 评测里是 3σ 和锚点，链路里是 p95 和抖动，测试里是溯源到每一条 Log。

做的东西横跨三个领域，方法是同一套：**先定义什么叫「对」，再让它可测量、可复现、可被别人接手。**

---

## 我在做的两个方向

主线是评测；另一条是半导体与嵌入式——手上在做，同时在补硬件那一半。

<table>
<tr>
<td width="100%" valign="top">

### 🧪 大模型评测与 agent 训练环境

*怎么判断一个「提升」是真的。*

**agentic RL 训练数据构建**（2026.06– ，实习）— 基于 Harbor 容器环境：题面（instruction）、可运行环境（Dockerfile）、评分器（verifier）；定可改面、冻结协议、三 seed 成对对照、证据链打包。

**[evalkit](https://github.com/wang2067562393-dot/llm-inference-efficiency-notes)** — 3σ 幅度门槛、归一化评分、13 条发布前检查；含四个「看起来通过但不算数」的反例。

**推理效率实测**：12 GB A 卡上 7B Q4 生成 **67.2 t/s**（CPU 8.3 t/s，**8.08×**），实测有效带宽 314 GB/s ≈ 标称的 72.7%；预填充只快 1.7×，长 prompt 收益远小于生成。

`Python` `统计判定` `Docker` `CI`
<sub>43 个测试 · 零依赖 · 4 个评测方向</sub>

</td>
</tr>
<tr>
<td width="100%" valign="top">

### 🔬 半导体与嵌入式系统

*从解析 Log，到驱动芯片。*

**[chip-test-automation](https://github.com/wang2067562393-dot/chip-test-automation)** — 日志解析、跨固件版本配对对比、3σ / MAD 异常检测；纯标准库，clone 即用。

百万行日志实测 **23.2 万行/秒**、峰值内存 **309.5 MB**；配 `chiptest gate` 回归门，指标漂移超阈值直接 exit 1 并定位到测试项。

**UWB 芯片测试**（2025.12–2026.08）— 固件烧录与版本管理、用上位机 Log 定位异常。

**在学**（嵌入式和 AI 一起学）：从 UART / SPI / I2C 与寄存器读写起步 → 硬件在环测试夹具 → 板端推理。目标是把「上位机 + 总线 + 仪器」这条链路亲手打通，让测试从「读别人导出的 Log」变成「自己驱动被测芯片」。

`Python` `C` `日志` `零依赖`
<sub>5 个工具 · 17 个测试 + CI · 嵌入式在学</sub>

</td>
</tr>
</table>

**在补的地基**：[ai-plan-2029](https://github.com/wang2067562393-dot/ai-plan-2029) — 每周一个能跑、能复现的交付；正在补手写反向传播与 MLP。

---

## 技能

**能独立做的**
评测协议设计 · 对照实验与统计判定 · 任务包与 verifier 自检 · 日志与数据自动化 · 测试与 CI

**在学**
UART / SPI / I2C 与寄存器读写 · 硬件在环测试夹具 · 交叉编译与板端推理

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

- **在找**：大模型评测、agent 训练环境（RLVR / verifier 方向）的实习（长沙线下或远程）；也在看半导体测试自动化 / 嵌入式软件的岗位
- **在补**：Harbor 与 verifier 的实战（从零重做一道题、自己 hack 一次自己的评分器）；嵌入式那一半——总线协议、硬件在环、板端推理
- **短板写在明处**：没有真机经验，C++ 只到能读、能改小模块，嵌入式还没在真实板子上跑出过东西

<div align="center">

<sub><i>If you can't measure it, you can't claim it.</i></sub>

</div>

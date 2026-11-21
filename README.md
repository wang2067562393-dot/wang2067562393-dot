<div align="center">

# 王同学

**人工智能硕士在读 · 长沙**

大模型评测工程 · 实时链路测量 · 测试自动化

<a href="mailto:wang2067562393@gmail.com"><img src="https://img.shields.io/badge/Gmail-wang2067562393@gmail.com-D14836?logo=gmail&logoColor=white&style=flat-square"></a>
<img src="https://img.shields.io/badge/长沙-中国-00B96B?logo=openstreetmap&logoColor=white&style=flat-square">
<img src="https://img.shields.io/badge/2027_寒假实习-求职中-FF6A00?style=flat-square">

</div>

---

**把「感觉」变成「数字」。** 评测里是 3σ 和锚点，链路里是 p95 和抖动。

做过半年的大模型评测实习：把论文变成能公平评测的任务，定可改面、冻结协议、跑三 seed 成对对照、判断改善是否成立。
现在自己做端到端的延迟测量——先证明测量工具没坏，再谈优化。

---

## 项目

<table>
<tr>
<td width="50%" valign="top">

### 🧪 [LLM 评测工具](https://github.com/wang2067562393-dot/llm-inference-efficiency-notes)

**把「怎么判断一个提升是真的」写成会抛错的代码。**

3σ 幅度门槛、归一化评分、13 条任务包发布前检查。
附一个完整判定案例，含四个「看起来通过但不算数」的反例：单位混用、σ=0、事后调锚点、样本量不足。

`Python` `统计判定` `CI`
<sub>llm-inference-efficiency-notes · 43 个测试 · 零依赖</sub>

</td>
<td width="50%" valign="top">

### 🎮 [遥操作实验台](https://github.com/wang2067562393-dot/teleop-link-lab)

**控制端 → 弱网代理 → 机器人 → 视频回流，全链路打点。**

自研延迟/抖动/丢包注入器；先校准测量工具再测链路——零延迟基线压到 **0.4 ms**，注入 100 ms 后往返 **203.8 ms**，六个弱网场景全部可复现。

`asyncio` `UDP` `实时测量`
<sub>60 个测试 · 六场景实验报告</sub>

</td>
</tr>
<tr>
<td valign="top">

### 🔬 [芯片测试日志自动化](https://github.com/wang2067562393-dot/chip-test-automation)

**把人工翻几千行 Log 变成一条命令。**

解析、跨固件版本配对对比、3σ / MAD 异常检测。
纯标准库，`git clone` 后无需装任何依赖。

`Python` `日志` `零依赖`
<sub>3 个工具 · 单元测试 + CI</sub>

</td>
<td valign="top">

### 🗂 [系统补强日志](https://github.com/wang2067562393-dot/ai-plan-2029)

**每周一个能跑、能复现的交付。**

GPU 基准、多镜像降级的数据获取、纯函数化的可测试分析。
环境锁定、结果入库、CI 每次 push 自动跑。

`uv` `PyTorch` `CI`
<sub>环境可复现 · 每周推进</sub>

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

- **在找**：大模型评测、推理效率、机器人实时链路方向的实习（长沙线下或远程）
- **在补**：深度学习地基（手写反向传播与 MLP）、推理方法的原理实测（投机解码的接受率曲线）
- **短板写在明处**：没有真机经验，C++ 只到能读、能改小模块

<div align="center">

<sub><i>If you can't measure it, you can't claim it.</i></sub>

</div>

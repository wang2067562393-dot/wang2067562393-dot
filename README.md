<div align="center">

# 你好，我是 王同学 👋

**AI 方向硕士研一在读 · 大模型评测工程与推理效率**

`Agentic 评测` · `统计判定与质量门` · `推理加速` · `测试自动化`

<a href="mailto:wang2067562393@gmail.com"><img src="https://img.shields.io/badge/Gmail-wang2067562393@gmail.com-D14836?logo=gmail&logoColor=white"></a>
<img src="https://img.shields.io/badge/长沙-中国-00B96B?logo=openstreetmap&logoColor=white">
<img src="https://img.shields.io/badge/2027寒假实习-求职中-FF6A00">
<img src="https://img.shields.io/badge/关注-评测的可信度-6366F1">

</div>

---

## ⏱ 30 秒看懂

| 项目 | 它解决什么问题 | 可验证的结果 |
|---|---|---|
| **[eval-kit](https://github.com/wang2067562393-dot/eval-kit)** | 把评测的验收判定（3σ、归一化评分）和任务包返修原因写成代码 | 13 条静态规则、**37 个单元测试**、零第三方依赖、CI 三版本矩阵 |
| **[llm-inference-efficiency-notes](https://github.com/wang2067562393-dot/llm-inference-efficiency-notes)** | KV Cache 压缩 / 视觉 Token 削减 / 投机解码，公式全部落成可运行工具 | 4 篇笔记 + 3 个工具 + **9 个测试**，含评测方法论专题 |
| **[chip-test-automation](https://github.com/wang2067562393-dot/chip-test-automation)** | 把「人工翻几千行 Log」变成一条命令出结构化报告 | 跨固件对比：通过率 33.3% → 83.3%（虚构示例数据） |
| **[ai-plan-2029](https://github.com/wang2067562393-dot/ai-plan-2029)** | 按周推进的工程化补强日志，每周一个可运行交付 | FP32 13.72 → FP16 31.68 TFLOPS（RTX 4060 Laptop 实测） |

> 我尽量只写自己跑过、能复现的数字。没跑出来的地方留空，不写估算值。

---

## 🧭 关于我

- 🎓 **硕士在读**：湖南工商大学 · 人工智能（2026 级）
- 🔬 我在意的问题：**怎么判断一个评测结论是真的**。同一份结果，用总体标准差还是样本标准差、上锚点是拍脑袋还是事先声明、Dev 和 Test 有没有串用，会得出完全相反的结论。这个方向不性感，但它决定一个 benchmark 值不值得信。
- 🧰 工程习惯：`uv` 锁依赖、`ruff` + `mypy`、pytest/unittest、GitHub Actions 每次 push 跑测试、Conventional Commits、每个结论附复现命令。
- 🌱 学习观：**公开可验证的产出 > 收藏的书单**。所以我把学习过程做成仓库，而不是做成笔记。
- 🤝 欢迎交流：评测方法论、推理效率、怎么给一个 benchmark 做「质检」。

## 📂 精选项目

<table>
<tr>
<td width="50%" valign="top">

### 🧪 [eval-kit](https://github.com/wang2067562393-dot/eval-kit)

**评测的判定层**

3σ 幅度门槛、归一化评分、成对对照；任务包发布前的 13 条静态自检规则（答案泄漏、清单哈希、超时缺失）。

`Python` `统计` `CI` `零依赖`

</td>
<td width="50%" valign="top">

### ⚡ [llm-inference-efficiency-notes](https://github.com/wang2067562393-dot/llm-inference-efficiency-notes)

**推理效率笔记 + 可运行工具**

Prefill / Decode 两段的瓶颈拆解；KV 显存估算、配对多 seed 统计、NumPy 手写 Attention。

`LLM` `KV Cache` `投机解码`

</td>
</tr>
<tr>
<td valign="top">

### 🔬 [chip-test-automation](https://github.com/wang2067562393-dot/chip-test-automation)

**芯片测试日志自动化**

UWB 功能/可靠性测试的 Log 解析、跨固件版本配对对比、3σ / MAD 异常检测。

`Python` `日志` `异常检测`

</td>
<td valign="top">

### 🗂 [ai-plan-2029](https://github.com/wang2067562393-dot/ai-plan-2029)

**按周交付的补强日志**

GPU 基准、多镜像降级的数据获取、纯函数化的可测试分析。

`uv` `PyTorch` `数据工程`

</td>
</tr>
</table>

## 🎯 评测方法论：我认为最容易出错的地方

这部分是我从实际交付里踩出来的，写在这里是因为它比代码更能说明我怎么想问题。

| 约定 | 常见的错法 | 后果 |
|---|---|---|
| 3σ 用 **Baseline 的样本标准差**（n−1） | 用总体标准差、或错用配对差值的标准差 | 波动被低估，改善显得更显著 |
| 上锚点 U **事先声明** | 用 Reference 的成绩反推 U | 分数恒等于 1，判定失去意义 |
| 单位统一 | 小数和百分数混用 | Δ 和 σ 差 100 倍，且程序不报错 |
| Dev / Test 隔离 | 拿私有 Test 的反馈反复调方法 | 最终分数不可信（等价于污染） |
| σ = 0 时不谈倍数 | 把「无穷大倍改善」当强证据 | 通常意味着 seed 没真正独立 |
| 幅度门槛 ≠ 统计检验 | 把 3σ 说成「99.7% 概率有效」 | 结论被夸大到无法辩护 |

这些规则我没有停在文档里：`eval-kit` 把它们实现成会抛异常、会报警的函数，并且有测试盯着。

## 🛠 技术栈

**语言**
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?logo=c&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-4EAA25?logo=gnubash&logoColor=white)

**AI / 数据**
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![HuggingFace](https://img.shields.io/badge/HuggingFace-FFD21E?logo=huggingface&logoColor=black)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![pandas](https://img.shields.io/badge/pandas-150458?logo=pandas&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white)

**工程**
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/CI-GitHub%20Actions-2088FF?logo=githubactions&logoColor=white)

## 🌱 我正在补什么

- **深度学习地基**：不满足于「会调库」。正在用 RTX 4060 从零手写 CNN 与 Attention，每个部件都要能解释梯度和显存。
- **C++**：目前只到「能读、能改小模块」，目标是能写一个固定步长的实时循环。
- **评测的规模化**：`eval-kit` 目前只做静态检查，下一步是把「方法空间是否成立」和「评分是否可复现」也变成可自动化的检查。

我把短板写在这里，是因为面试时反正会被问到，不如先自己说出来。

## 📍 2026 – 2027 里程碑

- [x] `eval-kit` v0.1：统计判定 + 13 条自检规则 + CI
- [x] GPU 基准与开发环境工程化（uv / ruff / pre-commit / Actions）
- [ ] 从零手搓 CNN 完成 CIFAR-10 全流程（不复制教程）
- [ ] 从零实现 Attention / Transformer 关键模块并验证数值
- [ ] 用 0.5B 级小模型实测 KV Cache 与投机解码的显存/延迟，替换笔记里的公式估算
- [ ] LeetCode 150 题
- [ ] 大模型评测 / 推理优化方向实习

## 📫 联系我

- 📧 邮箱：**wang2067562393@gmail.com**
- 💬 长沙线下 / 远程均可，欢迎前辈内推与技术交流

<div align="center">

*If you can't measure it, you can't claim it.*

</div>

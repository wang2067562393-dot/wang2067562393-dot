<div align="center">

# 你好，我是 王同学 👋

**AI 方向硕士研一在读 · 把「感觉」翻译成数字**

`实时链路测量` · `评测判定与质量门` · `推理效率` · `测试自动化`

<a href="mailto:wang2067562393@gmail.com"><img src="https://img.shields.io/badge/Gmail-wang2067562393@gmail.com-D14836?logo=gmail&logoColor=white"></a>
<img src="https://img.shields.io/badge/长沙-中国-00B96B?logo=openstreetmap&logoColor=white">
<img src="https://img.shields.io/badge/2027寒假实习-求职中-FF6A00">
<img src="https://img.shields.io/badge/关注-结论的可信度-6366F1">

</div>

---

## ⏱ 30 秒看懂

| 项目 | 它回答什么问题 | 可验证的结果 |
|---|---|---|
| **[teleop-link-lab](https://github.com/wang2067562393-dot/teleop-link-lab)** | 遥操作链路里，延迟来自哪一段？该降级还是该修？ | 基线往返 **0.4 ms**；注入 100 ms 单向 → 实测往返 **203.8 ms**、画面 **110.0 ms**；6 场景实验表 + **60 个测试** |
| **[llm-inference-efficiency-notes](https://github.com/wang2067562393-dot/llm-inference-efficiency-notes)** | 怎么判断一个「提升」是真的？ | 内置 `evalkit`：3σ 幅度门槛 + 归一化评分 + 13 条任务包自检规则，**43 个测试**，零依赖 |
| **[chip-test-automation](https://github.com/wang2067562393-dot/chip-test-automation)** | 怎么把「人工翻几千行 Log」变成一条命令？ | 跨固件对比：通过率 33.3% → 83.3%（虚构示例数据） |
| **[ai-plan-2029](https://github.com/wang2067562393-dot/ai-plan-2029)** | 每周一个可运行交付，怎么坚持？ | FP32 13.72 → FP16 31.68 TFLOPS（RTX 4060 Laptop 实测） |

> 只写自己跑过、能复现的数字。跑不出来的地方留空，不写估算值。

---

## 🧭 一条主线

看起来我做的两件事不相干：一边是大模型评测的统计学，一边是遥操作链路的延迟测量。其实是同一个问题——

> **你怎么知道一个结论是真的？**

在评测里，答案是 Baseline 的样本标准差、事先声明的上锚点、Dev/Test 不许回灌。
在实时链路里，答案是单调时钟、分位数、以及**先证明测量工具没坏**。

后者我吃过亏：基线第一次测出 30.6 ms，一路查到 Windows 定时器粒度、`loop.time()` 的 15.6 ms 分辨率、
最后发现延迟注入器会**提前 6 ms** 触发。修完之后基线是 0.4 ms。完整过程写在仓库的「调试记录」里，
我认为那三节比代码更能说明我怎么工作。

## 📂 精选项目

<table>
<tr>
<td width="50%" valign="top">

### 🎮 [teleop-link-lab](https://github.com/wang2067562393-dot/teleop-link-lab)

控制端 → 弱网代理 → 模拟机器人 → 视频回流，全链路打点。自研延迟/抖动/丢包注入器（独立线程排程），降级策略带回滞。

`Python` `asyncio` `UDP` `实时测量`

</td>
<td width="50%" valign="top">

### ⚡ [llm-inference-efficiency-notes](https://github.com/wang2067562393-dot/llm-inference-efficiency-notes)

KV Cache / 视觉 Token / 投机解码的瓶颈拆解，外加 `evalkit`：把评测纪律写成会抛错的代码。

`LLM` `3σ 判定` `质量门` `零依赖`

</td>
</tr>
<tr>
<td valign="top">

### 🔬 [chip-test-automation](https://github.com/wang2067562393-dot/chip-test-automation)

UWB 芯片测试的日志解析、跨固件版本配对对比、3σ / MAD 异常检测。

`Python` `日志` `异常检测`

</td>
<td valign="top">

### 🗂 [ai-plan-2029](https://github.com/wang2067562393-dot/ai-plan-2029)

按周交付的系统补强日志：GPU 基准、多镜像降级的数据获取、纯函数化分析。

`uv` `PyTorch` `数据工程`

</td>
</tr>
</table>

## 🛠 技术栈

**语言**
![Python](https://img.shields.io/badge/Python-3776AB?logo=python&logoColor=white)
![C](https://img.shields.io/badge/C-A8B9CC?logo=c&logoColor=black)
![Bash](https://img.shields.io/badge/Bash-4EAA25?logo=gnubash&logoColor=white)

**实时 / 网络**
![Linux](https://img.shields.io/badge/Linux-FCC624?logo=linux&logoColor=black)
![UDP](https://img.shields.io/badge/UDP%2FWebSocket-333333?logo=webrtc&logoColor=white)
![tcpdump](https://img.shields.io/badge/抓包-1679A7?logo=wireshark&logoColor=white)
![ffmpeg](https://img.shields.io/badge/ffmpeg-007808?logo=ffmpeg&logoColor=white)

**AI / 数据**
![PyTorch](https://img.shields.io/badge/PyTorch-EE4C2C?logo=pytorch&logoColor=white)
![NumPy](https://img.shields.io/badge/NumPy-013243?logo=numpy&logoColor=white)
![OpenCV](https://img.shields.io/badge/OpenCV-5C3EE8?logo=opencv&logoColor=white)

**工程**
![Git](https://img.shields.io/badge/Git-F05032?logo=git&logoColor=white)
![Docker](https://img.shields.io/badge/Docker-2496ED?logo=docker&logoColor=white)
![GitHub Actions](https://img.shields.io/badge/CI-GitHub%20Actions-2088FF?logo=githubactions&logoColor=white)

## 🌱 我正在补什么

- **深度学习地基**：不满足于「会调库」。正在用 RTX 4060 从零手写 MLP / CNN / Attention，每一块都要能解释梯度和显存。
- **C++**：目前只到「能读、能改小模块」，目标是能写固定步长的实时循环。
- **真机**：上面所有链路都是本机回环 + 注入器。下一步要上真机/真网络，把「注入的延迟」换成「测出来的延迟」。

短板写在这里，是因为面试时反正会被问到。

## 📍 里程碑

- [x] `teleop-link-lab` v0.1：60 个测试 + 6 场景实验报告
- [x] `evalkit` 合入 llm 仓库：43 个测试，13 条自检规则
- [ ] 从零手搓 CNN 完成 CIFAR-10 全流程
- [ ] 从零实现 Attention / Transformer 并做数值对齐
- [ ] 0.5B 级小模型实测 KV Cache 与投机解码，替换笔记里的公式估算
- [ ] H.264 串流路径 + 玻璃到玻璃延迟校准

## 📫 联系我

- 📧 **wang2067562393@gmail.com**
- 💬 长沙本地，欢迎前辈内推与技术交流

<div align="center">

*If you can't measure it, you can't claim it.*

</div>

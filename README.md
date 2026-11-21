<div align="center">

# 王同学

**硕士在读（人工智能）· 长沙**

实时链路测量 · 评测判定 · 测试自动化

<a href="mailto:wang2067562393@gmail.com">wang2067562393@gmail.com</a> ·
<a href="https://github.com/wang2067562393-dot">GitHub</a> · 2027 寒假实习求职中

</div>

---

研一在读，湖南工商大学人工智能专业。做过一批大模型评测任务包的构建与质检：冻结评测协议、做 baseline 与 reference 的成对多 seed 对照、用 3σ 与归一化评分判定改善是否成立。现在在做遥操作链路的延迟测量。

我的工程习惯只有一条：**先证明测量工具没坏，再去测别人的东西。** 基线第一次测出 30.6 ms 时，我没有去优化系统，而是花时间查到 Windows 定时器粒度和延迟注入器提前触发的问题——修完之后基线是 0.4 ms。

## 项目

**[teleop-link-lab](https://github.com/wang2067562393-dot/teleop-link-lab)** · 遥操作链路实验台
控制端 → 弱网代理 → 机器人 → 视频回流，全链路打点，自研延迟/抖动/丢包注入器。
`Python` `asyncio` `UDP` — 基线往返 **0.4 ms**，100 ms 单向注入实测往返 **203.8 ms**，60 个测试

**[llm-inference-efficiency-notes](https://github.com/wang2067562393-dot/llm-inference-efficiency-notes)** · 推理效率笔记 + 评测工具
KV Cache 压缩 / 视觉 Token 削减 / 投机解码的瓶颈拆解，附 `evalkit`（3σ 门槛、归一化评分、13 条任务包自检）。
`LLM` `统计` `CI` — 43 个测试

**[chip-test-automation](https://github.com/wang2067562393-dot/chip-test-automation)** · 芯片测试日志自动化
UWB 功能与可靠性测试的 Log 解析、跨固件版本配对对比、3σ / MAD 异常检测。
`Python` — 跨固件通过率 33.3% → 83.3%（虚构示例数据）

**[ai-plan-2029](https://github.com/wang2067562393-dot/ai-plan-2029)** · 按周交付的系统补强日志
GPU 基准、多镜像降级的数据获取、纯函数化的可测试分析。
`PyTorch` `uv` — FP32 13.72 → FP16 31.68 TFLOPS（RTX 4060 Laptop 实测）

## 技能

**语言** Python（熟练）· C · Bash
**方向** 评测判定（3σ / 归一化评分 / 质量门）· 实时链路测量（延迟 / 抖动 / 丢包 / 降级）· 数据与测试自动化
**工具** Linux · Git / GitHub Actions · Docker · PyTorch · NumPy · OpenCV · ffmpeg

## 现在

- 在补深度学习地基：从零手写 MLP / CNN / Attention，每一块都要能解释梯度和显存
- 在找大模型评测、推理效率、机器人实时链路方向的实习（长沙线下或远程）
- 短板写在明处：没有真机经验，C++ 只到能读、能改小模块

<div align="center">

*If you can't measure it, you can't claim it.*

</div>

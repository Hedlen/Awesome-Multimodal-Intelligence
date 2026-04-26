<div align="center">

<img src="./imgs/vlm_teaser.png" width="45%"> <img src="./imgs/vla_teaser.png" width="45%">

# Awesome Multimodal Intelligence

[![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![PRs Welcome](https://img.shields.io/badge/PRs-Welcome-red)
![Stars](https://img.shields.io/github/stars/yourusername/yourrepo?style=social)

专注于 VLM、VLA、世界模型及通用具身智能等方向，收录前沿论文、开源代码与数据集，追踪从感知到决策的下一代智能体技术。

A curated collection for multimodal intelligence research, covering VLMs, VLAs, World Models, and embodied AI — tracking next-generation agent technologies from perception to decision-making, with a focus on papers, code, and datasets.

如果本仓库对你有帮助，欢迎 Star ⭐ 或分享 ⬆️，感谢支持！  
If you find this repository helpful, please consider Stars ⭐ or Sharing ⬆️. Thanks.

</div>

---

## 📌 News

- **2026.4**: 全面更新 VLM（新增 SigLIP/SigLIP2、Qwen2.5-VL、Qwen3-VL、InternVL3、Molmo、Emu3 等），新增世界模型与具身 AI 专题，补全训练数据集与评估 Benchmark。
- **2026.4**: Major update — added SigLIP/SigLIP2, Qwen2.5-VL, Qwen3-VL, InternVL3, Molmo, Emu3 to VLMs; launched World Models and Embodied AI collections with full datasets and benchmarks.

---

## 📂 Collection Index

| Topic　　　　　　　　　　　　　　　　　　　 | Description　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　　| Link　　　　　　　　　　　　　　　　　　　　　　　　　　　　　|
| :--------------------------------------------| :-------------------------------------------------------------------------------------------| :-------------------------------------------------------------:|
| 🖼️ **Vision Language Models (VLMs)**　　　　| 视觉语言模型：感知、理解与多模态推理 / Perception, understanding, and multimodal reasoning | [📄 View](./mdfiles/Awesome-Vision-Language-Models.md)　　　　|
| 🤖 **Vision Language Action Models (VLAs)** | 视觉语言动作模型：从感知到物理决策 / From perception to physical decision-making　　　　　 | [📄 View](./mdfiles/Awesome-Vision-Language-Action-Models.md) |
| 🌍 **World Models**　　　　　　　　　　　　 | 世界模型：环境建模与预测性规划 / Environment modeling and predictive planning　　　　　　　| [📄 View](./mdfiles/Awesome-World-Models.md)　　　　　　　　　|
| 🧠 **Embodied AI**　　　　　　　　　　　　　| 通用具身智能：感知、规划与执行的统一 / Unified perception, planning, and execution　　　　 | [📄 View](./mdfiles/Awesome-Embodied-AI.md)　　　　　　　　　 |

---

## 🗺️ Research Landscape

```
Perception ──► Understanding ──► Reasoning ──► Planning ──► Action
    │               │                │              │           │
   VLMs            VLMs 
Perception ──► Understanding ──► Reasoning ──► Planning ──► Action
    │               │                │              │           │
   VLMs            VLMs             VLMs           VLAs        VLAs
                                  World Models   World Models  Embodied AI
```

- **VLMs** 负责视觉感知与语言理解的桥接，是整个智能体栈的感知基础。
- **VLAs** 在 VLM 基础上引入动作输出，实现端到端的感知-决策闭环。
- **World Models** 对环境动态建模，为规划提供预测性先验。
- **Embodied AI** 整合上述能力，面向真实世界的通用智能体。

---

## 🔖 Quick Links

- [Awesome VLMs →](ed VLMs (LLaVA series, InternVL3, Qwen3-VL, Qwen2.5-VL, Idefics3)
  - Grounding & Localization (KOSMOS-2, Grounding DINO 1.5, SAM2)
  - Efficient VLMs (PaliGemma2, Phi-4-Vision, SmolVLM)
  - Proprietary VLMs (GPT-4o, Gemini 2.0, Claude 3.5)
  - Training Datasets (LAION-5B, DataComp, MMC4, PixMo)
  - Benchmarks (MMMU-Pro, MMStar, MathVista, Video-MME)

- [Awesome VLAs →](./mdfiles/Awesome-Vision-Language-Action-Models.md)
  - Foundational Policies (ACT, Diffusion Policy, RT-1, SayCan)
  - VLA Base Models (RT-2, OpenVLA, π0, π0.5)
  - Generalist Policies (Octo, CrossFormer)
  - Manipulation, Navigation, Dexterous Control
  - RL & Self-Improvement (OpenVLA-OFT, VLARL)
  - Datasets & Benchmarks (Open X-Embodiment, LIBERO, CALVIN)

- [Awesome World Models →](./mdfiles/Awesome-World-Models.md)
  - Model-Based RL (DreamerV3, TD-MPC2, MuZero, IRIS)
  - JEPA (I-JEPA, V-JEPA, V-JEPA2)
  - Video Generation (Sora, Cosmos, Genie2, DIAMOND)
  - Autonomous Driving (GAIA-1, DriveDreamer, Vista, OccWorld)
  - Robot World Models (UniSim, GR-1, UniPi, Pandora)
  - Benchmarks (VBench, EvalCrafter, nuPlan, CARLA)

- [Awesome Embodied AI →](./mdfiles/Awesome-Embodied-AI.md)
  - Perception (EmbodiedScan, ConceptFusion, AnyGrasp)
  - Navigation (NavGPT2, ViNT, NoMaD, CoW)
  - Manipulation (RVT-2, Diffusion Policy, 3D Diffusion Policy)
  - Task Planning (SayCan, Code-as-Policies, Voyager, ReKep)
  - General Agents (Gato, OpenVLA, π0, Octo, LEO)
  - Humanoid (Figure02, HumanPlus, OmniH2O, DexVLA)
  - Simulators (Isaac Lab, ManiSkill3, Habitat 3.0, Genesis)
  - Benchmarks (CALVIN, MetaWorld, EmbodiedBench, BEHAVIOR-1K)

---

## 🤝 Contributing

欢迎提交 PR 补充新论文、数据集或工具！请遵循各子文档的表格格式。

PRs are welcome to add new papers, datasets, or toolkits. Please follow the table format in each sub-document.

1. Fork 本仓库
2. 在对应的 `.md` 文件中添加条目
3. 提交 Pull Request，简要说明新增内容

---

## 📜 License

This project is released under the [MIT License](./LICENSE).

---

<div align="center">
<sub>Maintained with ❤️ — tracking the frontier of multimodal intelligence</sub>
</div>

<div align="center">
<br>
<image src="./imgs/vla_teaser.png", width="900px", height="300px">
<br>
</div>

# Awesome Vision Language Action Models (VLAs) [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

Vision-Language-Action (VLA) models represent a paradigm shift in robotics, unifying visual perception, language understanding, and physical action generation into a single end-to-end learnable system. This repository continuously tracks and summarizes the research progress of VLA models across foundational works, manipulation, navigation, and open-source toolkits.

If you find this repository helpful, please consider Stars ⭐ or Sharing ⬆️. Thanks.

## News
- 2026.4: Initial release — covering foundational policies (ACT, Diffusion Policy, RT-1, SayCan, PaLM-E), VLA base models (RT-2, RT-X, OpenVLA, π0, RoboFlamingo, CLIP-RT), generalist policies (Octo, CrossFormer), manipulation works (GR-1, Mobile ALOHA, VLA-0, UniVLA, SuSIE, Instruct2Act), navigation (NavGPT, EmbodiedScan), dexterous control (π0.5, DexVLA), RL self-improvement (Recap, VLARL, OpenVLA-OFT), efficient VLAs (OTTER, TinyVLA), datasets & benchmarks (Open X-Embodiment, LIBERO, CALVIN, RLBench, ALOHA, BridgeData V2), and toolkits (openpi, LeRobot, open-pi-zero).

## Contents

- [Foundational Papers](#foundational-papers)
  - [Language-Conditioned Robot Policies](#language-conditioned-robot-policies)
  - [VLA Base Models](#vla-base-models)
  - [Generalist Robot Policies](#generalist-robot-policies)
- [Derivative Papers](#derivative-papers)
  - [Manipulation](#manipulation)
  - [Navigation](#navigation)
  - [Dexterous and Bimanual Control](#dexterous-and-bimanual-control)
  - [RL and Self-Improvement](#rl-and-self-improvement)
  - [Efficient VLAs](#efficient-vlas)
- [Datasets and Benchmarks](#datasets-and-benchmarks)
- [Projects and Toolkits](#projects-and-toolkits)

## Papers / Projects

### Foundational Papers

#### Language-Conditioned Robot Policies
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| SayCan | ![img](https://say-can.github.io/assets/saycan_teaser.gif) | [CoRL2022](https://arxiv.org/abs/2204.01691) | [Project](https://say-can.github.io/) | [Code](https://github.com/google-research/google-research/tree/master/saycan) | Google | Grounds LLM planning in robot affordances; uses value functions to score which skills are both useful and feasible. |
| PaLM-E | ![img](https://palm-e.github.io/assets/palm-e-teaser.gif) | [arXiv](https://arxiv.org/abs/2303.03378) | [Project](https://palm-e.github.io/) | - | Google | A 562B embodied multimodal LLM that ingests robot sensor data directly; enables multi-step planning and manipulation. |
| RT-1 | ![img](https://robotics-transformer1.github.io/img/rt1.gif) | [RSS2023](https://arxiv.org/abs/2212.06817) | [Project](https://robotics-transformer1.github.io/) | [Code](https://github.com/google-research/robotics_transformer) | Google | Robotics Transformer trained on 130k real-robot demonstrations; efficient tokenization of images and actions. |
| ACT | ![img](https://tonyzhaozh.github.io/aloha/resources/act_teaser.gif) | [RSS2023](https://arxiv.org/abs/2304.13705) | [Project](https://tonyzhaozh.github.io/aloha/) | [Code](https://github.com/tonyzhaozh/act) | Stanford | Action Chunking with Transformers; predicts sequences of actions to reduce compounding errors in imitation learning. |
| Diffusion Policy | ![img](https://diffusion-policy.cs.columbia.edu/diffusion_policy_teaser.jpg) | [RSS2023](https://arxiv.org/abs/2303.04137) | [Project](https://diffusion-policy.cs.columbia.edu/) | [Code](https://github.com/real-stanford/diffusion_policy) | Columbia | Visuomotor policy learning via conditional denoising diffusion; handles multimodal action distributions robustly. |

#### VLA Base Models
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| RT-2 | ![img](https://robotics-transformer2.github.io/img/rt2.png) | [CoRL2023](https://arxiv.org/abs/2307.15818) | [Project](https://robotics-transformer2.github.io/) | - | Google DeepMind | First VLA to co-fine-tune a VLM (PaLI-X / PaLM-E) on robot data; emergent semantic reasoning and chain-of-thought planning. |
| RT-X | - | [ICRA2024](https://arxiv.org/abs/2310.08864) | [Project](https://robotics-transformer-x.github.io/) | [Code](https://github.com/google-deepmind/open_x_embodiment) | Google DeepMind & 33 labs | Scales RT-2 training across the Open X-Embodiment dataset; demonstrates cross-embodiment generalization at scale. |
| OpenVLA | - | [CoRL2024](https://arxiv.org/abs/2406.09246) | [Project](https://openvla.github.io/) | [Code](https://github.com/openvla/openvla) | Stanford & Berkeley | Open-source 7B VLA based on Prismatic VLM; outperforms RT-2-X (55B) by 16.5% with 7× fewer parameters. |
| π0 (pi-zero) | ![img](https://www.physicalintelligence.company/images/pi0-teaser.gif) | [arXiv](https://arxiv.org/abs/2410.24164) | [Blog](https://www.physicalintelligence.company/blog/pi0) | [Code](https://github.com/Physical-Intelligence/openpi) | Physical Intelligence | A VLA flow model for general robot control; uses flow matching for continuous action generation across diverse tasks. |
| RoboFlamingo | - | [ICLR2024](https://arxiv.org/abs/2311.01378) | [Project](https://roboflamingo.github.io/) | [Code](https://github.com/RoboFlamingo/RoboFlamingo) | ByteDance | Fine-tunes OpenFlamingo as a robot imitator with an explicit policy head; strong on CALVIN manipulation benchmark. |
| CLIP-RT | - | [arXiv](https://arxiv.org/abs/2411.00508) | - | [Code](https://github.com/clip-rt/clip-rt) | - | Learns robot policies directly from natural language supervision using CLIP; enables zero-shot generalization to new instructions. |

#### Generalist Robot Policies
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Octo | ![img](https://octo-models.github.io/octo-teaser.gif) | [RSS2024](https://arxiv.org/abs/2405.12213) | [Project](https://octo-models.github.io/) | [Code](https://github.com/octo-models/octo) | UC Berkeley | Open-source generalist robot policy (93M) trained on 800k trajectories from Open X-Embodiment; easy to fine-tune. |
| CrossFormer | - | [arXiv](https://arxiv.org/abs/2408.11812) | [Project](https://crossformer-model.github.io/) | - | UC Berkeley | Scalable transformer policy trained on 900k trajectories across 20 embodiments; first to achieve SoTA across 6 embodiment types. |
| Open X-Embodiment | - | [ICRA2024](https://arxiv.org/abs/2310.08864) | [Project](https://robotics-transformer-x.github.io/) | [Code](https://github.com/google-deepmind/open_x_embodiment) | Google DeepMind & 33 labs | A large-scale robot learning dataset with 1M+ trajectories from 22 robot embodiments; enables cross-embodiment generalization. |

### Derivative Papers

#### Manipulation
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| GR-1 | ![img](https://gr1-manipulation.github.io/static/images/teaser.gif) | [ICLR2024](https://arxiv.org/abs/2312.13139) | [Project](https://gr1-manipulation.github.io/) | [Code](https://github.com/bytedance/GR-1) | ByteDance | GPT-style transformer pre-trained on large-scale video data; jointly predicts robot actions and future frames. |
| ACT+ (Mobile ALOHA) | - | [arXiv](https://arxiv.org/abs/2401.02117) | [Project](https://mobile-aloha.github.io/) | [Code](https://github.com/MarkFzp/mobile-aloha) | Stanford | Extends ACT to whole-body mobile manipulation; learns complex household tasks via imitation learning. |
| VLA-0 | - | [arXiv](https://arxiv.org/abs/2510.13054) | - | - | - | Represents actions directly as text tokens with zero VLM modification; outperforms π0 on LIBERO benchmark. |
| UniVLA | - | [arXiv](https://arxiv.org/abs/2505.06111) | - | - | - | Unified VLA framework with task-centric latent actions; enables policy learning across embodiments without action labels. |
| SuSIE | - | [arXiv](https://arxiv.org/abs/2311.12871) | [Project](https://rail-berkeley.github.io/susie/) | - | UC Berkeley | Zero-shot robot manipulation via subgoal synthesis using internet-pretrained video diffusion models. |
| Instruct2Act | ![img](https://github.com/OpenGVLab/Instruct2Act/raw/main/images/instruct2act_framework.png) | [arXiv](https://arxiv.org/abs/2305.11176) | - | [Code](https://github.com/OpenGVLab/Instruct2Act) | OpenGVLab | Maps multi-modal instructions to robot actions via Python programs; uses SAM for object grounding. |
| LLaVA-VLA | - | - | - | [Code](https://github.com/OpenHelix-Team/LLaVA-VLA) | OpenHelix | A simple yet powerful VLA model built on LLaVA; actively maintained with strong manipulation performance. |

#### Navigation
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| NavGPT | - | [arXiv](https://arxiv.org/abs/2305.16986) | - | [Code](https://github.com/GengzeZhou/NavGPT) | - | Explicit reasoning for vision-and-language navigation using GPT-4 as a zero-shot navigator. |
| EmbodiedScan | - | [CVPR2024](https://arxiv.org/abs/2312.16170) | [Project](https://tai-wang.github.io/embodiedscan/) | [Code](https://github.com/OpenRobotLab/EmbodiedScan) | Shanghai AI Lab | A holistic multi-modal 3D perception suite for embodied AI; covers detection, VQA, and grounding in 3D scenes. |

#### Dexterous and Bimanual Control
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| π0.5 | - | [arXiv](https://arxiv.org/abs/2504.16054) | [Blog](https://www.physicalintelligence.company/blog/pi05) | - | Physical Intelligence | Extends π0 with open-world generalization; trained on diverse real-world data for deployment outside the lab. |
| DexVLA | - | [arXiv](https://arxiv.org/abs/2502.05855) | - | - | - | VLA with a plug-in diffusion transformer for dexterous manipulation; decouples high-level reasoning from low-level control. |

#### RL and Self-Improvement
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| RLVR for VLA | - | [arXiv](https://arxiv.org/abs/2511.14759) | - | - | Physical Intelligence | Recap: RL with experience and corrections via advantage-conditioned policies; enables VLAs to improve from real-world deployment. |
| VLARL | - | - | - | [Code](https://github.com/GuanxingLu/vlarl) | - | Single-file implementation for advancing VLA models with reinforcement learning; minimal and extensible. |
| OpenVLA-OFT | - | [arXiv](https://arxiv.org/abs/2412.06173) | - | [Code](https://github.com/openvla/openvla-oft) | Stanford | Efficient fine-tuning of OpenVLA with parallel decoding and action chunking; 6× faster inference than base OpenVLA. |

#### Efficient VLAs
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| OpenVLA-OFT | - | [arXiv](https://arxiv.org/abs/2412.06173) | - | [Code](https://github.com/openvla/openvla-oft) | Stanford | Efficient fine-tuning of OpenVLA with parallel decoding and action chunking; 6× faster inference than base OpenVLA. |
| OTTER (VLA) | - | [arXiv](https://arxiv.org/abs/2503.03734) | - | - | - | Selectively extracts task-relevant visual features aligned with language instructions; keeps VLM encoders frozen. |
| TinyVLA | - | [arXiv](https://arxiv.org/abs/2409.12514) | - | [Code](https://github.com/lesjie-wen/tinyvla) | - | A compact VLA that achieves competitive performance with much smaller model size; suitable for edge deployment. |

### Datasets and Benchmarks
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Open X-Embodiment | - | [ICRA2024](https://arxiv.org/abs/2310.08864) | [Project](https://robotics-transformer-x.github.io/) | [Code](https://github.com/google-deepmind/open_x_embodiment) | Google & 33 labs | 1M+ robot trajectories from 22 embodiments; the largest cross-embodiment robot learning dataset to date. |
| LIBERO | - | [NeurIPS2023](https://arxiv.org/abs/2306.03310) | [Project](https://libero-project.github.io/) | [Code](https://github.com/Lifelong-Robot-Learning/LIBERO) | UNC | Benchmark for lifelong robot learning with 130 language-conditioned manipulation tasks across 4 task suites. |
| CALVIN | - | [RA-L2022](https://arxiv.org/abs/2112.03227) | [Project](http://calvin.cs.uni-freiburg.de/) | [Code](https://github.com/mees/calvin) | University of Freiburg | A benchmark for language-conditioned long-horizon robot manipulation with 34 tasks in 4 environments. |
| RLBench | - | [RA-L2020](https://arxiv.org/abs/1909.12271) | [Project](https://sites.google.com/view/rlbench) | [Code](https://github.com/stepjam/RLBench) | Imperial College London | A large-scale benchmark with 100 unique robot manipulation tasks for imitation and reinforcement learning. |
| ALOHA / ALOHA 2 | - | [RSS2023](https://arxiv.org/abs/2304.13705) | [Project](https://tonyzhaozh.github.io/aloha/) | [Code](https://github.com/tonyzhaozh/aloha) | Stanford | Low-cost bimanual teleoperation hardware + dataset; the platform behind ACT and Mobile ALOHA. |
| BridgeData V2 | - | [arXiv](https://arxiv.org/abs/2308.12952) | [Project](https://rail-berkeley.github.io/bridgedata/) | [Code](https://github.com/rail-berkeley/bridge_data_v2) | UC Berkeley | 60k+ robot trajectories across 24 environments; widely used for training and evaluating generalist robot policies. |

### Projects and Toolkits
| Title | Presentation | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|
| openpi (π0) | - | [Blog](https://www.physicalintelligence.company/blog/pi0) | [Code](https://github.com/Physical-Intelligence/openpi) | Physical Intelligence | Official open-source release of the π0 VLA model with training and inference code. |
| open-pi-zero | - | - | [Code](https://github.com/allenzren/open-pi-zero) | Community | Community re-implementation of the π0 VLA model; useful for research and experimentation. |
| Awesome Embodied VLA | - | - | [Code](https://github.com/jonyzhang2023/awesome-embodied-vla-va-vln) | Community | Curated list of VLA, VLN, and embodied learning papers; actively maintained. |
| Awesome Robotics Foundation Models | - | - | [Code](https://github.com/robotics-survey/Awesome-Robotics-Foundation-Models) | Community | Partner repository for the survey "Foundation Models in Robotics: Applications, Challenges, and the Future". |
| LeRobot | - | [Blog](https://huggingface.co/blog/lerobot) | [Code](https://github.com/huggingface/lerobot) | HuggingFace | State-of-the-art robot learning library with pre-trained models, datasets, and simulation environments. |

## Acknowledgement
Some of the presentations in this repository are borrowed from the original authors, and we are very thankful for their contributions.

## License
This project is released under the MIT license.

<div align="center">
<br>
<img src="https://worldmodels.github.io/assets/world_model.png" width="600px">
<br>
</div>

# Awesome World Models [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

World Models learn internal representations of environments to predict future states, enabling agents to plan, reason, and act without constant real-world interaction. This repository tracks research progress across model-based RL, video generation world models, autonomous driving world models, and robot world models.

If you find this repository helpful, please consider Stars ⭐ or Sharing ⬆️. Thanks.

## News
- 2026.4: Initial release — covering foundational world models (DreamerV3, JEPA), video generation (Sora, Cosmos), autonomous driving (GAIA-1, DriveDreamer), robot world models (UniSim, IRASim), and comprehensive benchmarks.

## Contents

- [Foundational Works](#foundational-works)
  - [Early World Models](#early-world-models)
  - [Model-Based RL World Models](#model-based-rl-world-models)
  - [Joint-Embedding Predictive Architectures](#joint-embedding-predictive-architectures)
- [Video Generation World Models](#video-generation-world-models)
- [Autonomous Driving World Models](#autonomous-driving-world-models)
- [Robot and Manipulation World Models](#robot-and-manipulation-world-models)
- [LLM-Based World Models](#llm-based-world-models)
- [Training Datasets](#training-datasets)
- [Benchmarks and Evaluation](#benchmarks-and-evaluation)
- [Projects and Toolkits](#projects-and-toolkits)

## Papers / Projects

### Foundational Works

#### Early World Models
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| World Models (Ha & Schmidhuber) | - | [NeurIPS2018](https://arxiv.org/abs/1803.10122) | [Project](https://worldmodels.github.io/) | [Code](https://github.com/hardmaru/WorldModels) | Google Brain | Seminal work learning compressed spatial and temporal representations; trains a compact controller in the dream. |
| PlaNet | - | [ICML2019](https://arxiv.org/abs/1811.04551) | [Project](https://planetrl.github.io/) | [Code](https://github.com/google-research/planet) | Google Brain | Deep Planning Network; learns latent dynamics models for planning from pixels with recurrent state-space models. |
| Dreamer | - | [ICLR2020](https://arxiv.org/abs/1912.01603) | [Project](https://danijar.com/project/dreamer/) | [Code](https://github.com/danijar/dreamer) | Google Brain | Learns long-horizon behaviors from images purely in latent space; actor-critic trained on imagined rollouts. |
| DreamerV2 | - | [ICLR2021](https://arxiv.org/abs/2010.02193) | [Project](https://danijar.com/project/dreamerv2/) | [Code](https://github.com/danijar/dreamerv2) | Google Brain | Mastering Atari with discrete world models; categorical representations improve sample efficiency. |
| DreamerV3 | - | [arXiv](https://arxiv.org/abs/2301.04104) | [Project](https://danijar.com/project/dreamerv3/) | [Code](https://github.com/danijar/dreamerv3) | Google DeepMind | Mastering diverse domains through world models; single set of hyperparameters works across all domains. |
| TD-MPC | - | [ICML2022](https://arxiv.org/abs/2203.04955) | [Project](https://nicklashansen.github.io/td-mpc/) | [Code](https://github.com/nicklashansen/tdmpc) | UCSD | Temporal Difference Learning for Model Predictive Control; combines latent world models with TD learning. |
| TD-MPC2 | - | [ICLR2024](https://arxiv.org/abs/2310.16828) | [Project](https://www.tdmpc2.com/) | [Code](https://github.com/nicklashansen/tdmpc2) | UCSD | Scalable, robust world models for continuous control; single model handles 80+ tasks across multiple domains. |

#### Model-Based RL World Models
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| MBPO | - | [NeurIPS2019](https://arxiv.org/abs/1906.08253) | - | [Code](https://github.com/jannerm/mbpo) | Berkeley | Model-Based Policy Optimization; short model rollouts with real data mixing for sample-efficient RL. |
| IRIS | - | [ICLR2023](https://arxiv.org/abs/2209.14430) | [Project](https://iris-minigpt.github.io/) | [Code](https://github.com/eloialonso/iris) | Geneva | Transformers as world models for Atari; discrete tokenization of observations enables autoregressive planning. |
| STORM | - | [NeurIPS2023](https://arxiv.org/abs/2310.09615) | - | [Code](https://github.com/weipu-zhang/STORM) | - | Efficient Stochastic Transformer-based World Models for Reinforcement Learning; strong on Atari 100K. |
| TWM | - | [NeurIPS2023](https://arxiv.org/abs/2301.03149) | - | [Code](https://github.com/jrobine/twm) | - | Transformer World Models; uses transformers for both world model and policy in model-based RL. |
| EfficientZero | - | [NeurIPS2021](https://arxiv.org/abs/2111.00210) | - | [Code](https://github.com/YeWR/EfficientZero) | Tsinghua | Achieves superhuman performance on Atari 100K with self-supervised consistency loss and look-ahead search. |
| MuZero | - | [Nature2020](https://arxiv.org/abs/1911.08265) | [Blog](https://deepmind.google/discover/blog/muzero-mastering-go-chess-shogi-and-atari-without-rules/) | - | DeepMind | Learns a model of the environment without knowing the rules; plans with learned value, policy, and reward. |

#### Joint-Embedding Predictive Architectures
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| I-JEPA | - | [CVPR2023](https://arxiv.org/abs/2301.08243) | [Blog](https://ai.meta.com/blog/yann-lecun-ai-model-i-jepa/) | [Code](https://github.com/facebookresearch/ijepa) | Meta | Image-based Joint-Embedding Predictive Architecture; learns abstract image representations without pixel reconstruction. |
| V-JEPA | - | [arXiv](https://arxiv.org/abs/2404.08471) | [Blog](https://ai.meta.com/blog/v-jepa-yann-lecun-ai-model-video-joint-embedding-predictive-architecture/) | [Code](https://github.com/facebookresearch/jepa) | Meta | Video JEPA; predicts abstract representations of future video frames without generating pixels. |
| V-JEPA 2 | - | [arXiv](https://arxiv.org/abs/2506.09985) | [Blog](https://ai.meta.com/blog/v-jepa-2-world-model-benchmark-planning/) | [Code](https://github.com/facebookresearch/vjepa2) | Meta | Self-supervised video world model enabling understanding, prediction, and planning; SoTA on physical reasoning. |
| MC-JEPA | - | [arXiv](https://arxiv.org/abs/2307.12698) | - | - | Meta | Multi-view Contrastive JEPA; extends JEPA to multi-view settings for richer world representations. |

### Video Generation World Models
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Sora | - | [Tech Report](https://openai.com/research/video-generation-models-as-world-simulators) | [Blog](https://openai.com/sora) | - | OpenAI | Video generation as world simulation; DiT-based model generating minute-long videos with physical consistency. |
| Cosmos | - | [arXiv](https://arxiv.org/abs/2501.03575) | [Project](https://www.nvidia.com/en-us/ai/cosmos/) | [Code](https://github.com/NVIDIA/Cosmos) | NVIDIA | World Foundation Model Platform for Physical AI; pre-trained video world models for robotics and AV. |
| Cosmos-Reason1 | - | [arXiv](https://arxiv.org/abs/2503.15558) | - | - | NVIDIA | Physical common sense reasoning for embodied decisions; chain-of-thought reasoning over physical world states. |
| VideoPoet | - | [ICML2024](https://arxiv.org/abs/2312.14125) | [Project](https://sites.research.google/videopoet/) | - | Google | Large language model for zero-shot video generation; handles text-to-video, image-to-video, and video editing. |
| Emu Video | - | [ECCV2024](https://arxiv.org/abs/2311.10709) | [Project](https://emu-video.metademolab.com/) | - | Meta | Factorized text-to-video generation; first generates an image then animates it with a video diffusion model. |
| CogVideo | - | [ICLR2023](https://arxiv.org/abs/2205.15868) | - | [Code](https://github.com/THUDM/CogVideo) | Tsinghua | Large-scale text-to-video generation with multi-frame-rate hierarchical training strategy. |
| CogVideoX | - | [arXiv](https://arxiv.org/abs/2408.06072) | - | [Code](https://github.com/THUDM/CogVideo) | Tsinghua | Expert transformer for video generation; 3D full attention with expert adaptive LayerNorm for text-video alignment. |
| Open-Sora | - | [arXiv](https://arxiv.org/abs/2412.00131) | - | [Code](https://github.com/hpcaitech/Open-Sora) | HPC-AI Tech | Open-source Sora reproduction; scalable video generation with efficient training and inference. |
| Open-Sora-Plan | - | - | - | [Code](https://github.com/PKU-YuanGroup/Open-Sora-Plan) | PKU | Open-source video generation framework; CausalVideoVAE with masked diffusion transformer. |
| HunyuanVideo | - | [arXiv](https://arxiv.org/abs/2412.03603) | [Project](https://aivideo.hunyuan.tencent.com/) | [Code](https://github.com/Tencent/HunyuanVideo) | Tencent | Open-source video generation model with 13B parameters; strong temporal consistency and motion quality. |
| Wan | - | [arXiv](https://arxiv.org/abs/2503.20314) | [Project](https://wan-video.github.io/) | [Code](https://github.com/Wan-Video/Wan2.1) | Alibaba | Open-source video generation with strong physical plausibility; supports text-to-video and image-to-video. |

### Autonomous Driving World Models
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| GAIA-1 | - | [arXiv](https://arxiv.org/abs/2309.17080) | [Blog](https://wayve.ai/thinking/introducing-gaia1/) | - | Wayve | Generative AI for Autonomy; generates realistic driving scenarios from video, text, and action inputs. |
| DriveDreamer | - | [ECCV2024](https://arxiv.org/abs/2309.09777) | [Project](https://drivedreamer.github.io/) | [Code](https://github.com/JeffWang987/DriveDreamer) | - | World model for autonomous driving; generates controllable driving videos conditioned on structured traffic constraints. |
| DriveDreamer-2 | - | [arXiv](https://arxiv.org/abs/2403.06845) | [Project](https://drivedreamer2.github.io/) | - | - | LLM-enhanced world model for diverse driving video generation; supports user-text-guided scenario creation. |
| UniSim | - | [CVPR2024](https://arxiv.org/abs/2308.01545) | [Project](https://waabi.ai/unisim/) | - | Waabi | A real-world simulator for autonomous driving; generates sensor-realistic data for closed-loop training. |
| WoVogen | - | [arXiv](https://arxiv.org/abs/2312.02235) | - | - | - | World volume-aware video generation for driving; 3D-consistent video synthesis with LiDAR-camera alignment. |
| GenAD | - | [CVPR2024](https://arxiv.org/abs/2403.09517) | - | - | - | Generalized predictive model for autonomous driving; unifies scene understanding and future prediction. |
| Vista | - | [NeurIPS2024](https://arxiv.org/abs/2405.17398) | [Project](https://vista-demo.github.io/) | [Code](https://github.com/OpenDriveLab/Vista) | OpenDriveLab | A generalizable driving world model with high fidelity; supports long-horizon prediction and action conditioning. |
| DriveX | - | [arXiv](https://arxiv.org/abs/2410.13571) | - | - | - | Generalizable world model for autonomous driving; cross-dataset transfer with unified scene representation. |
| MUVO | - | [arXiv](https://arxiv.org/abs/2311.11762) | - | - | - | Multimodal world model for autonomous driving with unified video and occupancy prediction. |
| OccWorld | - | [ECCV2024](https://arxiv.org/abs/2311.16038) | - | [Code](https://github.com/wzzheng/OccWorld) | PKU | Learning a 3D occupancy world model for autonomous driving; predicts future 3D occupancy and ego motion. |

### Robot and Manipulation World Models
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| UniSim (Robot) | - | [ICML2024](https://arxiv.org/abs/2406.14540) | [Project](https://universal-simulator.github.io/unisim/) | - | Stanford | A fine-grained world model for robot manipulation; predicts future frames conditioned on robot actions. |
| IRASim | - | [arXiv](https://arxiv.org/abs/2406.14540) | - | - | - | Interactive robot action simulation; generates realistic robot interaction videos for policy learning. |
| RoboDreamer | - | [arXiv](https://arxiv.org/abs/2406.13111) | [Project](https://robodreamer.github.io/) | - | - | Compositional world dreaming for robot manipulation; generates diverse training scenarios via world model. |
| SuSIE | - | [arXiv](https://arxiv.org/abs/2311.12871) | [Project](https://rail-berkeley.github.io/susie/) | - | UC Berkeley | Zero-shot robot manipulation via subgoal synthesis using internet-pretrained video diffusion world models. |
| GR-1 | - | [ICLR2024](https://arxiv.org/abs/2312.13139) | [Project](https://gr1-manipulation.github.io/) | [Code](https://github.com/bytedance/GR-1) | ByteDance | GPT-style world model pre-trained on video; jointly predicts future frames and robot actions. |
| UniPi | - | [ICLR2024](https://arxiv.org/abs/2302.01877) | [Project](https://universal-policy.github.io/unipi/) | - | Berkeley | Learning universal policies via text-guided video generation; plans by generating future video then extracting actions. |
| SWIM | - | [arXiv](https://arxiv.org/abs/2312.09256) | - | - | - | Scalable World Models for robot learning; efficient video prediction for diverse manipulation tasks. |
| Pandora | - | [arXiv](https://arxiv.org/abs/2406.09455) | [Project](https://world-pandora.github.io/) | - | - | Towards general world model with natural language actions and video generation for embodied agents. |

### LLM-Based World Models
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| LWM | - | [arXiv](https://arxiv.org/abs/2402.08438) | [Project](https://largeworldmodel.github.io/) | [Code](https://github.com/LargeWorldModel/LWM) | Berkeley | Large World Model; trains on long video and text sequences with RingAttention for 1M context understanding. |
| Genie | - | [ICML2024](https://arxiv.org/abs/2402.15391) | [Blog](https://deepmind.google/discover/blog/genie-generative-interactive-environments/) | - | Google DeepMind | Generative Interactive Environments; unsupervised learning of interactive worlds from internet videos. |
| Genie 2 | - | [Blog](https://deepmind.google/discover/blog/genie-2-a-large-scale-foundation-world-model/) | - | - | Google DeepMind | Large-scale foundation world model generating diverse 3D environments for agent training and evaluation. |
| GameNGen | - | [arXiv](https://arxiv.org/abs/2408.14837) | [Project](https://gamengen.github.io/) | - | Google | Neural game engine running DOOM in real-time; diffusion model as interactive world simulator. |
| DIAMOND | - | [NeurIPS2024](https://arxiv.org/abs/2405.12399) | [Project](https://diamond-wm.github.io/) | [Code](https://github.com/eloialonso/diamond) | Geneva | Diffusion for World Modeling; uses diffusion models as world models for RL; SoTA on Atari 100K. |
| iVideoGPT | - | [arXiv](https://arxiv.org/abs/2405.15223) | - | [Code](https://github.com/thuml/iVideoGPT) | Tsinghua | Interactive VideoGPT; autoregressive world model supporting action-conditioned video prediction for robot learning. |

### Training Datasets
| Title | Scale | Paper page | Project page | Data | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Something-Something V2 | 220K | [arXiv](https://arxiv.org/abs/1706.04261) | [Project](https://developer.qualcomm.com/software/ai-datasets/something-something) | [Data](https://developer.qualcomm.com/software/ai-datasets/something-something) | TwentyBN | 220K crowd-sourced videos of humans performing physical actions; tests temporal and causal reasoning. |
| Ego4D | 3,670h | [CVPR2022](https://arxiv.org/abs/2110.07058) | [Project](https://ego4d-data.org/) | [Data](https://ego4d-data.org/) | Meta & 13 universities | 3,670 hours of egocentric video from 74 worldwide locations; covers daily life activities for embodied AI. |
| EpicKitchens-100 | 100h | [IJCV2021](https://arxiv.org/abs/2006.13256) | [Project](https://epic-kitchens.github.io/) | [Data](https://epic-kitchens.github.io/) | Bristol | 100 hours of egocentric kitchen activity videos; benchmark for action recognition and anticipation. |
| BDD100K | 100K | [CVPR2020](https://arxiv.org/abs/1805.04687) | [Project](https://bdd-data.berkeley.edu/) | [Data](https://bdd-data.berkeley.edu/) | Berkeley | 100K diverse driving videos with rich annotations; widely used for autonomous driving world models. |
| nuScenes | 1000 scenes | [CVPR2020](https://arxiv.org/abs/1929.02545) | [Project](https://www.nuscenes.org/) | [Data](https://www.nuscenes.org/) | Motional | 1000 driving scenes with full sensor suite (camera, LiDAR, radar); standard AV benchmark. |
| Waymo Open Dataset | 1000 segments | [CVPR2020](https://arxiv.org/abs/1912.04838) | [Project](https://waymo.com/open/) | [Data](https://waymo.com/open/) | Waymo | High-quality LiDAR and camera data from real-world driving; standard for AV perception and prediction. |
| Open X-Embodiment | 1M+ | [ICRA2024](https://arxiv.org/abs/2310.08864) | [Project](https://robotics-transformer-x.github.io/) | [Code](https://github.com/google-deepmind/open_x_embodiment) | Google & 33 labs | 1M+ robot trajectories from 22 embodiments; enables cross-embodiment world model training. |
| RH20T | 110K | [arXiv](https://arxiv.org/abs/2307.00595) | [Project](https://rh20t.github.io/) | [Data](https://rh20t.github.io/) | Shanghai AI Lab | 110K contact-rich robot manipulation sequences with force/torque data; for dexterous world models. |
| Kinetics-700 | 650K | [arXiv](https://arxiv.org/abs/1907.06987) | - | [Data](https://www.deepmind.com/open-source/kinetics) | DeepMind | 650K video clips across 700 human action classes; standard pre-training dataset for video world models. |

### Benchmarks and Evaluation
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Atari 100K | - | [ICLR2021](https://arxiv.org/abs/2004.14990) | - | [Code](https://github.com/google/dopamine) | Google | Standard benchmark for sample-efficient RL; 100K environment steps per game across 26 Atari games. |
| DMControl | - | [arXiv](https://arxiv.org/abs/1801.00690) | [Project](https://github.com/google-deepmind/dm_control) | [Code](https://github.com/google-deepmind/dm_control) | DeepMind | DeepMind Control Suite; continuous control tasks for evaluating model-based RL world models. |
| Crafter | - | [TMLR2022](https://arxiv.org/abs/2109.06780) | [Project](https://danijar.com/project/crafter/) | [Code](https://github.com/danijar/crafter) | Google Brain | Open-world survival game benchmark; evaluates generalization, exploration, and long-horizon planning. |
| NetHack | - | [NeurIPS2020](https://arxiv.org/abs/2006.13760) | [Project](https://nethackchallenge.com/) | [Code](https://github.com/facebookresearch/nle) | Meta | Procedurally generated roguelike game; tests long-horizon planning and generalization in world models. |
| PHYRE | - | [NeurIPS2019](https://arxiv.org/abs/1908.05656) | [Project](https://phyre.ai/) | [Code](https://github.com/facebookresearch/phyre) | Meta | Physical reasoning benchmark; tests whether agents can predict outcomes of physical interactions. |
| IntPhys | - | [CVPR2019](https://arxiv.org/abs/1803.07616) | [Project](https://intphys.com/) | - | Meta | Intuitive physics benchmark; evaluates whether models understand basic physical laws. |
| nuPlan | - | [arXiv](https://arxiv.org/abs/2106.11810) | [Project](https://www.nuscenes.org/nuplan) | [Code](https://github.com/motional/nuplan-devkit) | Motional | Closed-loop planning benchmark for autonomous driving; 1300+ hours of expert driving data. |
| CARLA | - | [CoRL2017](https://arxiv.org/abs/1711.03938) | [Project](https://carla.org/) | [Code](https://github.com/carla-simulator/carla) | Intel | Open-source autonomous driving simulator; standard for evaluating AV world models in closed-loop. |
| Minecraft (MineRL) | - | [NeurIPS2019](https://arxiv.org/abs/1907.13440) | [Project](https://minerl.io/) | [Code](https://github.com/minerllabs/minerl) | CMU | Minecraft-based RL benchmark; tests long-horizon planning and world model generalization. |
| EvalCrafter | - | [CVPR2024](https://arxiv.org/abs/2310.11440) | [Project](https://evalcrafter.github.io/) | [Code](https://github.com/EvalCrafter/EvalCrafter) | - | Benchmarks video generation models on visual quality, motion quality, text-video alignment, and action quality. |
| VBench | - | [CVPR2024](https://arxiv.org/abs/2311.17982) | [Project](https://vchitect.github.io/VBench-project/) | [Code](https://github.com/Vchitect/VBench) | NTU | Comprehensive benchmark for video generation; 16 dimensions covering quality, semantics, and temporal consistency. |

### Projects and Toolkits
| Title | Presentation | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|
| Dreamer (Official) | - | [Project](https://danijar.com/project/dreamerv3/) | [Code](https://github.com/danijar/dreamerv3) | Google DeepMind | Official DreamerV3 implementation; single codebase for model-based RL across diverse domains. |
| JEPA (Official) | - | [Blog](https://ai.meta.com/blog/v-jepa-yann-lecun-ai-model-video-joint-embedding-predictive-architecture/) | [Code](https://github.com/facebookresearch/jepa) | Meta | Official V-JEPA implementation; self-supervised video world model training. |
| Awesome-World-Model | - | - | [Code](https://github.com/LMD0311/Awesome-World-Model) | Community | Curated list of world model papers for autonomous driving; actively maintained. |
| Genesis | - | - | [Code](https://github.com/Genesis-Embodied-AI/Genesis) | Community | A generative world for general-purpose robotics and embodied AI learning; physics-based simulation. |
| Open-Sora | - | - | [Code](https://github.com/hpcaitech/Open-Sora) | HPC-AI Tech | Open-source video world model training framework; scalable DiT-based video generation. |

## Acknowledgement
Some of the presentations in this repository are borrowed from the original authors, and we are very thankful for their contributions.

## License
This project is released under the MIT license.

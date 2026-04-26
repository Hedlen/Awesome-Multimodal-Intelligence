<div align="center">
<br>
<img src="https://allenai.org/static/images/embodied-ai-hero.jpg" width="700px">
<br>
</div>

# Awesome Embodied AI [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

Embodied AI focuses on agents that perceive, reason, and act in physical or simulated environments — bridging the gap from perception to decision-making. This repository tracks research across navigation, manipulation, task planning, sim-to-real transfer, humanoid robots, and general-purpose embodied agents.

If you find this repository helpful, please consider Stars ⭐ or Sharing ⬆️. Thanks.

## News
- 2026.4: Initial release — covering navigation (NavGPT, EmbodiedScan), manipulation (RoboAgent, AnyGrasp), task planning (SayCan, Code-as-Policies), humanoid robots (Figure, Unitree), general agents (GROOT, OpenVLA), simulators (Isaac Lab, ManiSkill3, Genesis), and comprehensive benchmarks.

## Contents

- [Perception and Scene Understanding](#perception-and-scene-understanding)
- [Navigation](#navigation)
- [Manipulation](#manipulation)
- [Task Planning and Reasoning](#task-planning-and-reasoning)
- [General Embodied Agents](#general-embodied-agents)
- [Humanoid and Dexterous Robots](#humanoid-and-dexterous-robots)
- [Sim-to-Real Transfer](#sim-to-real-transfer)
- [Training Datasets](#training-datasets)
- [Simulators and Environments](#simulators-and-environments)
- [Benchmarks and Evaluation](#benchmarks-and-evaluation)
- [Projects and Toolkits](#projects-and-toolkits)

## Papers / Projects

### Perception and Scene Understanding
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| EmbodiedScan | - | [CVPR2024](https://arxiv.org/abs/2312.16170) | [Project](https://tai-wang.github.io/embodiedscan/) | [Code](https://github.com/OpenRobotLab/EmbodiedScan) | Shanghai AI Lab | Holistic multi-modal 3D perception suite; covers detection, VQA, and grounding in 3D scenes. |
| 3D-LLM | - | [NeurIPS2023](https://arxiv.org/abs/2307.12981) | [Project](https://vis-www.cs.umass.edu/3dllm/) | [Code](https://github.com/UMass-Foundation-Model/3D-LLM) | UMass | Injects 3D world representations into LLMs; enables 3D QA, captioning, and task planning. |
| SQA3D | - | [ICLR2023](https://arxiv.org/abs/2210.07474) | [Project](https://sqa3d.github.io/) | [Code](https://github.com/SilongYong/SQA3D) | HKUST | Situated Question Answering in 3D scenes; evaluates spatial reasoning grounded in 3D environments. |
| ConceptFusion | - | [RSS2023](https://arxiv.org/abs/2302.07241) | [Project](https://concept-fusion.github.io/) | [Code](https://github.com/concept-fusion/concept-fusion) | MIT | Open-set multimodal 3D mapping; fuses CLIP features into 3D maps for zero-shot object retrieval. |
| OpenScene | - | [CVPR2023](https://arxiv.org/abs/2211.15654) | [Project](https://pengsongyou.github.io/openscene) | [Code](https://github.com/pengsongyou/openscene) | ETH | Open-vocabulary 3D scene understanding; distills 2D CLIP features into 3D point clouds. |
| LERF | - | [ICCV2023](https://arxiv.org/abs/2303.09553) | [Project](https://www.lerf.io/) | [Code](https://github.com/kerrj/lerf) | Berkeley | Language Embedded Radiance Fields; queries natural language in 3D NeRF scenes for embodied navigation. |
| Grounded-SAM | - | [arXiv](https://arxiv.org/abs/2401.14159) | - | [Code](https://github.com/IDEA-Research/Grounded-Segment-Anything) | IDEA Research | Combines Grounding DINO and SAM for open-set object detection and segmentation; widely used in robotics. |
| AnyGrasp | - | [T-RO2023](https://arxiv.org/abs/2212.08333) | [Project](https://graspnet.net/anygrasp.html) | [Code](https://github.com/graspnet/anygrasp_sdk) | Shanghai AI Lab | Robust and efficient grasp perception in spatial and temporal domains; handles diverse objects and scenes. |

### Navigation
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| NavGPT | - | [arXiv](https://arxiv.org/abs/2305.16986) | - | [Code](https://github.com/GengzeZhou/NavGPT) | - | Explicit reasoning for vision-and-language navigation using GPT-4 as a zero-shot navigator. |
| NavGPT-2 | - | [ECCV2024](https://arxiv.org/abs/2407.12366) | - | [Code](https://github.com/GengzeZhou/NavGPT-2) | - | Unleashing navigational reasoning capability of large VLMs; fine-tuned VLM for VLN with chain-of-thought. |
| VLN-BERT | - | [CVPR2021](https://arxiv.org/abs/2011.13922) | - | [Code](https://github.com/YicongHong/Recurrent-VLN-BERT) | ANU | Recurrent BERT for vision-and-language navigation; models history-conditioned action prediction. |
| DUET | - | [CVPR2022](https://arxiv.org/abs/2204.01393) | - | [Code](https://github.com/cshizhe/VLN-DUET) | INRIA | Dual-scale graph transformer for VLN; combines local and global action spaces for long-horizon navigation. |
| ETPNav | - | [TPAMI2024](https://arxiv.org/abs/2304.03047) | - | [Code](https://github.com/MarSaKi/ETPNav) | - | Evolving topological planning for VLN; builds topological maps online for efficient long-horizon navigation. |
| SemExp | - | [NeurIPS2020](https://arxiv.org/abs/2007.09549) | [Project](https://devendrachaplot.github.io/projects/semantic-exploration) | [Code](https://github.com/devendrachaplot/Object-Goal-Navigation) | CMU | Semantic exploration for object goal navigation; modular approach with semantic map and policy. |
| ZSON | - | [NeurIPS2022](https://arxiv.org/abs/2206.12403) | - | [Code](https://github.com/zinengtang/ZSON) | - | Zero-shot object-goal navigation using CLIP; generalizes to unseen object categories without fine-tuning. |
| CoW | - | [ICRA2023](https://arxiv.org/abs/2211.10220) | [Project](https://cow.cs.columbia.edu/) | [Code](https://github.com/real-stanford/cow) | Columbia | CLIP on Wheels; zero-shot object navigation using CLIP features with frontier-based exploration. |
| ViNT | - | [CoRL2023](https://arxiv.org/abs/2306.14846) | [Project](https://general-navigation-models.github.io/vint/) | [Code](https://github.com/robodhruv/visualnav-transformer) | Berkeley | Visual Navigation Transformer; a foundation model for outdoor robot navigation trained on diverse data. |
| NoMaD | - | [ICRA2024](https://arxiv.org/abs/2310.07896) | [Project](https://general-navigation-models.github.io/nomad/) | [Code](https://github.com/robodhruv/visualnav-transformer) | Berkeley | Goal-masked diffusion policies for navigation and exploration; handles both goal-directed and exploratory navigation. |

### Manipulation
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| RoboAgent | - | [ICRA2024](https://arxiv.org/abs/2309.01918) | [Project](https://robopen.github.io/) | [Code](https://github.com/robopen/roboagent) | CMU | Towards sample-efficient robot manipulation with semantic augmentations and multi-task learning. |
| RoboFlamingo | - | [ICLR2024](https://arxiv.org/abs/2311.01378) | [Project](https://roboflamingo.github.io/) | [Code](https://github.com/RoboFlamingo/RoboFlamingo) | ByteDance | Fine-tunes OpenFlamingo as a robot imitator with an explicit policy head; strong on CALVIN benchmark. |
| GNFactor | - | [CoRL2023](https://arxiv.org/abs/2308.16891) | [Project](https://yanjieze.com/GNFactor/) | [Code](https://github.com/YanjieZe/GNFactor) | Shanghai AI Lab | Multi-task real robot learning with generalizable neural feature fields; 3D-aware manipulation. |
| PerAct | - | [CoRL2022](https://arxiv.org/abs/2209.05451) | [Project](https://peract.github.io/) | [Code](https://github.com/peract/peract) | UW | Perceiver-Actor; a multi-task transformer for robot manipulation using 3D voxel observations. |
| RVT | - | [CoRL2023](https://arxiv.org/abs/2306.14896) | [Project](https://robotic-view-transformer.github.io/) | [Code](https://github.com/nvlabs/rvt) | NVIDIA | Robotic View Transformer; multi-view virtual rendering for 3D robot manipulation without 3D supervision. |
| RVT-2 | - | [RSS2024](https://arxiv.org/abs/2406.08545) | [Project](https://robotic-view-transformer-2.github.io/) | [Code](https://github.com/nvlabs/rvt) | NVIDIA | Improved RVT with better multi-view rendering and training; SoTA on RLBench multi-task benchmark. |
| SPA | - | [arXiv](https://arxiv.org/abs/2410.08208) | - | - | - | 3D spatial awareness for robot manipulation; leverages 3D scene understanding for precise manipulation. |
| Diffusion Policy | - | [RSS2023](https://arxiv.org/abs/2303.04137) | [Project](https://diffusion-policy.cs.columbia.edu/) | [Code](https://github.com/real-stanford/diffusion_policy) | Columbia | Visuomotor policy learning via conditional denoising diffusion; handles multimodal action distributions. |
| 3D Diffusion Policy | - | [RSS2024](https://arxiv.org/abs/2403.03954) | [Project](https://3d-diffusion-policy.github.io/) | [Code](https://github.com/YanjieZe/3D-Diffusion-Policy) | Shanghai AI Lab | Extends diffusion policy to 3D point cloud observations; better spatial understanding for manipulation. |
| ACT | - | [RSS2023](https://arxiv.org/abs/2304.13705) | [Project](https://tonyzhaozh.github.io/aloha/) | [Code](https://github.com/tonyzhaozh/act) | Stanford | Action Chunking with Transformers; predicts action sequences to reduce compounding errors in imitation. |
| GROOT | - | [arXiv](https://arxiv.org/abs/2403.13358) | [Project](https://ut-austin-rpl.github.io/GROOT/) | [Code](https://github.com/UT-Austin-RPL/GROOT) | UT Austin | Learning generalizable manipulation policies with object-centric 3D representations. |
| RoboPoint | - | [arXiv](https://arxiv.org/abs/2406.10721) | [Project](https://robo-point.github.io/) | - | UW | A VLM for predicting spatial affordances for robot manipulation; generates point predictions for grasping. |

### Task Planning and Reasoning
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| SayCan | - | [CoRL2022](https://arxiv.org/abs/2204.01691) | [Project](https://say-can.github.io/) | [Code](https://github.com/google-research/google-research/tree/master/saycan) | Google | Grounds LLM planning in robot affordances; value functions score which skills are both useful and feasible. |
| Code-as-Policies | - | [ICRA2023](https://arxiv.org/abs/2209.07753) | [Project](https://code-as-policies.github.io/) | [Code](https://github.com/google-research/google-research/tree/master/code_as_policies) | Google | LLMs write robot policy code; hierarchical code generation for complex manipulation tasks. |
| ProgPrompt | - | [ICRA2023](https://arxiv.org/abs/2209.11302) | [Project](https://progprompt.github.io/) | [Code](https://github.com/NVlabs/progprompt-vh) | NVIDIA | Programmatic LLM prompts for robot task planning; structured programs with assertions for error recovery. |
| Inner Monologue | - | [CoRL2022](https://arxiv.org/abs/2207.05608) | [Project](https://innermonologue.github.io/) | - | Google | Embodied reasoning through language model feedback; closed-loop planning with environment feedback. |
| DEPS | - | [arXiv](https://arxiv.org/abs/2302.01560) | - | [Code](https://github.com/CraftJarvis/DEPS) | PKU | Describe, Explain, Plan and Select; interactive planning with LLMs for open-world tasks in Minecraft. |
| Voyager | - | [arXiv](https://arxiv.org/abs/2305.16291) | [Project](https://voyager.minedojo.org/) | [Code](https://github.com/MineDojo/Voyager) | NVIDIA | LLM-powered embodied lifelong learning agent in Minecraft; automatic curriculum and skill library. |
| JARVIS-1 | - | [arXiv](https://arxiv.org/abs/2311.05997) | [Project](https://craftjarvis-jarvis1.github.io/) | [Code](https://github.com/CraftJarvis/JARVIS-1) | PKU | Open-world multi-task agents with memory-augmented multimodal language models; Minecraft agent. |
| EmbodiedGPT | - | [NeurIPS2023](https://arxiv.org/abs/2305.15021) | [Project](https://embodiedgpt.github.io/) | [Code](https://github.com/EmbodiedGPT/EmbodiedGPT_Pytorch) | Shanghai AI Lab | Chain-of-thought embodied planning; generates sub-goals and queries a policy network for execution. |
| ReKep | - | [arXiv](https://arxiv.org/abs/2409.01652) | [Project](https://rekep-robot.github.io/) | [Code](https://github.com/huangwl18/ReKep) | Stanford | Spatio-temporal keypoint constraints from VLMs for robot manipulation; generalizes to novel tasks. |
| RoboVQA | - | [arXiv](https://arxiv.org/abs/2311.00899) | - | - | Google | Multimodal long-horizon robot reasoning via VQA; decomposes tasks into visual questions for planning. |

### General Embodied Agents
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Gato | - | [arXiv](https://arxiv.org/abs/2205.06175) | [Blog](https://deepmind.google/discover/blog/a-generalist-agent/) | - | DeepMind | A generalist agent; single transformer trained on 600+ tasks including games, robotics, and language. |
| RT-2 | - | [CoRL2023](https://arxiv.org/abs/2307.15818) | [Project](https://robotics-transformer2.github.io/) | - | Google DeepMind | VLA co-fine-tuned on robot data; emergent semantic reasoning and chain-of-thought planning. |
| OpenVLA | - | [CoRL2024](https://arxiv.org/abs/2406.09246) | [Project](https://openvla.github.io/) | [Code](https://github.com/openvla/openvla) | Stanford & Berkeley | Open-source 7B VLA; outperforms RT-2-X (55B) by 16.5% with 7× fewer parameters. |
| π0 (pi-zero) | - | [arXiv](https://arxiv.org/abs/2410.24164) | [Blog](https://www.physicalintelligence.company/blog/pi0) | [Code](https://github.com/Physical-Intelligence/openpi) | Physical Intelligence | VLA flow model for general robot control; flow matching for continuous action generation. |
| Octo | - | [RSS2024](https://arxiv.org/abs/2405.12213) | [Project](https://octo-models.github.io/) | [Code](https://github.com/octo-models/octo) | UC Berkeley | Open-source generalist robot policy (93M) trained on 800k trajectories; easy to fine-tune. |
| LEO | - | [ICML2024](https://arxiv.org/abs/2311.12871) | [Project](https://embodied-generalist.github.io/) | [Code](https://github.com/embodied-generalist/embodied-generalist) | NTU | Embodied generalist agent for 3D world understanding and interaction; unifies perception, grounding, and action. |
| ManipLLM | - | [CVPR2024](https://arxiv.org/abs/2312.16217) | [Project](https://sites.google.com/view/manipllm) | [Code](https://github.com/clorislili/ManipLLM) | - | Embodied multimodal large language model for object-centric robotic manipulation. |
| RoboMamba | - | [arXiv](https://arxiv.org/abs/2406.04339) | - | [Code](https://github.com/lmzpai/roboMamba) | - | Efficient embodied language model with Mamba architecture; fast inference for real-time robot control. |
| UniSim (General) | - | [ICLR2024](https://arxiv.org/abs/2310.06114) | [Project](https://universal-simulator.github.io/) | - | Stanford | Learning interactive real-world simulators; generates diverse embodied experiences for agent training. |
| GROOT | - | [arXiv](https://arxiv.org/abs/2403.13358) | [Project](https://ut-austin-rpl.github.io/GROOT/) | [Code](https://github.com/UT-Austin-RPL/GROOT) | UT Austin | Generalizable manipulation with object-centric 3D representations; zero-shot transfer to novel objects. |

### Humanoid and Dexterous Robots
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Figure 02 | - | [Blog](https://www.figure.ai/news/figure-02) | [Project](https://www.figure.ai/) | - | Figure AI | Commercial humanoid robot with OpenAI-powered VLA; demonstrates household task execution. |
| Unitree H1/G1 | - | [Blog](https://www.unitree.com/h1/) | [Project](https://www.unitree.com/) | - | Unitree | Affordable humanoid robots widely used in embodied AI research; open SDK for policy deployment. |
| HumanPlus | - | [arXiv](https://arxiv.org/abs/2406.10454) | [Project](https://humanoid-ai.github.io/) | [Code](https://github.com/MarkFzp/humanplus) | Stanford | Humanoid shadowing and imitation from human data; whole-body teleoperation and policy learning. |
| OmniH2O | - | [arXiv](https://arxiv.org/abs/2406.08858) | [Project](https://omni.human2humanoid.com/) | - | CMU | Universal and dexterous human-to-humanoid whole-body teleoperation and learning. |
| DexMimicGen | - | [arXiv](https://arxiv.org/abs/2410.24185) | [Project](https://dexmimicgen.github.io/) | - | NVIDIA | Automated data generation for dexterous manipulation from a small number of human demonstrations. |
| AnyTeleop | - | [RSS2023](https://arxiv.org/abs/2307.04577) | [Project](https://anyteleop.com/) | [Code](https://github.com/dexsuite/dex-retargeting) | UCSD | A general vision-based dexterous robot arm-hand teleoperation system. |
| DEXART | - | [CVPR2023](https://arxiv.org/abs/2305.05706) | [Project](https://www.chenbao.tech/dexart/) | [Code](https://github.com/Kami-code/dexart-release) | PKU | Benchmarking generalizable dexterous manipulation with articulated objects. |
| DexVLA | - | [arXiv](https://arxiv.org/abs/2502.05855) | - | - | - | VLA with plug-in diffusion transformer for dexterous manipulation; decouples reasoning from low-level control. |

### Sim-to-Real Transfer
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| DR (Domain Randomization) | - | [IROS2017](https://arxiv.org/abs/1703.06907) | - | - | OpenAI | Randomizes simulation parameters to bridge the sim-to-real gap; foundational technique for robot learning. |
| Dactyl | - | [Science Robotics2019](https://arxiv.org/abs/1808.00177) | [Blog](https://openai.com/research/learning-dexterity) | - | OpenAI | Dexterous in-hand manipulation learned in simulation; transfers to real robot hand via domain randomization. |
| RMA | - | [RSS2021](https://arxiv.org/abs/2107.04034) | [Project](https://ashish-kmr.github.io/rma-legged-robots/) | [Code](https://github.com/antonilo/rl_locomotion) | Berkeley | Rapid Motor Adaptation for legged robots; online adaptation to unseen terrains via privileged learning. |
| Walk These Ways | - | [CoRL2022](https://arxiv.org/abs/2212.03238) | [Project](https://gmargo11.github.io/walk-these-ways/) | [Code](https://github.com/Improbable-AI/walk-these-ways) | MIT | Gait conditioning for agile locomotion; single policy handles diverse gaits and terrains. |
| DreamWaQ | - | [ICRA2023](https://arxiv.org/abs/2301.10602) | - | - | - | Learning robust quadrupedal locomotion with implicit terrain imagination via deep reinforcement learning. |
| MimicGen | - | [CoRL2023](https://arxiv.org/abs/2310.17596) | [Project](https://mimicgen.github.io/) | [Code](https://github.com/NVlabs/mimicgen) | NVIDIA | Automated data generation for robot learning from a small number of human demonstrations. |

### Training Datasets
| Title | Scale | Paper page | Project page | Data | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Open X-Embodiment | 1M+ | [ICRA2024](https://arxiv.org/abs/2310.08864) | [Project](https://robotics-transformer-x.github.io/) | [Code](https://github.com/google-deepmind/open_x_embodiment) | Google & 33 labs | 1M+ robot trajectories from 22 embodiments; the largest cross-embodiment robot learning dataset. |
| LIBERO | 130 tasks | [NeurIPS2023](https://arxiv.org/abs/2306.03310) | [Project](https://libero-project.github.io/) | [Code](https://github.com/Lifelong-Robot-Learning/LIBERO) | UNC | Benchmark for lifelong robot learning with 130 language-conditioned manipulation tasks. |
| BridgeData V2 | 60K+ | [arXiv](https://arxiv.org/abs/2308.12952) | [Project](https://rail-berkeley.github.io/bridgedata/) | [Code](https://github.com/rail-berkeley/bridge_data_v2) | UC Berkeley | 60K+ robot trajectories across 24 environments; widely used for generalist robot policy training. |
| ALOHA / ALOHA 2 | - | [RSS2023](https://arxiv.org/abs/2304.13705) | [Project](https://tonyzhaozh.github.io/aloha/) | [Code](https://github.com/tonyzhaozh/aloha) | Stanford | Low-cost bimanual teleoperation hardware + dataset; platform behind ACT and Mobile ALOHA. |
| RH20T | 110K | [arXiv](https://arxiv.org/abs/2307.00595) | [Project](https://rh20t.github.io/) | [Data](https://rh20t.github.io/) | Shanghai AI Lab | 110K contact-rich robot manipulation sequences with force/torque data; for dexterous manipulation. |
| Ego4D | 3,670h | [CVPR2022](https://arxiv.org/abs/2110.07058) | [Project](https://ego4d-data.org/) | [Data](https://ego4d-data.org/) | Meta & 13 universities | 3,670 hours of egocentric video; covers daily life activities for embodied AI research. |
| EpicKitchens-100 | 100h | [IJCV2021](https://arxiv.org/abs/2006.13256) | [Project](https://epic-kitchens.github.io/) | [Data](https://epic-kitchens.github.io/) | Bristol | 100 hours of egocentric kitchen activity; benchmark for action recognition and anticipation. |
| Something-Something V2 | 220K | [arXiv](https://arxiv.org/abs/1706.04261) | - | [Data](https://developer.qualcomm.com/software/ai-datasets/something-something) | TwentyBN | 220K videos of humans performing physical actions; tests temporal and causal reasoning. |
| HM3D | 1000 scenes | [arXiv](https://arxiv.org/abs/2109.08238) | [Project](https://aihabitat.org/datasets/hm3d/) | [Data](https://aihabitat.org/datasets/hm3d/) | Meta | Habitat-Matterport 3D Dataset; 1000 high-quality 3D indoor scenes for embodied navigation. |
| Gibson | 572 spaces | [CVPR2018](https://arxiv.org/abs/1801.04592) | [Project](http://gibsonenv.stanford.edu/) | [Data](http://gibsonenv.stanford.edu/database/) | Stanford | Real-world 3D scans of indoor spaces; photorealistic navigation environments for embodied agents. |
| ScanNet | 1513 scans | [CVPR2017](https://arxiv.org/abs/1702.04405) | [Project](http://www.scan-net.org/) | [Data](http://www.scan-net.org/) | TU Munich | 3D indoor scene dataset with semantic annotations; widely used for 3D perception in embodied AI. |
| BEHAVIOR-1K | 1000 tasks | [CoRL2022](https://arxiv.org/abs/2403.09227) | [Project](https://behavior.stanford.edu/) | [Code](https://github.com/StanfordVL/BEHAVIOR-1K) | Stanford | 1000 everyday household activities in simulation; tests long-horizon task planning and execution. |
| MineRL | - | [NeurIPS2019](https://arxiv.org/abs/1907.13440) | [Project](https://minerl.io/) | [Code](https://github.com/minerllabs/minerl) | CMU | Minecraft human demonstration dataset; tests long-horizon planning and skill acquisition. |
| R2R | 21K | [CVPR2018](https://arxiv.org/abs/1711.07280) | [Project](https://bringmeaspoon.org/) | [Code](https://github.com/peteanderson80/Matterport3DSimulator) | ANU | Room-to-Room VLN dataset; 21K instructions for navigation in Matterport3D environments. |

### Simulators and Environments
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Isaac Lab | - | [arXiv](https://arxiv.org/abs/2301.04195) | [Project](https://isaac-sim.github.io/IsaacLab/) | [Code](https://github.com/isaac-sim/IsaacLab) | NVIDIA | GPU-accelerated robot learning framework built on Isaac Sim; supports RL, IL, and sim-to-real. |
| ManiSkill3 | - | [arXiv](https://arxiv.org/abs/2410.00425) | [Project](https://maniskill.ai/) | [Code](https://github.com/haosulab/ManiSkill) | Hillbot | GPU-parallelized robotics simulator; 10-1000x faster than other platforms with 30K+ FPS. |
| ManiSkill2 | - | [ICLR2023](https://arxiv.org/abs/2302.04659) | - | [Code](https://github.com/haosulab/ManiSkill2) | UCSD | 20 manipulation task families with 2000+ object models and 4M+ demonstration frames. |
| Habitat 3.0 | - | [ICLR2024](https://arxiv.org/abs/2310.13724) | [Project](https://aihabitat.org/) | [Code](https://github.com/facebookresearch/habitat-sim) | Meta | A co-habitat for humans and robots; supports social navigation and human-robot interaction tasks. |
| AI2-THOR | - | [arXiv](https://arxiv.org/abs/1712.05474) | [Project](https://ai2thor.allenai.org/) | [Code](https://github.com/allenai/ai2thor) | AI2 | Interactive 3D indoor environments; supports object interaction, navigation, and task completion. |
| RoboSuite | - | [arXiv](https://arxiv.org/abs/2009.12293) | [Project](https://robosuite.ai/) | [Code](https://github.com/ARISE-Initiative/robosuite) | Stanford | Modular robot learning framework with diverse manipulation tasks; built on MuJoCo. |
| SAPIEN | - | [CVPR2020](https://arxiv.org/abs/2003.08515) | [Project](https://sapien.ucsd.edu/) | [Code](https://github.com/haosulab/SAPIEN) | UCSD | A simulated part-based interactive environment; supports articulated object manipulation. |
| Genesis | - | [arXiv](https://arxiv.org/abs/2501.00001) | - | [Code](https://github.com/Genesis-Embodied-AI/Genesis) | Community | A generative world for general-purpose robotics; physics-based simulation with generative capabilities. |
| PyBullet / MuJoCo | - | - | [MuJoCo](https://mujoco.org/) | [Code](https://github.com/google-deepmind/mujoco) | DeepMind | Physics simulators widely used for robot learning; MuJoCo now open-source from DeepMind. |
| CARLA | - | [CoRL2017](https://arxiv.org/abs/1711.03938) | [Project](https://carla.org/) | [Code](https://github.com/carla-simulator/carla) | Intel | Open-source autonomous driving simulator; standard for AV and embodied driving agents. |
| VirtualHome | - | [CVPR2018](https://arxiv.org/abs/1806.07011) | [Project](http://virtual-home.org/) | [Code](https://github.com/xavierpuigf/virtualhome) | MIT | Household activity simulation; 1000+ activities with 200+ object interactions for task planning. |

### Benchmarks and Evaluation
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| CALVIN | - | [RA-L2022](https://arxiv.org/abs/2112.03227) | [Project](http://calvin.cs.uni-freiburg.de/) | [Code](https://github.com/mees/calvin) | Freiburg | Language-conditioned long-horizon manipulation; 34 tasks in 4 environments with 1000 instruction chains. |
| RLBench | - | [RA-L2020](https://arxiv.org/abs/1909.12271) | [Project](https://sites.google.com/view/rlbench) | [Code](https://github.com/stepjam/RLBench) | Imperial College | 100 unique robot manipulation tasks for imitation and reinforcement learning. |
| MetaWorld | - | [CoRL2019](https://arxiv.org/abs/1910.10897) | [Project](https://meta-world.github.io/) | [Code](https://github.com/Farama-Foundation/Metaworld) | Berkeley | 50 diverse robot manipulation tasks; standard benchmark for multi-task and meta-RL. |
| FurnitureBench | - | [RSS2023](https://arxiv.org/abs/2305.12821) | [Project](https://clvrai.github.io/furniture-bench/) | [Code](https://github.com/clvrai/furniture-bench) | CLVR | Reproducible real-world furniture assembly benchmark; tests long-horizon dexterous manipulation. |
| EmbodiedBench | - | [arXiv](https://arxiv.org/abs/2502.09560) | - | - | - | Extensive benchmark for vision-driven embodied agents; 1128 tasks across 4 environments. |
| EmbodiedEval | - | [arXiv](https://arxiv.org/abs/2501.11858) | - | - | - | Evaluates MLLMs as embodied agents; 328 tasks in 125 3D scenes covering diverse embodied AI tasks. |
| ScanQA | - | [CVPR2022](https://arxiv.org/abs/2112.10482) | [Project](https://scene.vision.ist.i.kyoto-u.ac.jp/scanqa/) | [Code](https://github.com/ATR-DBI/ScanQA) | Kyoto | 3D spatial question answering in ScanNet scenes; tests grounded 3D scene understanding. |
| MP3D-EQA | - | [CVPR2018](https://arxiv.org/abs/1711.11543) | [Project](https://embodiedqa.org/) | [Code](https://github.com/facebookresearch/EmbodiedQA) | Georgia Tech | Embodied Question Answering; agent navigates to answer questions about indoor environments. |
| ObjectNav | - | [arXiv](https://arxiv.org/abs/2006.13171) | [Project](https://aihabitat.org/) | [Code](https://github.com/facebookresearch/habitat-lab) | Meta | Object Goal Navigation benchmark; navigate to find target object categories in unseen environments. |
| VLN-CE | - | [EMNLP2020](https://arxiv.org/abs/2004.02857) | [Project](https://jacobkrantz.github.io/vlnce/) | [Code](https://github.com/jacobkrantz/VLN-CE) | Oregon State | VLN in Continuous Environments; navigation following natural language instructions without teleportation. |
| BEHAVIOR-1K | - | [CoRL2022](https://arxiv.org/abs/2403.09227) | [Project](https://behavior.stanford.edu/) | [Code](https://github.com/StanfordVL/BEHAVIOR-1K) | Stanford | 1000 everyday household activities; tests long-horizon planning, dexterity, and generalization. |
| HomeRobot | - | [arXiv](https://arxiv.org/abs/2306.11565) | [Project](https://ovmm.github.io/) | [Code](https://github.com/facebookresearch/home-robot) | Meta | Open-vocabulary mobile manipulation benchmark; pick-and-place with language-specified objects. |

### Projects and Toolkits
| Title | Presentation | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|
| LeRobot | - | [Blog](https://huggingface.co/blog/lerobot) | [Code](https://github.com/huggingface/lerobot) | HuggingFace | State-of-the-art robot learning library with pre-trained models, datasets, and simulation environments. |
| openpi (π0) | - | [Blog](https://www.physicalintelligence.company/blog/pi0) | [Code](https://github.com/Physical-Intelligence/openpi) | Physical Intelligence | Official open-source release of the π0 VLA model with training and inference code. |
| RoboSuite | - | [Project](https://robosuite.ai/) | [Code](https://github.com/ARISE-Initiative/robosuite) | Stanford | Modular robot learning framework; supports diverse manipulation tasks and policy training. |
| Lerobot Datasets | - | [Datasets](https://huggingface.co/lerobot) | [Code](https://github.com/huggingface/lerobot) | HuggingFace | Standardized robot learning datasets; compatible with LeRobot training pipeline. |
| HCPLab Embodied AI List | - | - | [Code](https://github.com/HCPLab-SYSU/Embodied_AI_Paper_List) | SYSU | Comprehensive paper list for embodied AI; covers perception, planning, manipulation, and navigation. |
| Awesome Embodied VLA | - | - | [Code](https://github.com/jonyzhang2023/awesome-embodied-vla-va-vln) | Community | Curated list of VLA, VLN, and embodied learning papers; actively maintained. |
| Awesome Robotics Foundation Models | - | - | [Code](https://github.com/robotics-survey/Awesome-Robotics-Foundation-Models) | Community | Survey companion for "Foundation Models in Robotics: Applications, Challenges, and the Future". |
| MineDojo | - | [Project](https://minedojo.org/) | [Code](https://github.com/MineDojo/MineDojo) | NVIDIA | Open-ended embodied agent framework in Minecraft; 3000+ diverse tasks with internet-scale knowledge. |

## Acknowledgement
Some of the presentations in this repository are borrowed from the original authors, and we are very thankful for their contributions.

## License
This project is released under the MIT license.

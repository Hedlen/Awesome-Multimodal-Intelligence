<div align="center">
<br>
<image src="https://github.com/haotian-liu/LLaVA/raw/main/images/llava_logo.png", width="120px">
<br>
</div>

# Awesome Vision Language Models (VLMs) [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

Vision Language Models (VLMs) have emerged as a transformative force at the intersection of computer vision and natural language processing, enabling machines to perceive, reason, and converse about the visual world. This repository continuously tracks and summarizes the research progress of VLMs across foundational models, benchmarks, applications, and toolkits.

If you find this repository helpful, please consider Stars ⭐ or Sharing ⬆️. Thanks.

## News
- 2026.4: Added Qwen2-VL, InternVL 2.5, LLaVA-OneVision and more recent works.
- 2025.5: Added Idefics2, SmolVLM, and updated benchmark section with latest results.
- 2024.9: Added GPT-4o, Gemini 1.5 Pro, and Claude 3.5 Sonnet multimodal capabilities.
- 2024.4: Added InternVL (CVPR 2024 Oral), ShareGPT4V, and mPLUG-Owl2.
- 2023.12: Added CogVLM, Otter, and KOSMOS-2 grounding models.
- 2023.7: Added LLaVA-1.5, InstructBLIP, and Qwen-VL.
- 2023.4: Initial release tracking foundational VLM papers and projects.

## Contents

- [Foundational Papers](#foundational-papers)
  - [Contrastive Pre-training](#contrastive-pre-training)
  - [Generative VLMs](#generative-vlms)
  - [Instruction-Tuned VLMs](#instruction-tuned-vlms)
  - [Grounding and Localization](#grounding-and-localization)
  - [Efficient and Lightweight VLMs](#efficient-and-lightweight-vlms)
- [Benchmarks and Evaluation](#benchmarks-and-evaluation)
- [Applications](#applications)
  - [Medical VLMs](#medical-vlms)
  - [Document Understanding](#document-understanding)
  - [Video Understanding](#video-understanding)
  - [Embodied AI](#embodied-ai)
- [Projects and Toolkits](#projects-and-toolkits)

## Papers / Projects

### Foundational Papers

#### Contrastive Pre-training
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| CLIP | ![img](https://github.com/openai/CLIP/raw/main/CLIP.png) | [ICML2021](https://arxiv.org/abs/2103.00020) | [Blog](https://openai.com/research/clip) | [Code](https://github.com/openai/CLIP) | OpenAI | Contrastive Language-Image Pre-Training; learns visual concepts from natural language supervision at web scale. |
| ALIGN | - | [ICML2021](https://arxiv.org/abs/2102.05918) | - | - | Google | Scales up noisy image-text pairs for robust vision-language alignment without expensive curation. |
| Florence | - | [arXiv](https://arxiv.org/abs/2111.11432) | - | - | Microsoft | A universal vision foundation model covering representation, detection, segmentation, and captioning. |
| FLAVA | - | [CVPR2022](https://arxiv.org/abs/2112.04482) | [Project](https://flava-model.github.io/) | [Code](https://github.com/facebookresearch/multimodal/tree/main/examples/flava) | Meta | A foundational language and vision alignment model trained with contrastive, multimodal, and unimodal objectives. |

#### Generative VLMs
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Flamingo | ![img](https://github.com/mlfoundations/open_flamingo/raw/main/docs/flamingo.png) | [NeurIPS2022](https://arxiv.org/abs/2204.14198) | [Blog](https://www.deepmind.com/blog/tackling-multiple-tasks-with-a-single-visual-language-model) | [OpenFlamingo](https://github.com/mlfoundations/open_flamingo) | DeepMind | A family of VLMs for few-shot learning; interleaves images and text via cross-attention into a frozen LLM. |
| BLIP-2 | ![img](https://github.com/salesforce/LAVIS/raw/main/docs/_static/logo_final.png) | [ICML2023](https://arxiv.org/abs/2301.12597) | [Demo](https://huggingface.co/spaces/Salesforce/BLIP2) | [Code](https://github.com/salesforce/LAVIS/tree/main/projects/blip2) | Salesforce | Bootstraps vision-language pre-training from frozen image encoders and LLMs via a lightweight Q-Former. |
| PaLM-E | ![img](https://palm-e.github.io/assets/palm-e-teaser.gif) | [arXiv](https://arxiv.org/abs/2303.03378) | [Project](https://palm-e.github.io/) | - | Google | An embodied multimodal language model (562B) that ingests robot sensor data directly into a language model. |
| mPLUG-Owl | ![img](https://github.com/X-PLUG/mPLUG-Owl/raw/main/assets/mplug_owl_logo.png) | [arXiv](https://arxiv.org/abs/2304.14178) | [Demo](https://www.modelscope.cn/studios/damo/mPLUG-Owl) | [Code](https://github.com/X-PLUG/mPLUG-Owl) | Alibaba DAMO | Modularization empowers LLMs with multimodality via a two-stage visual knowledge alignment strategy. |
| MiniGPT-4 | ![img](https://minigpt-4.github.io/static/images/minigpt4.png) | [arXiv](https://arxiv.org/abs/2304.10592) | [Demo](https://huggingface.co/spaces/Vision-CAIR/minigpt4) | [Code](https://github.com/Vision-CAIR/MiniGPT-4) | KAUST | Aligns a frozen visual encoder with Vicuna using a single projection layer; demonstrates GPT-4-like multimodal capabilities. |
| VisionLLM | - | [NeurIPS2023](https://arxiv.org/abs/2305.11175) | - | [Code](https://github.com/OpenGVLab/VisionLLM) | OpenGVLab | Uses LLM as an open-ended decoder for vision-centric tasks including detection, segmentation, and captioning. |

#### Instruction-Tuned VLMs
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| LLaVA | ![img](https://llava-vl.github.io/static/images/llava_logo.png) | [NeurIPS2023 Oral](https://arxiv.org/abs/2304.08485) | [Project](https://llava-vl.github.io/) | [Code](https://github.com/haotian-liu/LLaVA) | UW-Madison | Visual instruction tuning with GPT-4-generated data; first open-source model approaching GPT-4V-level multimodal chat. |
| LLaVA-1.5 | ![img](https://llava-vl.github.io/static/images/llava_v1_5_radar.jpg) | [CVPR2024](https://arxiv.org/abs/2310.03744) | [Project](https://llava-vl.github.io/) | [Code](https://github.com/haotian-liu/LLaVA) | UW-Madison | Improved LLaVA with MLP connector and academic-task-oriented data; achieves SoTA on 11 benchmarks with 13B params. |
| InstructBLIP | - | [NeurIPS2023](https://arxiv.org/abs/2305.06500) | [Demo](https://huggingface.co/spaces/hysts/InstructBLIP) | [Code](https://github.com/salesforce/LAVIS/tree/main/projects/instructblip) | Salesforce | Instruction-tuned BLIP-2 with instruction-aware Q-Former; SoTA zero-shot on 13 held-out datasets. |
| Qwen-VL | ![img](https://github.com/QwenLM/Qwen-VL/raw/master/assets/logo.jpg) | [arXiv](https://arxiv.org/abs/2308.12966) | [Demo](https://huggingface.co/spaces/Qwen/Qwen-VL-Chat-Demo) | [Code](https://github.com/QwenLM/Qwen-VL) | Alibaba | A versatile LVLM supporting image captioning, VQA, visual localization, and flexible interaction; strong on Chinese benchmarks. |
| Qwen2-VL | ![img](https://github.com/QwenLM/Qwen2-VL/raw/main/assets/qwen2vl.png) | [arXiv](https://arxiv.org/abs/2409.12191) | [Demo](https://huggingface.co/spaces/Qwen/Qwen2-VL) | [Code](https://github.com/QwenLM/Qwen2-VL) | Alibaba | Introduces Naive Dynamic Resolution and Multimodal Rotary Position Embedding (M-RoPE) for any-resolution image understanding. |
| InternVL | ![img](https://internvl.github.io/internvl/images/internvl_logo.png) | [CVPR2024 Oral](https://arxiv.org/abs/2312.14238) | [Project](https://internvl.github.io/) | [Code](https://github.com/OpenGVLab/InternVL) | OpenGVLab | A pioneering open-source alternative to GPT-4o; InternVL 2.5-78B first open model to exceed 70% on MMMU. |
| CogVLM | ![img](https://github.com/THUDM/CogVLM/raw/main/assets/cogvlm-logo.png) | [arXiv](https://arxiv.org/abs/2311.03079) | [Demo](https://huggingface.co/spaces/THUDM/CogVLM) | [Code](https://github.com/THUDM/CogVLM) | Tsinghua | Deep visual-language feature alignment via a trainable visual expert module; strong on grounding and referring tasks. |
| ShareGPT4V | - | [arXiv](https://arxiv.org/abs/2311.12793) | [Project](https://sharegpt4v.github.io/) | [Code](https://github.com/InternLM/InternLM-XComposer/tree/main/projects/ShareGPT4V) | Shanghai AI Lab | Improves LMMs with 1.2M high-quality GPT-4V-generated captions; significant gains in pre-training and SFT phases. |
| LLaVA-OneVision | - | [arXiv](https://arxiv.org/abs/2408.03326) | [Demo](https://huggingface.co/spaces/lmms-lab/LLaVA-OneVision) | [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) | ByteDance & NTU | Unifies single-image, multi-image, and video understanding in one model; SoTA on diverse multimodal benchmarks. |
| Idefics2 | - | [arXiv](https://arxiv.org/abs/2405.02246) | [Demo](https://huggingface.co/spaces/HuggingFaceM4/idefics2_playground) | [Code](https://github.com/huggingface/transformers) | HuggingFace | An 8B efficient foundational VLM; consolidates best practices for architecture, data, and training of VLMs. |

#### Grounding and Localization
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| KOSMOS-2 | ![img](https://github.com/microsoft/unilm/raw/master/kosmos-2/assets/kosmos2-teaser.png) | [arXiv](https://arxiv.org/abs/2306.14824) | [Demo](https://huggingface.co/spaces/ydshieh/Kosmos-2) | [Code](https://github.com/microsoft/unilm/tree/master/kosmos-2) | Microsoft | Grounds language to the visual world via referring expression comprehension and generation with bounding boxes. |
| Grounding DINO | ![img](https://github.com/IDEA-Research/GroundingDINO/raw/main/.asset/hero_figure.png) | [arXiv](https://arxiv.org/abs/2303.05499) | [Demo](https://huggingface.co/spaces/ShilongLiu/Grounding_DINO_demo) | [Code](https://github.com/IDEA-Research/GroundingDINO) | IDEA Research | Open-set object detector combining DINO with grounded pre-training; detects arbitrary objects from text prompts. |
| OWL-ViT | ![img](https://github.com/google-research/scenic/raw/main/scenic/projects/owl_vit/data/text_cond_wiki_stillife_1.gif) | [ECCV2022](https://arxiv.org/abs/2205.06230) | - | [Code](https://github.com/google-research/scenic/tree/main/scenic/projects/owl_vit) | Google | Open-vocabulary object detection with image-level contrastive pre-training and transfer to detection. |
| Shikra | - | [arXiv](https://arxiv.org/abs/2306.15195) | - | [Code](https://github.com/shikras/shikra) | SenseTime | Unified VLM that handles referring expression comprehension and generation in natural language coordinates. |

#### Efficient and Lightweight VLMs
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| MobileVLM | - | [arXiv](https://arxiv.org/abs/2312.16886) | - | [Code](https://github.com/Meituan-AutoML/MobileVLM) | Meituan | A fast and strong multimodal language model for mobile devices with a lightweight downsampling projector. |
| MoE-LLaVA | - | [arXiv](https://arxiv.org/abs/2401.15947) | [Demo](https://huggingface.co/spaces/LanguageBind/MoE-LLaVA) | [Code](https://github.com/PKU-YuanGroup/MoE-LLaVA) | PKU | Mixture of Experts for LLaVA; activates sparse experts per token to scale capacity without proportional compute cost. |
| SmolVLM | - | [Blog](https://huggingface.co/blog/smolvlm) | [Demo](https://huggingface.co/spaces/HuggingFaceTB/SmolVLM) | [Code](https://github.com/huggingface/smollm) | HuggingFace | A compact 2B VLM designed for on-device deployment; strong performance-to-size ratio across multimodal benchmarks. |

### Benchmarks and Evaluation
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| MMBench | - | [arXiv](https://arxiv.org/abs/2307.06281) | [Leaderboard](https://mmbench.opencompass.org.cn/leaderboard) | [Code](https://github.com/open-compass/MMBench) | OpenCompass | A systematically designed objective benchmark for holistic evaluation of VLMs across 20 ability dimensions. |
| MMMU | - | [CVPR2024](https://arxiv.org/abs/2311.16502) | [Project](https://mmmu-benchmark.github.io/) | [Code](https://github.com/MMMU-Benchmark/MMMU) | UMich & others | Massive Multi-discipline Multimodal Understanding benchmark with 11.5K college-level questions across 30 subjects. |
| MME | - | [arXiv](https://arxiv.org/abs/2306.13394) | - | [Code](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models/tree/Evaluation) | Xiamen University | A comprehensive evaluation benchmark measuring both perception and cognition abilities of MLLMs. |
| SeedBench | - | [CVPR2024](https://arxiv.org/abs/2307.16125) | [Leaderboard](https://huggingface.co/spaces/AILab-CVC/SEED-Bench_Leaderboard) | [Code](https://github.com/AILab-CVC/SEED-Bench) | Tencent AI Lab | Evaluates generative comprehension of MLLMs with 19K multiple-choice questions across 12 evaluation dimensions. |
| LLaVA-Bench | - | [NeurIPS2023](https://arxiv.org/abs/2304.08485) | - | [Code](https://github.com/haotian-liu/LLaVA) | UW-Madison | In-the-wild benchmark for instruction-following VLMs covering conversation, detail description, and complex reasoning. |

### Applications

#### Medical VLMs
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| LLaVA-Med | ![img](https://github.com/microsoft/LLaVA-Med/raw/main/images/llava_med_logo.png) | [NeurIPS2023](https://arxiv.org/abs/2306.00890) | - | [Code](https://github.com/microsoft/LLaVA-Med) | Microsoft | Adapts LLaVA for biomedicine via self-instruct data from PubMed figure-caption pairs; strong on medical VQA. |
| Med-Flamingo | - | [arXiv](https://arxiv.org/abs/2307.15189) | - | [Code](https://github.com/snap-stanford/med-flamingo) | Stanford | A medical few-shot learner built on OpenFlamingo; fine-tuned on paired medical image-text data from textbooks. |

#### Document Understanding
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| mPLUG-DocOwl | - | [arXiv](https://arxiv.org/abs/2307.02499) | - | [Code](https://github.com/X-PLUG/mPLUG-DocOwl) | Alibaba | Instruction-tuned VLM for document understanding; handles OCR-free comprehension of documents, tables, and charts. |
| TextMonkey | - | [arXiv](https://arxiv.org/abs/2403.14252) | - | [Code](https://github.com/Yuliang-Liu/Monkey) | HUST | An OCR-free document understanding model with shifted window attention for high-resolution text-rich images. |

#### Video Understanding
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Video-LLaVA | - | [arXiv](https://arxiv.org/abs/2311.10122) | [Demo](https://huggingface.co/spaces/LanguageBind/Video-LLaVA) | [Code](https://github.com/PKU-YuanGroup/Video-LLaVA) | PKU | Unifies visual representations for images and videos to empower LLMs with video understanding capabilities. |
| VideoChat | - | [arXiv](https://arxiv.org/abs/2305.06355) | [Demo](https://huggingface.co/spaces/OpenGVLab/VideoChat) | [Code](https://github.com/OpenGVLab/Ask-Anything) | OpenGVLab | Chat-centric video understanding system combining video foundation models with LLMs for temporal reasoning. |
| TimeChat | - | [CVPR2024](https://arxiv.org/abs/2312.02051) | - | [Code](https://github.com/RenShuhuai-Andy/TimeChat) | PKU | A time-sensitive multimodal LLM for long video understanding with timestamp-aware frame encoding. |

#### Embodied AI
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| EmbodiedGPT | - | [NeurIPS2023](https://arxiv.org/abs/2305.15021) | [Project](https://embodiedgpt.github.io/) | [Code](https://github.com/EmbodiedGPT/EmbodiedGPT_Pytorch) | Shanghai AI Lab | Chain-of-thought embodied planning using VLMs; generates sub-goals and queries a policy network for execution. |
| SQA3D | - | [ICLR2023](https://arxiv.org/abs/2210.07474) | [Project](https://sqa3d.github.io/) | [Code](https://github.com/SilongYong/SQA3D) | HKUST | Situated Question Answering in 3D scenes; evaluates VLMs on spatial reasoning grounded in 3D environments. |

### Projects and Toolkits
| Title | Presentation | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|
| LLaMA-Factory | - | [Demo](https://huggingface.co/spaces/hiyouga/LLaMA-Board) | [Code](https://github.com/hiyouga/LLaMA-Factory) | - | Unified efficient fine-tuning framework supporting 100+ LLMs and VLMs with LoRA, QLoRA, and full fine-tuning. |
| LMDeploy | - | - | [Code](https://github.com/InternLM/lmdeploy) | Shanghai AI Lab | Efficient deployment toolkit for LLMs and VLMs with TurboMind engine; supports quantization and serving. |
| Awesome-Multimodal-LLMs | - | [Leaderboard](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models) | [Code](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models) | - | A curated list of multimodal LLM papers, evaluation benchmarks, and leaderboards. |
| OpenCompass | - | [Leaderboard](https://opencompass.org.cn/leaderboard-multimodal) | [Code](https://github.com/open-compass/opencompass) | OpenCompass | A unified evaluation platform for LLMs and VLMs covering 100+ datasets and 50+ models. |
| lmms-eval | - | [Leaderboard](https://lmms-lab.github.io/) | [Code](https://github.com/EvolvingLMMs-Lab/lmms-eval) | LMMs-Lab | One-command evaluation framework for large multimodal models across diverse vision-language benchmarks. |

## Acknowledgement
Some of the presentations in this repository are borrowed from the original authors, and we are very thankful for their contributions.

## License
This project is released under the MIT license.

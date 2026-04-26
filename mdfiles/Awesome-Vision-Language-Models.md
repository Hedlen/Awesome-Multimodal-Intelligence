<div align="center">
<br>
<image src="https://github.com/haotian-liu/LLaVA/raw/main/images/llava_logo.png", width="120px">
<br>
</div>

# Awesome Vision Language Models (VLMs) [![Awesome](https://cdn.rawgit.com/sindresorhus/awesome/d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome)

Vision Language Models (VLMs) have emerged as a transformative force at the intersection of computer vision and natural language processing, enabling machines to perceive, reason, and converse about the visual world. This repository continuously tracks and summarizes the research progress of VLMs across foundational models, benchmarks, applications, and toolkits.

If you find this repository helpful, please consider Stars ⭐ or Sharing ⬆️. Thanks.

## News
- 2026.4: Added Qwen3-VL, InternVL3, SigLIP 2, Molmo, Emu3, and comprehensive training datasets section.
- 2025.9: Added Qwen2.5-VL, LLaVA-OneVision, Idefics3, and updated benchmark section.
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
  - [Proprietary / Frontier VLMs](#proprietary--frontier-vlms)
- [Training Datasets](#training-datasets)
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
| SigLIP | - | [ICCV2023](https://arxiv.org/abs/2303.15343) | - | [Code](https://github.com/google-research/big_vision) | Google | Sigmoid Loss for Language Image Pre-Training; replaces softmax contrastive loss with pairwise sigmoid loss for better scaling. |
| SigLIP 2 | - | [arXiv](https://arxiv.org/abs/2502.14786) | - | [Code](https://github.com/google-research/big_vision) | Google | Multilingual vision-language encoders extending SigLIP with captioning-based pretraining, self-distillation, and masked prediction. |
| EVA-CLIP | - | [arXiv](https://arxiv.org/abs/2303.15389) | - | [Code](https://github.com/baaivision/EVA) | BAAI | Explores the limits of CLIP training at scale; EVA-CLIP-18B achieves SoTA zero-shot performance with 18B parameters. |
| DFN | - | [arXiv](https://arxiv.org/abs/2309.17425) | - | - | Apple | Data Filtering Networks for efficient and high-quality image-text data curation for CLIP-style training. |
| MetaCLIP | - | [ICLR2024](https://arxiv.org/abs/2309.16671) | - | [Code](https://github.com/facebookresearch/MetaCLIP) | Meta | Demystifies CLIP data curation; metadata-based balanced sampling from CommonCrawl achieves competitive performance. |

#### Generative VLMs
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Flamingo | ![img](https://github.com/mlfoundations/open_flamingo/raw/main/docs/flamingo.png) | [NeurIPS2022](https://arxiv.org/abs/2204.14198) | [Blog](https://www.deepmind.com/blog/tackling-multiple-tasks-with-a-single-visual-language-model) | [OpenFlamingo](https://github.com/mlfoundations/open_flamingo) | DeepMind | A family of VLMs for few-shot learning; interleaves images and text via cross-attention into a frozen LLM. |
| BLIP | - | [ICML2022](https://arxiv.org/abs/2201.12086) | - | [Code](https://github.com/salesforce/BLIP) | Salesforce | Bootstrapping Language-Image Pre-training with unified understanding and generation via CapFilt data bootstrapping. |
| BLIP-2 | ![img](https://github.com/salesforce/LAVIS/raw/main/docs/_static/logo_final.png) | [ICML2023](https://arxiv.org/abs/2301.12597) | [Demo](https://huggingface.co/spaces/Salesforce/BLIP2) | [Code](https://github.com/salesforce/LAVIS/tree/main/projects/blip2) | Salesforce | Bootstraps vision-language pre-training from frozen image encoders and LLMs via a lightweight Q-Former. |
| PaLM-E | ![img](https://palm-e.github.io/assets/palm-e-teaser.gif) | [arXiv](https://arxiv.org/abs/2303.03378) | [Project](https://palm-e.github.io/) | - | Google | An embodied multimodal language model (562B) that ingests robot sensor data directly into a language model. |
| mPLUG-Owl | - | [arXiv](https://arxiv.org/abs/2304.14178) | [Demo](https://www.modelscope.cn/studios/damo/mPLUG-Owl) | [Code](https://github.com/X-PLUG/mPLUG-Owl) | Alibaba DAMO | Modularization empowers LLMs with multimodality via a two-stage visual knowledge alignment strategy. |
| MiniGPT-4 | - | [arXiv](https://arxiv.org/abs/2304.10592) | [Demo](https://huggingface.co/spaces/Vision-CAIR/minigpt4) | [Code](https://github.com/Vision-CAIR/MiniGPT-4) | KAUST | Aligns a frozen visual encoder with Vicuna using a single projection layer; demonstrates GPT-4-like multimodal capabilities. |
| Otter | - | [arXiv](https://arxiv.org/abs/2305.03726) | - | [Code](https://github.com/Luodian/Otter) | NTU | Multi-modal in-context instruction tuning built on OpenFlamingo; introduces MIMIC-IT dataset for instruction following. |
| VisionLLM | - | [NeurIPS2023](https://arxiv.org/abs/2305.11175) | - | [Code](https://github.com/OpenGVLab/VisionLLM) | OpenGVLab | Uses LLM as an open-ended decoder for vision-centric tasks including detection, segmentation, and captioning. |
| Emu | - | [arXiv](https://arxiv.org/abs/2307.05222) | - | [Code](https://github.com/baaivision/Emu) | BAAI | Generalist multimodal model for both image understanding and generation; trained on interleaved image-text sequences. |
| Emu2 | - | [CVPR2024](https://arxiv.org/abs/2312.13286) | [Project](https://baaivision.github.io/emu2/) | [Code](https://github.com/baaivision/Emu) | BAAI | Generative multimodal model with strong in-context learning; supports image generation conditioned on interleaved inputs. |
| Emu3 | - | [arXiv](https://arxiv.org/abs/2409.18869) | [Project](https://emu.baai.ac.cn/) | [Code](https://github.com/baaivision/Emu3) | BAAI | Next-token prediction for multimodal understanding and generation; unifies image, video, and text in a single transformer. |
| Molmo | - | [arXiv](https://arxiv.org/abs/2409.17146) | [Demo](https://molmo.allenai.org/) | [Code](https://github.com/allenai/molmo) | AI2 | Open-weight VLM trained on PixMo dataset; achieves competitive performance with GPT-4V using fully open data pipeline. |

#### Instruction-Tuned VLMs
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| LLaVA | ![img](https://llava-vl.github.io/static/images/llava_logo.png) | [NeurIPS2023 Oral](https://arxiv.org/abs/2304.08485) | [Project](https://llava-vl.github.io/) | [Code](https://github.com/haotian-liu/LLaVA) | UW-Madison | Visual instruction tuning with GPT-4-generated data; first open-source model approaching GPT-4V-level multimodal chat. |
| LLaVA-1.5 | - | [CVPR2024](https://arxiv.org/abs/2310.03744) | [Project](https://llava-vl.github.io/) | [Code](https://github.com/haotian-liu/LLaVA) | UW-Madison | Improved LLaVA with MLP connector and academic-task-oriented data; achieves SoTA on 11 benchmarks with 13B params. |
| LLaVA-NeXT | - | [Blog](https://llava-vl.github.io/blog/2024-01-30-llava-next/) | [Project](https://llava-vl.github.io/) | [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) | UW-Madison | Improves LLaVA-1.5 with dynamic high-resolution image encoding; better OCR and document understanding. |
| LLaVA-OneVision | - | [arXiv](https://arxiv.org/abs/2408.03326) | [Demo](https://huggingface.co/spaces/lmms-lab/LLaVA-OneVision) | [Code](https://github.com/LLaVA-VL/LLaVA-NeXT) | ByteDance & NTU | Unifies single-image, multi-image, and video understanding in one model; SoTA on diverse multimodal benchmarks. |
| InstructBLIP | - | [NeurIPS2023](https://arxiv.org/abs/2305.06500) | [Demo](https://huggingface.co/spaces/hysts/InstructBLIP) | [Code](https://github.com/salesforce/LAVIS/tree/main/projects/instructblip) | Salesforce | Instruction-tuned BLIP-2 with instruction-aware Q-Former; SoTA zero-shot on 13 held-out datasets. |
| Qwen-VL | - | [arXiv](https://arxiv.org/abs/2308.12966) | [Demo](https://huggingface.co/spaces/Qwen/Qwen-VL-Chat-Demo) | [Code](https://github.com/QwenLM/Qwen-VL) | Alibaba | A versatile LVLM supporting image captioning, VQA, visual localization, and flexible interaction; strong on Chinese benchmarks. |
| Qwen2-VL | - | [arXiv](https://arxiv.org/abs/2409.12191) | [Demo](https://huggingface.co/spaces/Qwen/Qwen2-VL) | [Code](https://github.com/QwenLM/Qwen2-VL) | Alibaba | Introduces Naive Dynamic Resolution and Multimodal Rotary Position Embedding (M-RoPE) for any-resolution image understanding. |
| Qwen2.5-VL | - | [arXiv](https://arxiv.org/abs/2502.13923) | [Demo](https://huggingface.co/spaces/Qwen/Qwen2.5-VL) | [Code](https://github.com/QwenLM/Qwen2.5-VL) | Alibaba | Enhanced Qwen2-VL with improved document parsing, fine-grained video understanding, and agentic capabilities. |
| Qwen3-VL | - | [Blog](https://qwenlm.github.io/blog/qwen3-vl/) | - | [Code](https://github.com/QwenLM/Qwen3-VL) | Alibaba | Next-generation multimodal LLM with deeper reasoning, broader action capabilities, and ultra-long context windows. |
| InternVL | - | [CVPR2024 Oral](https://arxiv.org/abs/2312.14238) | [Project](https://internvl.github.io/) | [Code](https://github.com/OpenGVLab/InternVL) | OpenGVLab | A pioneering open-source alternative to GPT-4o; InternVL 2.5-78B first open model to exceed 70% on MMMU. |
| InternVL3 | - | [arXiv](https://arxiv.org/abs/2504.10479) | [Project](https://internvl.github.io/) | [Code](https://github.com/OpenGVLab/InternVL) | OpenGVLab | Advanced training and test-time recipes; further closes gap with proprietary models on multimodal reasoning. |
| CogVLM | - | [arXiv](https://arxiv.org/abs/2311.03079) | [Demo](https://huggingface.co/spaces/THUDM/CogVLM) | [Code](https://github.com/THUDM/CogVLM) | Tsinghua | Deep visual-language feature alignment via a trainable visual expert module; strong on grounding and referring tasks. |
| CogVLM2 | - | [arXiv](https://arxiv.org/abs/2408.16500) | - | [Code](https://github.com/THUDM/CogVLM2) | Tsinghua | Improved CogVLM with better high-resolution support and video understanding capabilities. |
| ShareGPT4V | - | [arXiv](https://arxiv.org/abs/2311.12793) | [Project](https://sharegpt4v.github.io/) | [Code](https://github.com/InternLM/InternLM-XComposer/tree/main/projects/ShareGPT4V) | Shanghai AI Lab | Improves LMMs with 1.2M high-quality GPT-4V-generated captions; significant gains in pre-training and SFT phases. |
| Idefics2 | - | [arXiv](https://arxiv.org/abs/2405.02246) | [Demo](https://huggingface.co/spaces/HuggingFaceM4/idefics2_playground) | [Code](https://github.com/huggingface/transformers) | HuggingFace | An 8B efficient foundational VLM; consolidates best practices for architecture, data, and training of VLMs. |
| Idefics3 | - | [arXiv](https://arxiv.org/abs/2408.12637) | - | [Code](https://github.com/huggingface/transformers) | HuggingFace | Builds on Idefics2 with Llama 3.1 backbone and DocOwl-style slicing for improved document and high-res understanding. |
| Cambrian-1 | - | [arXiv](https://arxiv.org/abs/2406.16860) | [Project](https://cambrian-mllm.github.io/) | [Code](https://github.com/cambrian-mllm/cambrian) | NYU | Spatial Vision Aggregator for multi-source visual feature fusion; strong on science and spatial reasoning benchmarks. |
| VILA | - | [CVPR2024](https://arxiv.org/abs/2312.07533) | - | [Code](https://github.com/NVlabs/VILA) | NVIDIA | Interleaved image-text pre-training enables multi-image reasoning and in-context learning; deployable on Jetson Orin. |
| InternLM-XComposer | - | [arXiv](https://arxiv.org/abs/2309.15112) | - | [Code](https://github.com/InternLM/InternLM-XComposer) | Shanghai AI Lab | Crafts interleaved text-image articles and answers diverse multimodal questions with high fidelity. |
| mPLUG-Owl2 | - | [CVPR2024](https://arxiv.org/abs/2311.04257) | - | [Code](https://github.com/X-PLUG/mPLUG-Owl) | Alibaba | Modality-collaborative training with shared and modality-specific modules; strong on both language and vision tasks. |

#### Grounding and Localization
| Title               | Presentation | Paper page                                   | Project page                                                         | Code base                                                                           | Affiliation   | Description                                                                                                         |
| :-------------------:| :------------:| :--------------------------------------------:| :--------------------------------------------------------------------:| :-----------------------------------------------------------------------------------:| :-------------:| :-------------------------------------------------------------------------------------------------------------------:|
| KOSMOS-2            | -            | [arXiv](https://arxiv.org/abs/2306.14824)    | [Demo](https://huggingface.co/spaces/ydshieh/Kosmos-2)               | [Code](https://github.com/microsoft/unilm/tree/master/kosmos-2)                     | Microsoft     | Grounds language to the visual world via referring expression comprehension and generation with bounding boxes.     |
| Grounding DINO      | -            | [arXiv](https://arxiv.org/abs/2303.05499)    | [Demo](https://huggingface.co/spaces/ShilongLiu/Grounding_DINO_demo) | [Code](https://github.com/IDEA-Research/GroundingDINO)                              | IDEA Research | Open-set object detector combining DINO with grounded pre-training; detects arbitrary objects from text prompts.    |
| Grounding DINO 1.5  | -            | [arXiv](https://arxiv.org/abs/2405.10300)    | -                                                                    | [Code](https://github.com/IDEA-Research/Grounding-DINO-1.5-API)                     | IDEA Research | Scales up Grounding DINO with more data and a stronger backbone; achieves SoTA on COCO and ODINW benchmarks.        |
| OWL-ViT             | -            | [ECCV2022](https://arxiv.org/abs/2205.06230) | -                                                                    | [Code](https://github.com/google-research/scenic/tree/main/scenic/projects/owl_vit) | Google        | Open-vocabulary object detection with image-level contrastive pre-training and transfer to detection.               |
| OWLv2               | -            | [arXiv](https://arxiv.org/abs/2306.09683)    | -                                                                    | [Code](https://github.com/google-research/scenic/tree/main/scenic/projects/owl_vit) | Google        | Scales OWL-ViT with self-training on web image-text data; strong open-vocabulary detection without box annotations. |
| Shikra              | -            | [arXiv](https://arxiv.org/abs/2306.15195)    | -                                                                    | [Code](https://github.com/shikras/shikra)                                           | SenseTime     | Unified VLM that handles referring expression comprehension and generation in natural language coordinates.         |
| Qwen-VL (Grounding) | -            | [arXiv](https://arxiv.org/abs/2308.12966)    | -                                                                    | [Code](https://github.com/QwenLM/Qwen-VL)                                           | Alibaba       | Supports fine-grained visual grounding with bounding box output in natural language; strong on RefCOCO benchmarks.  |
| GLaMM               | -            | [CVPR2024](https://arxiv.org/abs/2311.03356) | [Project](https://mbzuai-oryx.github.io/groundingLMM/)               | [Code](https://github.com/mbzuai-oryx/groundingLMM)                                 | MBZUAI        | Grounding Large Multimodal Model; pixel-level grounding with region-level and pixel-level descriptions.             |
| SAM 2               | -            | [arXiv](https://arxiv.org/abs/2408.00714)    | [Project](https://ai.meta.com/sam2/)                                 | [Code](https://github.com/facebookresearch/segment-anything-2)                      | Meta          | Segment Anything Model 2; extends SAM to video with streaming memory for real-time promptable segmentation.         |

#### Efficient and Lightweight VLMs
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| MobileVLM | - | [arXiv](https://arxiv.org/abs/2312.16886) | - | [Code](https://github.com/Meituan-AutoML/MobileVLM) | Meituan | A fast and strong multimodal language model for mobile devices with a lightweight downsampling projector. |
| MobileVLM V2 | - | [arXiv](https://arxiv.org/abs/2402.03766) | - | [Code](https://github.com/Meituan-AutoML/MobileVLM) | Meituan | Improved MobileVLM with better visual projector and training recipe; stronger on mobile deployment benchmarks. |
| MoE-LLaVA | - | [arXiv](https://arxiv.org/abs/2401.15947) | [Demo](https://huggingface.co/spaces/LanguageBind/MoE-LLaVA) | [Code](https://github.com/PKU-YuanGroup/MoE-LLaVA) | PKU | Mixture of Experts for LLaVA; activates sparse experts per token to scale capacity without proportional compute cost. |
| SmolVLM | - | [Blog](https://huggingface.co/blog/smolvlm) | [Demo](https://huggingface.co/spaces/HuggingFaceTB/SmolVLM) | [Code](https://github.com/huggingface/smollm) | HuggingFace | A compact 2B VLM designed for on-device deployment; strong performance-to-size ratio across multimodal benchmarks. |
| PaliGemma | - | [arXiv](https://arxiv.org/abs/2407.07726) | [Demo](https://huggingface.co/spaces/google/paligemma) | [Code](https://github.com/google-research/big_vision) | Google | A versatile 3B VLM combining SigLIP vision encoder with Gemma LLM; strong transfer across diverse vision tasks. |
| PaliGemma 2 | - | [arXiv](https://arxiv.org/abs/2412.03555) | - | [Code](https://github.com/google-research/big_vision) | Google | Improved PaliGemma with Gemma 2 backbone; available in 3B/10B/28B sizes with better reasoning and OCR. |
| Phi-3-Vision | - | [arXiv](https://arxiv.org/abs/2404.14219) | - | [Code](https://huggingface.co/microsoft/Phi-3-vision-128k-instruct) | Microsoft | Small but capable 4.2B VLM; strong on chart/document understanding with 128K context window. |
| Phi-4-Vision | - | [arXiv](https://arxiv.org/abs/2503.01743) | - | [Code](https://huggingface.co/microsoft/phi-4-multimodal-instruct) | Microsoft | Multimodal Phi-4 with vision and audio; strong reasoning with small footprint for edge deployment. |
| InternVL2-1B | - | [arXiv](https://arxiv.org/abs/2312.14238) | - | [Code](https://github.com/OpenGVLab/InternVL) | OpenGVLab | Smallest InternVL2 variant at 1B parameters; competitive with larger models on many benchmarks. |

#### Proprietary / Frontier VLMs
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| GPT-4V | - | [Blog](https://openai.com/research/gpt-4v-system-card) | [Demo](https://chat.openai.com/) | - | OpenAI | GPT-4 with vision; strong multimodal reasoning, OCR, and chart understanding; sets the bar for proprietary VLMs. |
| GPT-4o | - | [Blog](https://openai.com/index/hello-gpt-4o/) | [Demo](https://chat.openai.com/) | - | OpenAI | Omni model processing text, audio, and images natively; faster and cheaper than GPT-4V with improved vision. |
| Gemini 1.5 Pro | - | [arXiv](https://arxiv.org/abs/2403.05530) | [Demo](https://gemini.google.com/) | - | Google DeepMind | Multimodal model with 1M token context window; strong on long-document and long-video understanding. |
| Gemini 2.0 Flash | - | [Blog](https://deepmind.google/technologies/gemini/flash/) | [Demo](https://gemini.google.com/) | - | Google DeepMind | Fast and efficient Gemini 2.0 variant with native multimodal output including image and audio generation. |
| Claude 3.5 Sonnet | - | [Blog](https://www.anthropic.com/news/claude-3-5-sonnet) | [Demo](https://claude.ai/) | - | Anthropic | Strong vision capabilities with computer use; excels at document analysis and visual reasoning tasks. |

### Training Datasets
| Title | Scale | Paper page | Project page | Code / Data | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| CC3M | 3.3M | [ACL2018](https://arxiv.org/abs/1803.07670) | - | [Data](https://ai.google.com/research/ConceptualCaptions/) | Google | Conceptual Captions; 3.3M image-text pairs harvested from the web with automatic filtering and hypernymization. |
| CC12M | 12M | [CVPR2021](https://arxiv.org/abs/2102.08981) | - | [Data](https://github.com/google-research-datasets/conceptual-12m) | Google | Conceptual 12M; relaxed filtering of CC3M pipeline to yield 12M diverse image-text pairs for VLP. |
| YFCC100M | 100M | [CACM2016](https://arxiv.org/abs/1503.01817) | - | [Data](https://multimediacommons.wordpress.com/yfcc100m-core-dataset/) | Yahoo | 100M Flickr photos and videos with metadata; widely used for vision-language pre-training research. |
| WIT | 37.6M | [SIGIR2021](https://arxiv.org/abs/2103.01913) | - | [Data](https://github.com/google-research-datasets/wit) | Google | Wikipedia-based Image Text dataset; 37.6M image-text pairs from 108 languages for multilingual VLP. |
| LAION-400M | 400M | [arXiv](https://arxiv.org/abs/2111.02114) | [Project](https://laion.ai/) | [Data](https://laion.ai/blog/laion-400-open-dataset/) | LAION | 400M CLIP-filtered image-text pairs from Common Crawl; first large-scale open dataset for CLIP training. |
| LAION-5B | 5.85B | [NeurIPS2022](https://arxiv.org/abs/2210.08402) | [Project](https://laion.ai/) | [Data](https://laion.ai/blog/laion-5b/) | LAION | 5.85B CLIP-filtered image-text pairs; the largest open multimodal dataset enabling training of large VLMs. |
| COYO-700M | 700M | [arXiv](https://arxiv.org/abs/2209.01785) | - | [Data](https://github.com/kakaobrain/coyo-dataset) | Kakao Brain | 700M image-text pairs with rich metadata; higher quality than LAION through stricter filtering. |
| DataComp-1B | 1.28B | [NeurIPS2023](https://arxiv.org/abs/2304.14108) | [Project](https://www.datacomp.ai/) | [Data](https://github.com/mlfoundations/datacomp) | UW & others | A benchmark for dataset design; 1.28B filtered image-text pairs with standardized evaluation protocol. |
| LLaVA-Instruct-150K | 150K | [NeurIPS2023](https://arxiv.org/abs/2304.08485) | - | [Data](https://huggingface.co/datasets/liuhaotian/LLaVA-Instruct-150K) | UW-Madison | GPT-4-generated visual instruction tuning data; conversations, detailed descriptions, and complex reasoning. |
| ShareGPT4V-PT | 1.2M | [arXiv](https://arxiv.org/abs/2311.12793) | - | [Data](https://huggingface.co/datasets/Lin-Chen/ShareGPT4V) | Shanghai AI Lab | 1.2M high-quality GPT-4V-generated captions for diverse images; significantly improves VLM pre-training. |
| ALLaVA | 1.4M | [arXiv](https://arxiv.org/abs/2402.11684) | - | [Data](https://huggingface.co/datasets/FreedomIntelligence/ALLaVA-4V) | CUHK-SZ | High-quality instruction-following data generated by GPT-4V; covers diverse visual tasks and reasoning. |
| PixMo | ~1M | [arXiv](https://arxiv.org/abs/2409.17146) | - | [Data](https://huggingface.co/datasets/allenai/pixmo-docs) | AI2 | Fully open dataset for Molmo; includes dense captions, Q&A, and pointing data collected from human annotators. |
| OBELICS | 141M | [NeurIPS2023](https://arxiv.org/abs/2306.16527) | - | [Data](https://huggingface.co/datasets/HuggingFaceM4/OBELICS) | HuggingFace | 141M interleaved image-text documents from Common Crawl; used for training Idefics models. |
| MMC4 | 103M | [NeurIPS2023](https://arxiv.org/abs/2304.06939) | - | [Data](https://github.com/allenai/mmc4) | AI2 | Multimodal C4; 103M interleaved image-text documents for training open-source Flamingo-style models. |
| The Cauldron | 50 datasets | [arXiv](https://arxiv.org/abs/2405.02246) | - | [Data](https://huggingface.co/datasets/HuggingFaceM4/the_cauldron) | HuggingFace | A mixture of 50 vision-language datasets for instruction fine-tuning; used for Idefics2 training. |

### Benchmarks and Evaluation
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| VQAv2 | - | [CVPR2017](https://arxiv.org/abs/1612.00837) | [Project](https://visualqa.org/) | [Code](https://github.com/GT-Vision-Lab/VQA) | Georgia Tech | Visual Question Answering benchmark with 1.1M QA pairs; tests fine-grained visual understanding. |
| GQA | - | [CVPR2019](https://arxiv.org/abs/1902.09506) | [Project](https://cs.stanford.edu/people/dorarad/gqa/) | [Code](https://github.com/stanfordnlp/GQA) | Stanford | Compositional question answering over scene graphs; tests multi-step reasoning and spatial understanding. |
| TextVQA | - | [CVPR2019](https://arxiv.org/abs/1904.08920) | [Project](https://textvqa.org/) | [Code](https://github.com/facebookresearch/mmf) | Meta | VQA requiring reading and reasoning about text in images; tests OCR and text-grounded reasoning. |
| DocVQA | - | [WACV2021](https://arxiv.org/abs/2007.00398) | [Project](https://www.docvqa.org/) | [Code](https://github.com/anisha2102/docvqa) | IIIT Hyderabad | Document Visual QA; tests understanding of scanned documents including tables, forms, and figures. |
| MMBench | - | [arXiv](https://arxiv.org/abs/2307.06281) | [Leaderboard](https://mmbench.opencompass.org.cn/leaderboard) | [Code](https://github.com/open-compass/MMBench) | OpenCompass | A systematically designed objective benchmark for holistic evaluation of VLMs across 20 ability dimensions. |
| MMMU | - | [CVPR2024](https://arxiv.org/abs/2311.16502) | [Project](https://mmmu-benchmark.github.io/) | [Code](https://github.com/MMMU-Benchmark/MMMU) | UMich & others | Massive Multi-discipline Multimodal Understanding; 11.5K college-level questions across 30 subjects. |
| MMMU-Pro | - | [arXiv](https://arxiv.org/abs/2409.02813) | - | [Code](https://github.com/MMMU-Benchmark/MMMU) | UMich & others | Harder version of MMMU with more options and vision-only questions; better discriminates frontier models. |
| MME | - | [arXiv](https://arxiv.org/abs/2306.13394) | - | [Code](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models/tree/Evaluation) | Xiamen University | A comprehensive evaluation benchmark measuring both perception and cognition abilities of MLLMs. |
| SeedBench | - | [CVPR2024](https://arxiv.org/abs/2307.16125) | [Leaderboard](https://huggingface.co/spaces/AILab-CVC/SEED-Bench_Leaderboard) | [Code](https://github.com/AILab-CVC/SEED-Bench) | Tencent AI Lab | Evaluates generative comprehension of MLLMs with 19K multiple-choice questions across 12 evaluation dimensions. |
| SeedBench-2 | - | [arXiv](https://arxiv.org/abs/2311.17092) | - | [Code](https://github.com/AILab-CVC/SEED-Bench) | Tencent AI Lab | Extends SeedBench with 24K questions covering image and video understanding across 27 evaluation dimensions. |
| LLaVA-Bench | - | [NeurIPS2023](https://arxiv.org/abs/2304.08485) | - | [Code](https://github.com/haotian-liu/LLaVA) | UW-Madison | In-the-wild benchmark for instruction-following VLMs covering conversation, detail description, and complex reasoning. |
| MMStar | - | [arXiv](https://arxiv.org/abs/2403.20330) | [Leaderboard](https://mmstar-benchmark.github.io/) | [Code](https://github.com/MMStar-Benchmark/MMStar) | OpenGVLab | Elite 1.5K visual-indispensable benchmark; filters out language-solvable questions to test true visual reasoning. |
| MathVista | - | [ICLR2024](https://arxiv.org/abs/2310.02255) | [Project](https://mathvista.github.io/) | [Code](https://github.com/lupantech/MathVista) | UCLA | Mathematical reasoning in visual contexts; 6.1K problems across diverse math tasks and visual types. |
| ChartQA | - | [ACL2022](https://arxiv.org/abs/2203.10244) | - | [Code](https://github.com/vis-nlp/ChartQA) | York University | QA benchmark for chart understanding requiring visual and logical reasoning over bar, line, and pie charts. |
| OCRBench | - | [arXiv](https://arxiv.org/abs/2305.07895) | - | [Code](https://github.com/Yuliang-Liu/MultimodalOCR) | HUST | Comprehensive OCR evaluation for LMMs; covers text recognition, document parsing, and key information extraction. |
| HallusionBench | - | [CVPR2024](https://arxiv.org/abs/2310.14566) | - | [Code](https://github.com/tianyi-lab/HallusionBench) | UMD | Evaluates language hallucination and visual illusion in VLMs; tests whether models rely on language priors. |
| POPE | - | [EMNLP2023](https://arxiv.org/abs/2305.10355) | - | [Code](https://github.com/AoiDragon/POPE) | Jilin University | Polling-based Object Probing Evaluation for object hallucination in VLMs; simple yes/no questions. |
| Video-MME | - | [arXiv](https://arxiv.org/abs/2405.21075) | [Project](https://video-mme.github.io/) | [Code](https://github.com/BradyFU/Video-MME) | Tencent | Comprehensive video understanding benchmark with 2.7K videos across 30 domains and multiple durations. |
| MVBench | - | [CVPR2024](https://arxiv.org/abs/2311.17005) | - | [Code](https://github.com/OpenGVLab/Ask-Anything) | OpenGVLab | Multi-task video understanding benchmark with 20 challenging tasks requiring temporal reasoning. |

### Applications

#### Medical VLMs
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| LLaVA-Med | - | [NeurIPS2023](https://arxiv.org/abs/2306.00890) | - | [Code](https://github.com/microsoft/LLaVA-Med) | Microsoft | Adapts LLaVA for biomedicine via self-instruct data from PubMed figure-caption pairs; strong on medical VQA. |
| Med-Flamingo | - | [arXiv](https://arxiv.org/abs/2307.15189) | - | [Code](https://github.com/snap-stanford/med-flamingo) | Stanford | A medical few-shot learner built on OpenFlamingo; fine-tuned on paired medical image-text data from textbooks. |
| BioViL-T | - | [ECCV2022](https://arxiv.org/abs/2204.09817) | - | [Code](https://github.com/microsoft/hi-ml) | Microsoft | Temporal biomedical vision-language model for longitudinal chest X-ray analysis. |
| MedVersa | - | [arXiv](https://arxiv.org/abs/2405.01463) | - | [Code](https://github.com/zjunlp/MedVersa) | ZJU | A generalist medical AI system supporting diverse clinical tasks across multiple imaging modalities. |

#### Document Understanding
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| mPLUG-DocOwl | - | [arXiv](https://arxiv.org/abs/2307.02499) | - | [Code](https://github.com/X-PLUG/mPLUG-DocOwl) | Alibaba | Instruction-tuned VLM for document understanding; handles OCR-free comprehension of documents, tables, and charts. |
| mPLUG-DocOwl 1.5 | - | [arXiv](https://arxiv.org/abs/2403.12895) | - | [Code](https://github.com/X-PLUG/mPLUG-DocOwl) | Alibaba | Unified structure learning for OCR-free document understanding; high-resolution encoding with H-Reducer. |
| TextMonkey | - | [arXiv](https://arxiv.org/abs/2403.14252) | - | [Code](https://github.com/Yuliang-Liu/Monkey) | HUST | An OCR-free document understanding model with shifted window attention for high-resolution text-rich images. |
| InternVL-Doc | - | [arXiv](https://arxiv.org/abs/2312.14238) | - | [Code](https://github.com/OpenGVLab/InternVL) | OpenGVLab | InternVL applied to document understanding; strong on DocVQA, ChartQA, and InfoVQA benchmarks. |
| GOT-OCR2.0 | - | [arXiv](https://arxiv.org/abs/2409.01704) | - | [Code](https://github.com/Ucas-HaoranWei/GOT-OCR2.0) | UCAS | General OCR Theory; end-to-end OCR model supporting plain text, formatted text, and scene text. |

#### Video Understanding
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| Video-LLaVA | - | [arXiv](https://arxiv.org/abs/2311.10122) | [Demo](https://huggingface.co/spaces/LanguageBind/Video-LLaVA) | [Code](https://github.com/PKU-YuanGroup/Video-LLaVA) | PKU | Unifies visual representations for images and videos to empower LLMs with video understanding capabilities. |
| VideoChat | - | [arXiv](https://arxiv.org/abs/2305.06355) | [Demo](https://huggingface.co/spaces/OpenGVLab/VideoChat) | [Code](https://github.com/OpenGVLab/Ask-Anything) | OpenGVLab | Chat-centric video understanding system combining video foundation models with LLMs for temporal reasoning. |
| TimeChat | - | [CVPR2024](https://arxiv.org/abs/2312.02051) | - | [Code](https://github.com/RenShuhuai-Andy/TimeChat) | PKU | A time-sensitive multimodal LLM for long video understanding with timestamp-aware frame encoding. |
| InternVideo2 | - | [arXiv](https://arxiv.org/abs/2403.15377) | - | [Code](https://github.com/OpenGVLab/InternVideo) | OpenGVLab | Scaling video foundation models with progressive training; SoTA on video understanding and retrieval. |
| LongVA | - | [arXiv](https://arxiv.org/abs/2406.16852) | - | [Code](https://github.com/EvolvingLMMs-Lab/LongVA) | LMMs-Lab | Long context transfer for video understanding; processes 2000+ frames with 224K token context. |

#### Embodied AI
| Title | Presentation | Paper page | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|:---:|
| EmbodiedGPT | - | [NeurIPS2023](https://arxiv.org/abs/2305.15021) | [Project](https://embodiedgpt.github.io/) | [Code](https://github.com/EmbodiedGPT/EmbodiedGPT_Pytorch) | Shanghai AI Lab | Chain-of-thought embodied planning using VLMs; generates sub-goals and queries a policy network for execution. |
| SQA3D | - | [ICLR2023](https://arxiv.org/abs/2210.07474) | [Project](https://sqa3d.github.io/) | [Code](https://github.com/SilongYong/SQA3D) | HKUST | Situated Question Answering in 3D scenes; evaluates VLMs on spatial reasoning grounded in 3D environments. |
| 3D-LLM | - | [NeurIPS2023](https://arxiv.org/abs/2307.12981) | [Project](https://vis-www.cs.umass.edu/3dllm/) | [Code](https://github.com/UMass-Foundation-Model/3D-LLM) | UMass | Injects 3D world representations into LLMs; enables 3D question answering, captioning, and task planning. |
| LEO | - | [ICML2024](https://arxiv.org/abs/2311.12871) | [Project](https://embodied-generalist.github.io/) | [Code](https://github.com/embodied-generalist/embodied-generalist) | NTU | An embodied generalist agent for 3D world understanding and interaction; unifies perception, grounding, and action. |

### Projects and Toolkits
| Title | Presentation | Project page | Code base | Affiliation | Description |
|:---:|:---:|:---:|:---:|:---:|:---:|
| LLaMA-Factory | - | [Demo](https://huggingface.co/spaces/hiyouga/LLaMA-Board) | [Code](https://github.com/hiyouga/LLaMA-Factory) | - | Unified efficient fine-tuning framework supporting 100+ LLMs and VLMs with LoRA, QLoRA, and full fine-tuning. |
| LMDeploy | - | - | [Code](https://github.com/InternLM/lmdeploy) | Shanghai AI Lab | Efficient deployment toolkit for LLMs and VLMs with TurboMind engine; supports quantization and serving. |
| Awesome-Multimodal-LLMs | - | [Leaderboard](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models) | [Code](https://github.com/BradyFU/Awesome-Multimodal-Large-Language-Models) | - | A curated list of multimodal LLM papers, evaluation benchmarks, and leaderboards. |
| OpenCompass | - | [Leaderboard](https://opencompass.org.cn/leaderboard-multimodal) | [Code](https://github.com/open-compass/opencompass) | OpenCompass | A unified evaluation platform for LLMs and VLMs covering 100+ datasets and 50+ models. |
| lmms-eval | - | [Leaderboard](https://lmms-lab.github.io/) | [Code](https://github.com/EvolvingLMMs-Lab/lmms-eval) | LMMs-Lab | One-command evaluation framework for large multimodal models across diverse vision-language benchmarks. |
| LAVIS | - | - | [Code](https://github.com/salesforce/LAVIS) | Salesforce | A one-stop library for language-vision intelligence; supports BLIP, BLIP-2, InstructBLIP, and more. |
| Transformers (HF) | - | [Docs](https://huggingface.co/docs/transformers) | [Code](https://github.com/huggingface/transformers) | HuggingFace | The de-facto library for VLM inference and fine-tuning; supports 100+ VLMs out of the box. |

## Acknowledgement
Some of the presentations in this repository are borrowed from the original authors, and we are very thankful for their contributions.

## License
This project is released under the MIT license.

<div align="center">

# 📚 AI Knowledge Hub

**Clear, well-organised notes on LLM training, data, AI evals and more —
distilled from the best talks and lectures, with slides you can reuse.**

[![License: CC BY 4.0](https://img.shields.io/badge/License-CC_BY_4.0-lightgrey.svg)](LICENSE)
[![Website](https://img.shields.io/badge/Website-alihashemi--ai.github.io-blue)](https://alihashemi-ai.github.io)

</div>

---

## 🗺️ Topics

| # | Topic | What you'll find |
|---|---|---|
| 01 | [🧠 LLM Fundamentals](topics/01-llm-fundamentals/) | Transformers, tokenization, scaling laws |
| 02 | [🏋️ **LLM Training**](topics/02-llm-training/) | Pre-training, SFT, LoRA, RLHF/DPO, distributed training |
| 03 | [🗂️ **Data for AI**](topics/03-data/) | Data curation, synthetic data, quality, contamination |
| 04 | [📏 **AI Evals**](topics/04-ai-evals/) | Benchmarks, LLM-as-a-judge, human evals, app evals. See [Position bias in LLM-as-a-judge](topics/04-ai-evals/2026-11-25-llm-judge-position-bias.md). |
| 05 | [⚡ Inference & Deployment](topics/05-inference-and-deployment/) | Serving, quantization, cost & latency |
| 06 | [🤖 Agents & Applications](topics/06-agents-and-applications/) | Prompting, RAG, agents, tool use |
| 07 | [🔍 Interpretability & Safety](topics/07-interpretability-and-safety/) | XAI, mech interp, uncertainty, alignment |
| 08 | [🌍 AI Research & Industry](topics/08-ai-research-and-industry/) | Trends, strategy, careers |

## 🧭 Suggested learning path

```
Fundamentals ──► Data ──► Training ──► Evals ──► Inference ──► Applications
     01            03         02          04          05             06
```

New to LLMs? Start with **01**. Building or fine-tuning models? Go to **03 → 02 → 04**.
Shipping AI products? Start with **06** and **04**.

## 🆕 Latest

| Date | Article | Topic | Slides |
|---|---|---|---|
| 2026-11-25 | [Position bias in LLM-as-a-judge](topics/04-ai-evals/2026-11-25-llm-judge-position-bias.md) | [AI Evals](topics/04-ai-evals/) | _forthcoming_ |

## 📦 What's in each article

Every article follows the same format, so content is easy to scan:

- **TL;DR**: the key insight in two sentences
- **Key insights**: the main ideas, with timestamps back to the original talk
- **My perspective**: commentary and how it connects to practice and research
- **Takeaways**: what to remember or apply
- **Slides**: a downloadable deck (PDF) in [`slides/`](slides/)

## 📖 Reading list

Talks, papers, courses and tools, grouped by topic. Titles and authors are taken from the source pages. All credit belongs to the original authors.

- [Evaluation and LLM-as-judge](#evaluation-and-llm-as-judge)
- [Data and synthetic data](#data-and-synthetic-data)
- [Training and scaling](#training-and-scaling)
- [MoE](#moe)
- [Inference](#inference)
- [GPUs and systems](#gpus-and-systems)
- [Courses and lecture series](#courses-and-lecture-series)
- [Channels](#channels)

A shorter list of foundational papers is in [resources/reading-list.md](resources/reading-list.md).

### Evaluation and LLM-as-judge

| Title | Author / org | Note |
|---|---|---|
| [Stanford CME295 Lecture 8: LLM Evaluation](https://www.youtube.com/watch?v=8fNP4N46RRo&t=2328s) | Afshine Amidi and Shervine Amidi (Stanford Online) | Source lecture for the [position bias article](topics/04-ai-evals/2026-11-25-llm-judge-position-bias.md). Judge biases start at 38:48. Also: [syllabus](https://cme295.stanford.edu/syllabus/2025/), [slides](https://cme295.stanford.edu/slides/fall25-cme295-lecture8.pdf). |
| [Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685) | Lianmin Zheng, Wei-Lin Chiang, Ying Sheng et al. | The paper behind LLM-as-a-judge. It measures position, verbosity and self-enhancement bias. |
| [Building strong safety evaluations](https://www.anthropic.com/research/building-strong-safety-evaluations) | Anthropic | Practical guidance on designing safety evaluations. |
| [FineTasks: finding signal in 100s of evaluation tasks](https://huggingface.co/spaces/HuggingFaceFW/blogpost-fine-tasks) | Hynek Kydlíček, Guilherme Penedo, Clémentine Fourier, Nathan Habib, Thomas Wolf (Hugging Face) | How to pick evaluation tasks that give a usable signal. |
| [Department of Evals](https://departmentofevals.substack.com/about) | The Evals team at Braintrust | Substack on evals methodology and analysis. |
| [Give Me 45 Minutes, I'll Make LLM Evaluation Click Forever](https://www.youtube.com/watch?v=5NCmJA8VoAE&t=303s) | Zachary Huang | Video walkthrough of LLM evaluation (link starts at 5:03). |
| [Evaluation, Build Your Own LLM Workshop #20](https://www.youtube.com/watch?v=S6uLzsqOOUc) | Justin Angel | Workshop session on evaluating LLMs. |
| [From Vibes to Production: Evaluating and Shipping AI Agents That Work 101](https://www.youtube.com/watch?v=qZj7sqmidqA) | Laurie Voss (Arize AI), talk at AI Engineer | Talk on evaluating and shipping agents. |

### Data and synthetic data

| Title | Author / org | Note |
|---|---|---|
| [The Synthetic Data Playbook (FinePhrase)](https://huggingface.co/spaces/HuggingFaceFW/finephrase) | Joel Niklaus, Guilherme Penedo, Hynek Kydlicek, Elie Bakouch, Lewis Tunstall, Ed Beeching, Thibaud Frere, Colin Raffel, Leandro von Werra, Thomas Wolf (Hugging Face) | Experiments on synthetic pretraining data. Sections: [introduction](https://huggingface.co/spaces/HuggingFaceFW/finephrase#introduction), [math rephrasing, when worse outputs win](https://huggingface.co/spaces/HuggingFaceFW/finephrase#math-rephrasing-when-worse-outputs-win). |
| [What Makes Good Synthetic Pretraining Data](https://www.youtube.com/watch?v=Nk2HpRb1Vl4) | Joël Niklaus, interviewed on Deep Learning with Yacine | Interview with a FinePhrase author. |
| [How to Generate Synthetic Pretraining Data?](https://www.youtube.com/watch?v=bKdc0vpezw8) | Joël Niklaus, interviewed on Deep Learning with Yacine | Interview with a FinePhrase author. |
| [Building Synthetic Data Pipelines for Open Research and Scalable AI Development](https://www.youtube.com/watch?v=s_o0myJzh30) | NVIDIA Developer | Talk on synthetic data pipelines. |
| [How to Curate Text Data for LLM Pretraining with NVIDIA NeMo Curator](https://www.youtube.com/watch?v=3N-z1FgWbxw) | NVIDIA Developer | Data curation walkthrough. |
| [Optimizing Pretraining Data Mixes with LLM-Estimated Utility](https://huggingface.co/blog/WillHeld/utilimax-and-medu) | Will Held | Data mixing with LLM-estimated utility. |
| [Data Mixing for Large Language Models Pretraining: A Survey and Outlook](https://arxiv.org/abs/2604.16380) | Zhuo Chen, Yuxuan Miao, Supryadi, Deyi Xiong | Survey of data mixing for pretraining. [PDF](https://arxiv.org/pdf/2604.16380). |
| [Datasets documentation](https://huggingface.co/docs/datasets/en/index) | Hugging Face | Docs for the datasets library. |

### Training and scaling

| Title | Author / org | Note |
|---|---|---|
| [The Ultra-Scale Playbook: Training LLMs on GPU Clusters](https://huggingface.co/spaces/nanotron/ultrascale-playbook) | Nouamane Tazi, Ferdinand Mom, Haojun Zhao, Phuc Nguyen, Mohamed Mekkouri, Leandro von Werra, Thomas Wolf (Hugging Face) | Guide to training LLMs on large GPU clusters. |
| [The Ultra-Scale Playbook (video)](https://www.youtube.com/watch?v=og8Y6z2xC0I) | ThomWolf | Video companion to the playbook. |
| [Scaling LLM Training to Thousands of GPUs](https://www.youtube.com/watch?v=_Ig6_gAgFaQ) | Nouamane Tazi (Hugging Face), talk at BLISS e.V. Berlin | Talk by a playbook author. |
| [The Ultra-Scale Talk: Scaling Training to Thousands of GPUs](https://www.youtube.com/watch?v=8XXfOj-IUdY) | Nouamane Tazi (Hugging Face), talk at the PyTorch Foundation | Talk by a playbook author. |
| [Lecture 48: The Ultra Scale Playbook](https://www.youtube.com/watch?v=1E8GDR8QXKw) | GPU MODE | GPU MODE lecture on the playbook. |
| [CS25 V6: The Ultra-Scale Talk](https://www.youtube.com/watch?v=I5BKi32IEa8) | Stanford Online | CS25 session on scaling training to thousands of GPUs. |
| [How To Scale Your Model](https://jax-ml.github.io/scaling-book/) | Jacob Austin, Sholto Douglas, Roy Frostig, Anselm Levskaya, Charlie Chen, Sharad Vikram, Federico Lebron, Peter Choy, Vinay Ramasesh, Albert Webson, Reiner Pope (Google DeepMind and MatX) | Book on scaling models on TPUs and GPUs. |
| [Distributed LLM Training Explained: Data, Tensor and Pipeline Parallelism](https://www.youtube.com/watch?v=dHAEc9dmsF4) | Codemia | Parallelism overview. |
| [Give Me 42 Minutes, I'll Make LLM Post-Training Click Forever](https://www.youtube.com/watch?v=5l3l9aEwHlo) | Zachary Huang | Post-training explainer. |
| [Understanding the end-to-end LLM training and inference pipeline](https://www.youtube.com/watch?v=V2L6hufE2X4) | Mark Moyou, talk at PyData | End to end pipeline talk. |
| [Techniques for Efficient and Reproducible Foundation Model Pre-Training](https://www.youtube.com/watch?v=vHCVNr0uX_k) | NVIDIA Developer | Pretraining techniques talk. |
| [Reinforcement Learning, Kernels, Reasoning, Quantization and Agents](https://www.youtube.com/watch?v=OkEGJ5G3foU) | Daniel Han, workshop at AI Engineer | Full workshop on RL, kernels and quantization. |
| [Mastering LLM Techniques: Training](https://developer.nvidia.com/blog/mastering-llm-techniques-training/) | Anjali Shah, Tiffany Yeung, Annamalai Chockalingam (NVIDIA) | NVIDIA technical blog on training. |
| [Efficiently Scale LLM Training Across a Large GPU Cluster with Alpa and Ray](https://developer.nvidia.com/blog/efficiently-scale-llm-training-across-a-large-gpu-cluster-with-alpa-and-ray/) | Jiao Dong, Hao Zheng, Lianmin Zheng, Phi Nguyen | Alpa and Ray for large-cluster training. |
| [NVIDIA NeMo Accelerates LLM Innovation with Hybrid State Space Model Support](https://developer.nvidia.com/blog/nvidia-nemo-accelerates-llm-innovation-with-hybrid-state-space-model-support/) | Ashraf Eassa (NVIDIA) | SSM support in NeMo and Megatron-Core. |
| [Accelerate documentation](https://huggingface.co/docs/accelerate/en/index) | Hugging Face | Docs for distributed and mixed-precision training. |
| [PyTorch Distributed Overview](https://docs.pytorch.org/tutorials/beginner/dist_overview.html) | PyTorch | Official overview of the distributed APIs. |
| [Chat templates](https://huggingface.co/docs/transformers/en/chat_templating) | Hugging Face | How chat templates format conversations. |
| [LLM Model Pruning and Knowledge Distillation with NVIDIA NeMo Framework](https://developer.nvidia.com/blog/llm-model-pruning-and-knowledge-distillation-with-nvidia-nemo-framework/) | Gomathy Venkata Krishnan, Vinh Nguyen, Shashank Verma, Asha Anoosheh (NVIDIA) | Distillation and pruning. |
| [Compact Language Models via Pruning and Knowledge Distillation](https://arxiv.org/abs/2407.14679) | Saurav Muralidharan, Sharath Turuvekere Sreenivas, Raviraj Joshi, Marcin Chochowski, Mostofa Patwary, Mohammad Shoeybi, Bryan Catanzaro, Jan Kautz, Pavlo Molchanov | Distillation and pruning paper from NVIDIA. |
| [Everything You Need to Know about Knowledge Distillation](https://huggingface.co/blog/Kseniase/kd) | Ksenia Se and Alyona Vert | Distillation overview. |
| [Loop Engineering explained in 8min..](https://www.youtube.com/watch?v=4biXYSNkn9Y&t=1s) | Caleb Writes Code | Short explainer on loop engineering. |
| [Weight-Space Programming explained in 10min..](https://www.youtube.com/watch?v=77hHgDkbtLI) | Caleb Writes Code | Short explainer on weight-space programming. |

### MoE

| Title | Author / org | Note |
|---|---|---|
| [Mixture of Experts Explained](https://huggingface.co/blog/moe) | Omar Sanseviero, Lewis Tunstall, Philipp Schmid, Sourab Mangrulkar, Younes Belkada, Pedro Cuenca (Hugging Face) | Intro to MoE models. |
| [The Ultimate MoE Training Handbook](https://huggingface.co/spaces/huggingface/moe-blogpost) | Nouamane Tazi, Leandro von Werra, Thomas Wolf (Hugging Face) | Hands-on guide to training MoE models with Megatron-LM. See also [section 3.2, who selects](https://huggingface.co/spaces/huggingface/moe-blogpost#s-3-2-who-selects). |
| [Megatron-LM](https://github.com/NVIDIA/Megatron-LM) | NVIDIA | Training framework used in the MoE handbook, including the [MoE token dispatcher](https://github.com/NVIDIA/Megatron-LM/blob/d6316eb45bf1bfbb6f1f848c0b56e55166564d80/megatron/core/transformer/moe/token_dispatcher.py#L652-L657). |

### Inference

| Title | Author / org | Note |
|---|---|---|
| [Mastering LLM Techniques: Inference Optimization](https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization/) | Shashank Verma and Neal Vaidya (NVIDIA) | Prefill and decode, KV cache and batching. |
| [The Engineering Behind LLM Inference: Inside the GPU](https://www.youtube.com/watch?v=cbEhkd4ZeKs) | PY | Inference on the GPU. |
| [Inference Engines explained in 10min..](https://www.youtube.com/watch?v=_xM8scs4_x4) | Caleb Writes Code | Short explainer on inference engines. |
| [Give Me 1 Hour, I'll Make LLM Inference Engines Click Forever](https://www.youtube.com/watch?v=I2QhfZ0aVmk) | Zachary Huang | Inference engines walkthrough. |
| [How LLMs survive in low precision: Quantization Fundamentals](https://www.youtube.com/watch?v=qoQJq5UwV1c) | Julia Turc | Quantization basics. |

### GPUs and systems

| Title | Author / org | Note |
|---|---|---|
| [How to Think About GPUs](https://jax-ml.github.io/scaling-book/gpus/) | Jacob Austin, Swapnil Patil, Adam Paszke, Reiner Pope (Google DeepMind and MatX) | GPU chapter of How To Scale Your Model. |
| [TransformerEngine](https://github.com/NVIDIA/TransformerEngine) | NVIDIA | Library for accelerating Transformer models on NVIDIA GPUs, including FP8. |
| [Model-Optimizer examples/gpt-oss](https://github.com/NVIDIA/Model-Optimizer/tree/main/examples/gpt-oss) | NVIDIA | Example directory for gpt-oss in NVIDIA Model Optimizer. |

### Courses and lecture series

| Title | Author / org | Note |
|---|---|---|
| [CS25: Transformers United V6](https://web.stanford.edu/class/cs25/) | Stanford University | Seminar series on Transformers. Also: [recordings](https://web.stanford.edu/class/cs25/recordings/). |
| [Stanford CS25, Transformers United (playlist)](https://www.youtube.com/playlist?list=PLoROMvodv4rNiJRchCzutFw5ItR_Z27CM) | Stanford Online | Playlist of CS25 lectures. |
| [CS25 V6: From Representation Learning to World Modeling](https://www.youtube.com/watch?v=GBd7iuJkW08) | Stanford Online | One CS25 V6 session. |
| [LLM Course](https://github.com/mlabonne/llm-course) | Maxime Labonne | Roadmaps and Colab notebooks for LLMs (Apache-2.0). |

### Channels

| Title | Author / org | Note |
|---|---|---|
| [mesanu](https://www.youtube.com/@mesanu1/videos) | mesanu | YouTube channel: hard concepts, visualized and explained step by step. |
| [hu-po](https://www.youtube.com/@hu-po/streams) | hu-po | Livestreams on ML papers, coding and research. |

## 📚 Resources

- [Glossary](resources/glossary.md): key terms, explained simply
- [Foundational papers](resources/reading-list.md): classic papers collected by topic
- The longer list of talks, tools and courses is in the [Reading list](#reading-list) section above

## 👤 About

Curated by **Ali Hashemi**, AI/ML researcher. See [alihashemi-ai.github.io](https://alihashemi-ai.github.io).
Spotted an error or have a suggestion? [Open an issue](../../issues).

## 📝 License & attribution

Content is licensed under [CC BY 4.0](LICENSE): you may share and adapt it with credit.
Each article credits its original source; summaries and opinions are my own and do not
represent the views of the original speakers.

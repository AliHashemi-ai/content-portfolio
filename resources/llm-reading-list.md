# LLM reading list

[← Back to all topics](../README.md)

Public links collected for LLM evaluation, data, training, inference and systems. Every title and author was read from the page itself (arXiv metadata, YouTube oEmbed or page metadata) on 2026-11-28. All credit belongs to the original authors.

## Evaluation and LLM-as-judge

- [Stanford CME295 Transformers & LLMs | Autumn 2025 | Lecture 8 - LLM Evaluation](https://www.youtube.com/watch?v=8fNP4N46RRo&t=2328s), Afshine Amidi and Shervine Amidi (Stanford Online), Source lecture for the position bias post. LLM-as-a-judge, biases and benchmarks. Position, verbosity and self-enhancement bias chapter starts at about 38:48. Also: [Syllabus 2025](https://cme295.stanford.edu/syllabus/2025/); [Lecture 8 slides (PDF)](https://cme295.stanford.edu/slides/fall25-cme295-lecture8.pdf).
- [Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685), Lianmin Zheng, Wei-Lin Chiang, Ying Sheng, Siyuan Zhuang, Zhanghao Wu, Yonghao Zhuang, Zi Lin, Zhuohan Li, Dacheng Li, Eric P. Xing, Hao Zhang, Joseph E. Gonzalez, Ion Stoica, The paper behind LLM-as-a-judge. It measures position, verbosity and self-enhancement bias.
- [Building strong safety evaluations](https://www.anthropic.com/research/building-strong-safety-evaluations), Anthropic, Practical guidance on designing safety evaluations.
- [Scaling FineWeb to 1000+ languages: Step 1: finding signal in 100s of evaluation tasks](https://huggingface.co/spaces/HuggingFaceFW/blogpost-fine-tasks), Hynek Kydlíček, Guilherme Penedo, Clémentine Fourier, Nathan Habib, Thomas Wolf (Hugging Face), How to pick evaluation tasks that give a usable signal (FineTasks).
- [Department of Evals (About)](https://departmentofevals.substack.com/about), Department of Evals, the Evals team at Braintrust, Substack on evals methodology and analysis.
- [Give Me 45 Minutes, I'll Make LLM Evaluation Click Forever](https://www.youtube.com/watch?v=5NCmJA8VoAE&t=303s), Zachary Huang, Video walkthrough of LLM evaluation (link starts at 5:03).
- [Evaluation | Build Your Own LLM Workshop #20](https://www.youtube.com/watch?v=S6uLzsqOOUc), Justin Angel, Workshop session on evaluating LLMs.
- [From Vibes to Production: Evaluating and Shipping AI Agents That Work 101 — Laurie Voss, Arize AI](https://www.youtube.com/watch?v=qZj7sqmidqA), AI Engineer (talk by Laurie Voss, Arize AI), Talk on evaluating and shipping agents.

## Data and synthetic data

- [The Synthetic Data Playbook: Generating Trillions of the Finest Tokens (FinePhrase)](https://huggingface.co/spaces/HuggingFaceFW/finephrase), Joel Niklaus, Guilherme Penedo, Hynek Kydlicek, Elie Bakouch, Lewis Tunstall, Ed Beeching, Thibaud Frere, Colin Raffel, Leandro von Werra, Thomas Wolf (Hugging Face), Experiments on synthetic pretraining data. Also: [Introduction](https://huggingface.co/spaces/HuggingFaceFW/finephrase#introduction); [Math rephrasing: when worse outputs win](https://huggingface.co/spaces/HuggingFaceFW/finephrase#math-rephrasing-when-worse-outputs-win).
- [What Makes Good Synthetic Pretraining Data with Joël Niklaus from Hugginface (title as published)](https://www.youtube.com/watch?v=Nk2HpRb1Vl4), Deep Learning with Yacine, Interview with a FinePhrase author.
- [How to Generate Synthetic Pretraining Data? with Joël Niklaus from Hugginface (title as published)](https://www.youtube.com/watch?v=bKdc0vpezw8), Deep Learning with Yacine, Interview with a FinePhrase author.
- [Building Synthetic Data Pipelines for Open Research and Scalable AI Development](https://www.youtube.com/watch?v=s_o0myJzh30), NVIDIA Developer, Talk on synthetic data pipelines.
- [How to Curate Text Data for LLM Pretraining with NVIDIA NeMo Curator](https://www.youtube.com/watch?v=3N-z1FgWbxw), NVIDIA Developer, Data curation walkthrough.
- [Optimizing Pretraining Data Mixes with LLM-Estimated Utility](https://huggingface.co/blog/WillHeld/utilimax-and-medu), Will Held, Data mixing with LLM-estimated utility.
- [Data Mixing for Large Language Models Pretraining: A Survey and Outlook](https://arxiv.org/abs/2604.16380), Zhuo Chen, Yuxuan Miao, Supryadi, Deyi Xiong, Survey of data mixing for pretraining (arXiv v listing dated 2026-03-25). Ali shared the /pdf/ URL. Also: [PDF](https://arxiv.org/pdf/2604.16380).
- [Datasets (Hugging Face documentation)](https://huggingface.co/docs/datasets/en/index), Hugging Face, Docs for the datasets library.

## Training and scaling

- [The Ultra-Scale Playbook: Training LLMs on GPU Clusters](https://huggingface.co/spaces/nanotron/ultrascale-playbook), Nouamane Tazi, Ferdinand Mom, Haojun Zhao, Phuc Nguyen, Mohamed Mekkouri, Leandro von Werra, Thomas Wolf (Hugging Face), Guide to training LLMs on large GPU clusters.
- [The Ultra-Scale Playbook: Training LLMs on GPU Clusters](https://www.youtube.com/watch?v=og8Y6z2xC0I), ThomWolf (YouTube channel), Video on the playbook.
- [Scaling LLM Training to Thousands of GPUs | Nouamane Tazi, HuggingFace](https://www.youtube.com/watch?v=_Ig6_gAgFaQ), BLISS e.V. Berlin, Talk by a playbook author.
- [The Ultra-Scale Talk: Scaling Training to Thousands of GPUs - Nouamane Tazi, Hugging Face](https://www.youtube.com/watch?v=8XXfOj-IUdY), PyTorch Foundation, Talk by a playbook author.
- [Lecture 48: The Ultra Scale Playbook](https://www.youtube.com/watch?v=1E8GDR8QXKw), GPU MODE, GPU MODE lecture on the playbook.
- [Stanford CS25: Transformers United V6 I The Ultra-Scale Talk: Scaling Training to Thousands of GPUs](https://www.youtube.com/watch?v=I5BKi32IEa8), Stanford Online, CS25 V6 session (title from the watch page; oEmbed blocked).
- [How To Scale Your Model](https://jax-ml.github.io/scaling-book/), Jacob Austin, Sholto Douglas, Roy Frostig, Anselm Levskaya, Charlie Chen, Sharad Vikram, Federico Lebron, Peter Choy, Vinay Ramasesh, Albert Webson, Reiner Pope (Google DeepMind and MatX), Book on scaling LLMs on TPUs and GPUs.
- [Distributed LLM Training Explained: Data, Tensor and Pipeline Parallelism](https://www.youtube.com/watch?v=dHAEc9dmsF4), Codemia, Parallelism overview.
- [Give Me 42 Minutes, I'll Make LLM Post-Training Click Forever](https://www.youtube.com/watch?v=5l3l9aEwHlo), Zachary Huang, Post-training explainer.
- [Mark Moyou, PhD - Understanding the end-to-end LLM training and inference pipeline](https://www.youtube.com/watch?v=V2L6hufE2X4), PyData, End to end pipeline talk.
- [Techniques for Efficient and Reproducible Foundation Model Pre-Training](https://www.youtube.com/watch?v=vHCVNr0uX_k), NVIDIA Developer, Pretraining techniques talk.
- [[Full Workshop] Reinforcement Learning, Kernels, Reasoning, Quantization & Agents — Daniel Han](https://www.youtube.com/watch?v=OkEGJ5G3foU), AI Engineer (workshop by Daniel Han), Long workshop on RL, kernels and quantization.
- [Mastering LLM Techniques: Training](https://developer.nvidia.com/blog/mastering-llm-techniques-training/), Anjali Shah, Tiffany Yeung, Annamalai Chockalingam (NVIDIA), NVIDIA technical blog on training.
- [Efficiently Scale LLM Training Across a Large GPU Cluster with Alpa and Ray](https://developer.nvidia.com/blog/efficiently-scale-llm-training-across-a-large-gpu-cluster-with-alpa-and-ray/), Jiao Dong, Hao Zheng, Lianmin Zheng, Phi Nguyen (NVIDIA technical blog), Alpa and Ray for large-cluster training.
- [NVIDIA NeMo Accelerates LLM Innovation with Hybrid State Space Model Support](https://developer.nvidia.com/blog/nvidia-nemo-accelerates-llm-innovation-with-hybrid-state-space-model-support/), Ashraf Eassa (NVIDIA), SSM support in NeMo and Megatron-Core.
- [Accelerate (Hugging Face documentation)](https://huggingface.co/docs/accelerate/en/index), Hugging Face, Docs for distributed and mixed-precision training.
- [PyTorch Distributed Overview](https://docs.pytorch.org/tutorials/beginner/dist_overview.html), PyTorch, Official overview of the distributed APIs.
- [Chat templates (Transformers documentation)](https://huggingface.co/docs/transformers/en/chat_templating), Hugging Face, How chat templates format conversations.
- [LLM Model Pruning and Knowledge Distillation with NVIDIA NeMo Framework](https://developer.nvidia.com/blog/llm-model-pruning-and-knowledge-distillation-with-nvidia-nemo-framework/), Gomathy Venkata Krishnan, Vinh Nguyen, Shashank Verma, Asha Anoosheh (NVIDIA), Distillation and pruning.
- [Compact Language Models via Pruning and Knowledge Distillation](https://arxiv.org/abs/2407.14679), Saurav Muralidharan, Sharath Turuvekere Sreenivas, Raviraj Joshi, Marcin Chochowski, Mostofa Patwary, Mohammad Shoeybi, Bryan Catanzaro, Jan Kautz, Pavlo Molchanov, Distillation and pruning paper (NVIDIA).
- [Everything You Need to Know about Knowledge Distillation](https://huggingface.co/blog/Kseniase/kd), Ksenia Se and Alyona Vert, Distillation overview.
- [Loop Engineering explained in 8min..](https://www.youtube.com/watch?v=4biXYSNkn9Y&t=1s), Caleb Writes Code, Topic not classified by me beyond the title. Check relevance.
- [Weight-Space Programming explained in 10min..](https://www.youtube.com/watch?v=77hHgDkbtLI), Caleb Writes Code, Topic not classified by me beyond the title. Check relevance.

## MoE

- [Mixture of Experts Explained](https://huggingface.co/blog/moe), Omar Sanseviero, Lewis Tunstall, Philipp Schmid, Sourab Mangrulkar, Younes Belkada, Pedro Cuenca (Hugging Face), Intro to MoE models.
- [The Ultimate MoE Training Handbook](https://huggingface.co/spaces/huggingface/moe-blogpost), Nouamane Tazi, Leandro von Werra, Thomas Wolf (Hugging Face), Hands-on guide to training MoE models with Megatron-LM. Also: [Who selects (section 3.2)](https://huggingface.co/spaces/huggingface/moe-blogpost#s-3-2-who-selects); [Same page on hf.space](https://huggingface-moe-blogpost.hf.space/).
- [Megatron-LM: Ongoing research training transformer models at scale](https://github.com/NVIDIA/Megatron-LM), NVIDIA, Training framework used in the MoE handbook. Also: [MoE token_dispatcher.py (pinned commit, lines 652-657)](https://github.com/NVIDIA/Megatron-LM/blob/d6316eb45bf1bfbb6f1f848c0b56e55166564d80/megatron/core/transformer/moe/token_dispatcher.py#L652-L657).

## Inference

- [Mastering LLM Techniques: Inference Optimization](https://developer.nvidia.com/blog/mastering-llm-techniques-inference-optimization/), Shashank Verma and Neal Vaidya (NVIDIA), Prefill and decode, KV cache and batching.
- [The Engineering Behind LLM Inference: Inside the GPU](https://www.youtube.com/watch?v=cbEhkd4ZeKs), PY, Inference on the GPU.
- [Inference Engines explained in 10min..](https://www.youtube.com/watch?v=_xM8scs4_x4), Caleb Writes Code, Inference engines overview.
- [Give Me 1 Hour, I'll Make LLM Inference Engines Click Forever](https://www.youtube.com/watch?v=I2QhfZ0aVmk), Zachary Huang, Inference engines walkthrough.
- [How LLMs survive in low precision | Quantization Fundamentals](https://www.youtube.com/watch?v=qoQJq5UwV1c), Julia Turc, Quantization basics.

## GPUs and systems

- [How to Think About GPUs (How To Scale Your Model)](https://jax-ml.github.io/scaling-book/gpus/), Jacob Austin, Swapnil Patil, Adam Paszke, Reiner Pope (Google DeepMind and MatX), GPU chapter of the scaling book.
- [TransformerEngine: A library for accelerating Transformer models on NVIDIA GPUs](https://github.com/NVIDIA/TransformerEngine), NVIDIA, FP8 and Transformer layers on NVIDIA GPUs.
- [Model-Optimizer: examples/gpt-oss](https://github.com/NVIDIA/Model-Optimizer/tree/main/examples/gpt-oss), NVIDIA, Example directory for gpt-oss in NVIDIA Model Optimizer.

## Courses and lecture series

- [CS25: Transformers United V6](https://web.stanford.edu/class/cs25/), Stanford University (instructors listed on the course page), Stanford seminar series on Transformers. Also: [Recordings](https://web.stanford.edu/class/cs25/recordings/).
- [Stanford CS25 - Transformers United](https://www.youtube.com/playlist?list=PLoROMvodv4rNiJRchCzutFw5ItR_Z27CM), Stanford Online, Playlist of CS25 lectures.
- [Stanford CS25: Transformers United V6 I From Representation Learning to World Modeling](https://www.youtube.com/watch?v=GBd7iuJkW08), Stanford Online, CS25 V6 session (title from the watch page).
- [LLM Course (mlabonne/llm-course)](https://github.com/mlabonne/llm-course), Maxime Labonne, Roadmaps and Colab notebooks for LLMs (Apache-2.0 repo).

## Channels

- [mesanu (YouTube channel)](https://www.youtube.com/@mesanu1/videos), mesanu, Channel: "Hard concepts, visualized beautifully and explained step-by-step."
- [hu-po (YouTube channel)](https://www.youtube.com/@hu-po/streams), hu-po, Channel: livestreams on ML papers, coding and research.

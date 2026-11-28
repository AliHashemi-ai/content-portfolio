---
title: "Position bias in LLM-as-a-judge"
date: 2026-11-25
topic: 04-ai-evals
level: intermediate
tags: [llm-as-a-judge, position-bias, evaluation]
source: "Stanford CME295 Transformers & LLMs | Autumn 2025 | Lecture 8 - LLM Evaluation — Afshine Amidi and Shervine Amidi (Stanford Online), https://www.youtube.com/watch?v=8fNP4N46RRo&t=2328s"
slides: ""
---

# Position bias in LLM-as-a-judge

*TL;DR — Ask an LLM judge which of two answers is better, then swap the order and ask again. If the winner changes, the lecture says the judgment may not be reliable, so you should do something else.*

## Context

This note is based on Lecture 8 of Stanford's CME295 (Transformers and Large Language Models, Autumn 2025), taught by Afshine Amidi and Shervine Amidi. The lecture is about LLM evaluation. Position bias is one of three judge biases covered in the lecture, and that chapter starts at 38:48.

The social post draft below is mine. The lecture claims are from the instructors. My two additions are marked as such.

## Post draft

Ask an LLM judge which of two answers is better. Swap the order and ask again. Sometimes the winner changes.

This is position bias. It is one of the three judge biases in Lecture 8 of Stanford's CME295 (LLM evaluation, taught by Afshine Amidi and Shervine Amidi). The lecture's check is simple. Ask "A or B?", then "B or A?", and take the majority or average. If the pick changes, the judgment may not be reliable, so the lecture says to do something else.

Two things I would add to that.

1. Track which answer won, not which slot won. With only two runs there is no majority, so I would keep every flip and look at it by hand. The lecture does not say this, it is my addition.
2. A stable winner can still be wrong. The lecture says to write clear criteria, prefer binary pass/fail, ask for the rationale before the score, and compare the judge with human ratings.

Verbosity bias and self-enhancement bias are separate problems with separate fixes. Swapping the order tests neither.

I made a one minute animation of the swap. The A and B outcomes in it are constructed to show the idea. They are not a measured result from a model.

Lecture (position bias starts at 38:48): https://www.youtube.com/watch?v=8fNP4N46RRo&t=2328s

How do you check that your judge measures what you care about?

## Key insights

### 1. The lecture's swap check
Ask "A or B?", then "B or A?", and take the majority or average. If the pick changes, the judgment may not be reliable, so the lecture says to do something else. Timestamp: [38:48](https://www.youtube.com/watch?v=8fNP4N46RRo&t=2328s).

### 2. Three judge biases, three tests
Position bias, verbosity bias and self-enhancement bias are separate problems with separate fixes. Swapping the order tests only position bias.

### 3. A stable winner can still be wrong
The lecture also says to write clear criteria, prefer binary pass/fail, ask for the rationale before the score, and compare the judge with human ratings.

## My perspective

I would track which answer won, not which slot won. With only two runs there is no majority, so I would keep every flip and look at it by hand. The lecture does not say this. It is my addition.

## Takeaways
- Swap the order when you use a pairwise LLM judge, and look at whether the winner changes.
- Credit the check to Afshine Amidi and Shervine Amidi, CME295 Lecture 8.
- Do not treat a stable winner as proof that the judge is right.
- The animation that accompanies the post is constructed. It is not a measured result from a model.

## Source
Based on "Stanford CME295 Transformers & LLMs | Autumn 2025 | Lecture 8 - LLM Evaluation" by Afshine Amidi and Shervine Amidi, Stanford Online ([link, position bias at 38:48](https://www.youtube.com/watch?v=8fNP4N46RRo&t=2328s)). Also useful: the [2025 syllabus](https://cme295.stanford.edu/syllabus/2025/) and the [Lecture 8 slides](https://cme295.stanford.edu/slides/fall25-cme295-lecture8.pdf).
All summaries and opinions are my own.

## References

- [Stanford CME295 Transformers & LLMs | Autumn 2025 | Lecture 8 - LLM Evaluation](https://www.youtube.com/watch?v=8fNP4N46RRo&t=2328s), Afshine Amidi and Shervine Amidi (Stanford Online)
- [Judging LLM-as-a-Judge with MT-Bench and Chatbot Arena](https://arxiv.org/abs/2306.05685), Lianmin Zheng, Wei-Lin Chiang, Ying Sheng, Siyuan Zhuang, Zhanghao Wu, Yonghao Zhuang, Zi Lin, Zhuohan Li, Dacheng Li, Eric P. Xing, Hao Zhang, Joseph E. Gonzalez, Ion Stoica
- [Building strong safety evaluations](https://www.anthropic.com/research/building-strong-safety-evaluations), Anthropic
- [Scaling FineWeb to 1000+ languages: Step 1: finding signal in 100s of evaluation tasks](https://huggingface.co/spaces/HuggingFaceFW/blogpost-fine-tasks), Hynek Kydlíček, Guilherme Penedo, Clémentine Fourier, Nathan Habib, Thomas Wolf (Hugging Face)
- [Department of Evals (About)](https://departmentofevals.substack.com/about), Department of Evals, the Evals team at Braintrust
- [Give Me 45 Minutes, I'll Make LLM Evaluation Click Forever](https://www.youtube.com/watch?v=5NCmJA8VoAE&t=303s), Zachary Huang
- [Evaluation | Build Your Own LLM Workshop #20](https://www.youtube.com/watch?v=S6uLzsqOOUc), Justin Angel
- [From Vibes to Production: Evaluating and Shipping AI Agents That Work 101 — Laurie Voss, Arize AI](https://www.youtube.com/watch?v=qZj7sqmidqA), AI Engineer (talk by Laurie Voss, Arize AI)

A longer list of talks, papers, courses and tools, including training, data, MoE and systems, is in the [LLM reading list](../../resources/llm-reading-list.md).

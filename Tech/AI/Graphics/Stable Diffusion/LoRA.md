---
feed: show
title: What is LoRA
date: 08-08-2023
---

# What is [LoRA](https://github.com/microsoft/LoRA)

LoRA stands for Low-Rank Adaptation. It allows you to use low-rank adaptation technology to quickly fine-tune diffusion models. To put it in simple terms, the LoRA training model makes it easier to train Stable Diffusion on different concepts, such as characters or a specific style. These trained models then can be exported and used by others in their own generations.

LoRA reduces the number of trainable parameters by learning pairs of rank-decompostion matrices while freezing the original weights. This vastly reduces the storage requirement for large language models adapted to specific tasks and enables efficient task-switching during deployment all without introducing inference latency. LoRA also outperforms several other adaptation methods including adapter, prefix-tuning, and fine-tuning.
# Fine-Tuning-DeepSeek-R1-on-Medical-Reasoning-Dataset-using-LoRA
Fine-tuning DeepSeek R1 on a medical reasoning dataset (FreedomIntelligence/medical-o1-reasoning-SFT) using LoRA for efficient adaptation in Kaggle’s GPU environment. Implements instruction tuning for medical QA.

## 🧠 Introduction

Large language models like DeepSeek R1 exhibit impressive general reasoning capabilities. However, domain-specific performance (e.g., medical QA) often requires fine-tuning. This repository shows how to adapt DeepSeek R1 for medical question answering using **LoRA**, a lightweight method that avoids full model retraining.

We utilize:
- 💾 Dataset: [`FreedomIntelligence/medical-o1-reasoning-SFT`](https://huggingface.co/datasets/FreedomIntelligence/medical-o1-reasoning-SFT)
- 🧠 Model: [`deepseek-ai/deepseek-llm-7b`](https://huggingface.co/deepseek-ai/deepseek-llm-7b)
- 🚀 Fine-tuning Strategy: LoRA via `peft`
- 🧰 Framework: `transformers`, `peft`, `accelerate`
- ☁️ Runtime: Kaggle GPU (T4 / A100)

We apply LoRA to fine-tune only a small set of additional parameters (usually in attention layers), dramatically reducing GPU memory usage and training time.

you can use this template notebook to finetune any model outthere

Training 
-  [LLM Training](https://blog.replit.com/llm-training)
-  [Building LLM applications for production - Chip Huyen](https://huyenchip.com/2023/04/11/llm-engineering.html)           
-  [Build, customize and control your own personal LLMs - stochatic AI](https://github.com/stochasticai/xturing)
-  [lit-llama, Independent implementation of LLaMA pretraining, finetuning, and inference code](https://github.com/Lightning-AI/lit-llama)
-  [A Recipe for Training Large Models](https://wandb.ai/craiyon/report/reports/A-Recipe-for-Training-Large-Models--VmlldzozNjc4MzQz)
   - Sharding
   - Gradient checkpointing
-  [Deep Learning Tuning Playbook](https://github.com/google-research/tuning_playbook)
-  [Training Working Group](https://mlcommons.org/en/groups/training/)  <b>*Try this when time permits</b>
-  
Fine Tuning
-  [Fine tuning LLMs](https://magazine.sebastianraschka.com/p/finetuning-large-language-models)
- Finetuning pre-trained large language models (LLMs) is an effective method to tailor these models to suit specific business requirements and align them with target domain data.
    - This process involves adjusting the model parameters using a smaller dataset relevant to the desired domain, which enables the model to learn domain-specific knowledge and vocabulary.
- However, as LLMs are “large,” updating multiple layers in a transformer model can be very expensive, so researchers started developing parameter-efficient alternatives.
  1. [Parameter-Efficient Finetuning - PEFT](https://github.com/harirajeev/learn_LLMS/blob/main/PEFT.md)           
  2. [Mixed Precision & Quantization](https://github.com/harirajeev/learn_LLMS/blob/main/MixedPrecision&Quantization.md)
  3. [Example Models](https://github.com/harirajeev/learn_LLMS/blob/main/ExampleModels.md)
- [Simple LLM Finetuner Utility](https://github.com/lxe/simple-llm-finetuner)
- [A Hacker's Guide to LLM Optimization](https://matt-rickard.com/a-hackers-guide-to-llm-optimization)
- [Techniques for optimizing LLM performance - Prompt Eng](https://www.mlexpert.io/prompt-engineering/llm-optimization)
- [Strategies for optimizing infrastructure costs of large NLP models](https://neptune.ai/blog/nlp-models-infrastructure-cost-optimization)
- [Scaling](https://github.com/harirajeev/learn_LLMS/blob/main/Scaling.md)
  - memory optimization methods
      - Mixture-of-experts - The fundamental concept behind the Mixture-of-Experts method (MoE, Shazeer et al. 2017) is ensemble learning. To go into more detail, the MoE layer consists of a set of n  feed-forward expert networks E1,E2,…,En  (which can be distributed across GPUs) and the gating network G  whose output is a sparse n-dimensional vector.
      - Activation checkpointing - Suppose we partition a neural network into k partitions. In Activation Checkpointing (Chen et al. 2016), only the activations at the boundaries of each partition are saved and shared between workers during training. The intermediate activations of the neural network are recomputed on-the-fly during the backward pass of the training process rather than storing them in memory during the forward pass.
      - Mixed Precision Training - The concept of Mixed Precision Training (Narang & Micikevicius et al. 2018) bridges the gap between reducing memory usage during training and maintaining good accuracy.
Mixed Precision Training involves utilizing FP16 to store weights, activations, and gradients. However, to maintain accuracy similar to that of FP32 networks, an FP32 version of the weights (the master weights) is also kept and modified using the weight gradient during the optimizer step. In each iteration, a copy of the master weights in FP16 is utilized in both the forward and backward passes, which reduces storage and bandwidth requirements by half compared to FP32 training.
     ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/ff18abe9-9ecd-4b57-afdb-7689a8b54aa4)
      - Zero Redundancy Optimizer - Optimizers use a lot of memory. For example, while using the Adam optimizer, we need to save four times the memory of model weights, as it stores momentums and variances which are as big as the gradients and model parameters (Weng 2021). All parallelism techniques described in the previous sections store all the model parameters required for the entire training process, even though not all model states are needed during training. To address these drawbacks of training parallelism while retaining the benefits, Microsoft researchers developed a new memory optimization approach called Zero Redundancy Optimizer (ZeRO, Rajbhandari et al. 2019).
ZeRO aims to train very large models efficiently by eliminating redundant memory usage, resulting in better training speed. It eliminates memory redundancies in Data Parallel processes by dividing the model states across the devices instead of duplicating them.
      - Flash Attention -    Making Transformers understand longer inputs is difficult because their multi-head attention layer needs a substantial amount of memory and time to process the input, and this requirement grows quadratically with the length of the sequence. When training Transformers on long sequences with parallelism techniques described in previous sections, the batch size can become extremely small. This is the scenario which the FlashAttention method (Dao et al. 2022) improves. To optimize for long sequences for each attention head, FlashAttention splits the input Q,K,V  into blocks and loads these blocks from GPU HBM (which is the main memory) into SRAM (which is its fast cache). Then, it computes attention with respect to that block and writes back the output to HBM.

- BLOOM-176B
   - to fine-tune BLOOM-176B, one would require almost 3 TB of GPU memory (approximately 72 80GB A100 GPUs).
   - In addition to the model weights, the cost of storing intermediate computation outputs (optimizer states and gradients) is typically even higher
  
[Inference](https://github.com/harirajeev/learn_LLMS/blob/main/Inference.md)
  - Why is it hard to run inference for large language models ? There are 2 main factors contributing to the inference challenge
    1. Large Memoryfoot print
      - Both model parameters and intermediate states are needed in memory at inference time.
        - The KV cache should be stored in memory during decoding time. Eg: for a batch size of 512 and context length of 2048. The KV cache totals 3TB, that is 3X the model size
        - Inference cost from the attention mechanism scales quadratically with input sequence length
    2. Low parallelizability. Inference generation is executed in an autoregressive fashion, making the decoding process hard to parallel.

[Context Length & In Context Learning](https://github.com/harirajeev/learn_LLMS/blob/main/ContextLength&InContextLearning.md)

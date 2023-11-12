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
-  [Alignment - Align LLM with human preferences](https://github.com/huggingface/alignment-handbook)
   -   𝗦𝘂𝗽𝗲𝗿𝘃𝗶𝘀𝗲𝗱 𝗳𝗶𝗻𝗲-𝘁𝘂𝗻𝗶𝗻𝗴 (𝗦𝗙𝗧) - teach models to follow instructions
   -   𝗗𝗶𝗿𝗲𝗰𝘁 𝗽𝗿𝗲𝗳𝗲𝗿𝗲𝗻𝗰𝗲 𝗼𝗽𝘁𝗶𝗺𝗶𝘇𝗮𝘁𝗶𝗼𝗻 (𝗗𝗣𝗢) - an alternative to RLHF to better align LLMs
       - DPO is a promising technique that allows us to incorporate human feedback directly into the training process to steer models toward helpfulness and safety.
       - This stands in contrast to supervised fine-tuning, which relies solely on static datasets.   
- <b>Optimization techniques</b>
   -   [NEFTune: Noisy Embeddings Improve Instruction Finetuning](https://arxiv.org/pdf/2310.05914.pdf)
       -   NEFTune is a simple trick that can improve the finetuning process for language models with only a few lines of code.
       -   NEFTune just adds random (uniform) noise to an LLM’s input word embeddings
       -   To generate the random noise , we can independently sample values in the range [-1, 1], then scale these values according to the sequence length L, embedding dimension d, and two tunable parameters—α and ɛ.
       -   This approach is already implemented in TRL, so it can be used by simply setting a parameter in the SFTTrainer package.
- <b> Embeddings </b>
       -    [Utilizing Transformer Representations Efficiently](https://www.kaggle.com/code/rhtsingh/utilizing-transformer-representations-efficiently)
- However, as LLMs are “large,” updating multiple layers in a transformer model can be very expensive, so researchers started developing parameter-efficient alternatives.
  1. [Parameter-Efficient Finetuning - PEFT](https://github.com/harirajeev/learn_LLMS/blob/main/PEFT.md)           
  2. [Mixed Precision & Quantization](https://github.com/harirajeev/learn_LLMS/blob/main/MixedPrecision&Quantization.md)
  3. [Example Models](https://github.com/harirajeev/learn_LLMS/blob/main/ExampleModels.md)
- [Scaling](https://github.com/harirajeev/learn_LLMS/blob/main/Scaling.md)
- [Memory Optimization Methods](https://github.com/harirajeev/learn_LLMS/blob/main/MemoryOptimizationMethods.md)
- Good Reads
  - [Simple LLM Finetuner Utility](https://github.com/lxe/simple-llm-finetuner)
  - [A Hacker's Guide to LLM Optimization](https://matt-rickard.com/a-hackers-guide-to-llm-optimization)
  - [Techniques for optimizing LLM performance - Prompt Eng](https://www.mlexpert.io/prompt-engineering/llm-optimization)
  - [Strategies for optimizing infrastructure costs of large NLP models](https://neptune.ai/blog/nlp-models-infrastructure-cost-optimization)
- BLOOM-176B
   - to fine-tune BLOOM-176B, one would require almost 3 TB of GPU memory (approximately 72 80GB A100 GPUs).
   - In addition to the model weights, the cost of storing intermediate computation outputs (optimizer states and gradients) is typically even higher
- [LLaMa](https://github.com/harirajeev/learn_LLMS/blob/main/Llama.md)
- [Other Open Source LLMs](https://github.com/harirajeev/learn_LLMS/blob/main/OpenSourceLLM.md)
- More data is not always better when finetuning LLMs
   -  LIMA
   -  AlpaGasus
      - Trimming 52k instruction-response pairs in the popular Aplaca dataset to 9k can improve the performance when finetuning 7B and 13B parameters LLMs
      - [AlpaGasus: Training A Better Alpaca with Fewer Data](https://arxiv.org/abs/2307.08701)
- [Context Length & In Context Learning](https://github.com/harirajeev/learn_LLMS/blob/main/ContextLength&InContextLearning.md)

[Inference](https://github.com/harirajeev/learn_LLMS/blob/main/Inference.md)
  - Why is it hard to run inference for large language models ? There are 2 main factors contributing to the inference challenge
    1. Large Memoryfoot print
      - Both model parameters and intermediate states are needed in memory at inference time.
        - The KV cache should be stored in memory during decoding time. Eg: for a batch size of 512 and context length of 2048. The KV cache totals 3TB, that is 3X the model size
        - Inference cost from the attention mechanism scales quadratically with input sequence length
    2. Low parallelizability. Inference generation is executed in an autoregressive fashion, making the decoding process hard to parallel.
  - [vLLM Easy, fast, and cheap LLM serving for everyone](https://vllm.readthedocs.io/en/latest/)
  - [Frameworks for Serving LLMs](https://slgero.medium.com/frameworks-for-serving-llms-60b7f7b23407)
  - [llama2.c by Karpathy](https://github.com/karpathy/llama2.c#llama2c)

    
   <b>LLM Inference optimization techniques</b>
   ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/8abda650-a576-4a44-aa60-cd523dd5d4e7)


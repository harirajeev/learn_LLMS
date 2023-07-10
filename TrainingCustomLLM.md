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
- [How to train a large language model using limited hardware?](https://deepsense.ai/how-to-train-a-large-language-model-using-limited-hardware/)
   - Data Parallelism -  In data parallelism (DP), the entire dataset is divided into smaller subsets, and each subset is processed simultaneously on separate processing units.![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/3c8616e0-eb0b-4e0c-b5fb-cd39eef03ded)

   - Pipeline Parallelism - Since deep neural networks typically have multiple layers stacked on top of each other, the naive approach to model parallelism involves dividing a large model into smaller parts, with a few consecutive layers grouped together and assigned to a separate device, with the output of one stage serving as the input to the next stage.![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/fe57c1fb-06b8-4072-b8ff-9ecd93f8e9bd)

   - Tensor Parallelism - In tensor parallelism, specific model weights, gradients and optimizer states are split across devices and each device is responsible for processing a different portion of the parameters.In contrast to pipeline parallelism, which splits the model layer by layer, tensor parallelism splits individual weights. ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/cb2ac36b-082a-4b8c-bcee-8d7ab1bba35a)

- BLOOM-176B
   - to fine-tune BLOOM-176B, one would require almost 3 TB of GPU memory (approximately 72 80GB A100 GPUs).
   - In addition to the model weights, the cost of storing intermediate computation outputs (optimizer states and gradients) is typically even higher
  
Inference
- [How to Run LLMs Locally - GGML - CCP](https://wandb.ai/capecape/LLMs/reports/How-to-Run-LLMs-Locally--Vmlldzo0Njg5NzMx)
- [Large Transformer Model Inference Optimization - Lilian Weng](https://lilianweng.github.io/posts/2023-01-10-inference-optimization/)


[Context Length & In Context Learning](https://github.com/harirajeev/learn_LLMS/blob/main/ContextLength&InContextLearning.md)

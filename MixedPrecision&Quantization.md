# Mixed Precission Training
- [Accelerating Large Language Models with Mixed-Precision Techniques](https://lightning.ai/pages/community/tutorial/accelerating-large-language-models-with-mixed-precision-techniques/)  
 ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/41f0694a-5178-4a64-9123-9c932d9ee6a2)
 
# Quantization
If we want to increase the model performance during inference even more, we can also move beyond lower floating point precision and use quantization. Quantization converts the model weights from floats to low-bit integer representations, for example, 8-bit integers (and, recently, even 4-bit integers).

Quantization is a model size reduction technique that converts model weights from high-precision floating-point representation to low-precision floating-point (FP) or integer (INT) representations, such as 16-bit or 8-bit

  - [GPTQ: Accurate Post-Training Quantization for Generative Pre-trained Transformers 22/3/2023](https://arxiv.org/pdf/2210.17323.pdf)
    - GPT3-175B, have in the order of 175 billion parameters and require tens-to-hundreds of GPU years to train
the parameters of GPT3-175B occupy 326GB (counting in multiples of 1024) of memory when stored in a compact float16 format
    - More complex methods for low-bitwidth quantization or model pruning usually require model retraining, which is extremely expensive for billion-parameter models
    - Compress the model in one shot, without retraining, would be very appealing
    - We present a new post-training quantization method, called GPTQ, which is efficient enough to execute on models with hundreds of billions of parameters in at most a few hours, and precise enough to compress such models to 3 or 4 bits per parameter without significant loss of accuracy
    - GPTQ can quantize the largest publicly-available models, OPT-175B and BLOOM-176B, in approximately four GPU hours, with minimal increase in
perplexity, known to be a very stringent accuracy metric  
  - [QLORA: Efficient Finetuning of Quantized LLMs 23/5/2023](https://arxiv.org/pdf/2305.14314.pdf)
    - QLORA, an efficient finetuning approach that reduces memory usage enough to finetune a 65B parameter model on a single 48GB GPU while preserving full 16-bit finetuning task performance.
    - QLORA backpropagates gradients through a frozen, 4-bit quantized pretrained language model into Low Rank Adapters (LoRA).
    - QLORA introduces a number of innovations to save memory without sacrificing performance: (a) 4-bit NormalFloat (NF4), a new data type that is information theoretically optimal for normally distributed weights (b) Double Quantization to reduce the average memory footprint by quantizing the quantization constants, and (c) Paged Optimizers to manage memory spikes.
    - Our best model family, which we name Guanaco, outperforms all previous openly released models on the Vicuna benchmark, reaching 99.3% 
of the performance level of ChatGPT while only requiring 24 hours of finetuning on a single GPU
  - [A Gentle Introduction to 8-bit Matrix Multiplication for transformers at scale using Hugging Face Transformers, Accelerate and bitsandbytes](https://huggingface.co/blog/hf-bitsandbytes-integration)
    - Int8 (LLM.int8()) inference that does not degrade predictive performance of large models and reduces the memory footprint of large models by a factor or 2x
  
 
    

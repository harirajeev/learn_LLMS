Inference
- [How to Run LLMs Locally - GGML - CCP](https://wandb.ai/capecape/LLMs/reports/How-to-Run-LLMs-Locally--Vmlldzo0Njg5NzMx)
- [Large Transformer Model Inference Optimization - Lilian Weng](https://lilianweng.github.io/posts/2023-01-10-inference-optimization/)
  - Why is it hard to run inference for large language models ? There are 2 main factors contributing to the inference challenge
    1. Large Memoryfoot print
      - Both model parameters and intermediate states are needed in memory at inference time.
        - The KV cache should be stored in memory during decoding time. Eg: for a batch size of 512 and context length of 2048. The KV cache totals 3TB, that is 3X the model size
        - Inference cost from the attention mechanism scales quadratically with input sequence length
    2. Low parallelizability. Inference generation is executed in an autoregressive fashion, making the decoding process hard to parallel.
- [Incredibly Fast BLOOM Inference with DeepSpeed and Accelerate](https://huggingface.co/blog/bloom-inference-pytorch-scripts#huggingface-accelerate)
  - how to get an incredibly fast per token throughput when generating with the 176B parameter BLOOM model.
  - As the model needs 352GB in bf16 (bfloat16) weights (176*2), the most efficient set-up is 8x80GB A100 GPUs. Also 2x8x40GB A100s or 2x8x48GB A6000 can be used.
  - Benchmarks 
    1. how long did it take to load and prepare the model
       The loading time may or may not be of importance, since once loaded you can continually generate tokens again and again without an additional loading overhead
       - Deepspeed-Inference
       - accelerate

    2. Next the most important benchmark of token generation throughput
       The throughput metric here is a simple - how long did it take to generate 100 new tokens divided by 100 and the batch size (i.e. divided by the total number of generated tokens).
       -  Deepspeed-Inference's Tensor Parallelism (TP)
       -  Accelerate is super fast as well. It uses a very simple approach of naive Pipeline Parallelism (PP)
       - Deepspeed-ZeRO
  

- [PyTorch Lightning vs DeepSpeed vs FSDP vs FFCV vs …](https://towardsdatascience.com/pytorch-lightning-vs-deepspeed-vs-fsdp-vs-ffcv-vs-e0d6b2a95719)

- [DeepSpeed: Extreme-scale model training for everyone](https://www.microsoft.com/en-us/research/blog/deepspeed-extreme-scale-model-training-for-everyone/)
    - DeepSpeed is a technique created by Microsoft to train massive billion-parameter models at scale.
    - The crux of how DeepSpeed enables scale is through the introduction of the Zero Redundancy Optimizer (ZERO).
    - ZERO is a memory optimization method
    - two major memory consumption of large model training:
      1. The majority is occupied by model states,
         - including optimizer states (e.g. Adam momentums and variances), gradients and parameters.
         - Mixed-precision training demands a lot of memory since the optimizer needs to keep a copy of FP32 parameters and other optimizer states, besides the FP16 version.
      3. The remaining is consumed by
         - activations,
         - temporary buffers and
         - unusable fragmented memory (named residual states in the paper).
    - ZERO has 3 stages:
      1. Optimizer states are partitioned across processes.
      2. Gradients are partitioned across processes.
      3. Model parameters are partitioned across the processes.
    - Optimizers use a lot of memory.
      - For example, while using the Adam optimizer,
      - we need to save four times the memory of model weights,
      - as it stores momentums and variances which are as big as the gradients and model parameters
    - Parallelism Paradigms discussed earlier stores all the model parameters, tho not everything is required for training
    - ZERO aims to eliminate redundant memory usage resulting in better training speed.
    - It eliminates memory redundancies in Data Parallel processes
    - Three optimization stages of ZeRO compared with the data parallelism
     ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/f3351b56-d892-49fa-8970-d98a62b2b985)
    - memory reduction is directly proportional to the degree of data parallelism.
    - For instance, partitioning across 8 GPUs will lead to an 8-fold reduction in memory usage.
    - ZeRO combines two approaches, ZeRO-DP and ZeRO-R.
      - ZeRO-DP is an enhanced data parallelism to avoid simple redundancy over model states. It partitions optimizer state, gradients and parameters across multiple data parallel processes via a dynamic communication schedule to minimize the communication volume.
      - ZeRO-R optimizes the memory consumption of residual states, using partitioned activation recomputation, constant buffer size and on-the-fly memory defragmentation.
      
- [Different parallelism paradigms](https://github.com/harirajeev/learn_LLMS/blob/main/ParallelismParadigms.md)
  
- Fully-sharded data-parallel (FSDP)
  - FSDP is Meta’s version of sharding, inspired by DeepSpeed (stage 3) optimized for PyTorch compatibility
  - FSDP is a type of data-parallel training which, unlike traditional data-parallel processing,
    - shards the model’s parameters,
    - gradients and
    - optimizer states across data-parallel workers and
    - can optionally offload the sharded model parameters to the CPUs

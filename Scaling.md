![blah](https://github.com/harirajeev/learn_LLMS/blob/main/deepspeed.gif)

- Scaling
  ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/bf66a7f9-f1c8-4ac1-8c9d-b6f87199de18)
  - [DeepSpeed: Extreme-scale model training for everyone](https://www.microsoft.com/en-us/research/blog/deepspeed-extreme-scale-model-training-for-everyone/)
    - DeepSpeed enables scale is through the introduction of the Zero Redundancy Optimizer (ZERO)
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

  - [PyTorch Lightning vs DeepSpeed vs FSDP vs FFCV vs …](https://towardsdatascience.com/pytorch-lightning-vs-deepspeed-vs-fsdp-vs-ffcv-vs-e0d6b2a95719)
- [How to train a large language model using limited hardware?](https://deepsense.ai/how-to-train-a-large-language-model-using-limited-hardware/)
  - Different parallelism paradigms
      - Data Parallelism -  In data parallelism (DP), the entire dataset is divided into smaller subsets, and each subset is processed simultaneously on separate processing units.![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/dbdd89fd-fd6b-4d7b-8819-28f8f1095dd7)

      - Pipeline Parallelism - Since deep neural networks typically have multiple layers stacked on top of each other, the naive approach to model parallelism involves dividing a large model into smaller parts, with a few consecutive layers grouped together and assigned to a separate device, with the output of one stage serving as the input to the next stage.![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/fe57c1fb-06b8-4072-b8ff-9ecd93f8e9bd)

      - Tensor Parallelism - In tensor parallelism, specific model weights, gradients and optimizer states are split across devices and each device is responsible for processing a different portion of the parameters.In contrast to pipeline parallelism, which splits the model layer by layer, tensor parallelism splits individual weights. ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/cb2ac36b-082a-4b8c-bcee-8d7ab1bba35a)
      - Sequence Parallelism - Another method to parallelize computation across multiple devices is Sequence Parallelism (Li et al. 2021), a technique for training Transformer models on very long sequences by breaking them up into smaller chunks and processing each chunk in parallel across multiple GPUs.
![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/0ef8836f-b0ae-4ec1-a5b6-2940bf1a7e06)

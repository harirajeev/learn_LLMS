
 - Different parallelism paradigms
      - Data Parallelism -  In data parallelism (DP), the entire dataset is divided into smaller subsets, and each subset is processed simultaneously on separate processing units.![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/dbdd89fd-fd6b-4d7b-8819-28f8f1095dd7)

      - Pipeline Parallelism - Since deep neural networks typically have multiple layers stacked on top of each other, the naive approach to model parallelism involves dividing a large model into smaller parts, with a few consecutive layers grouped together and assigned to a separate device, with the output of one stage serving as the input to the next stage.![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/fe57c1fb-06b8-4072-b8ff-9ecd93f8e9bd)

      - Tensor Parallelism - In tensor parallelism, specific model weights, gradients and optimizer states are split across devices and each device is responsible for processing a different portion of the parameters.In contrast to pipeline parallelism, which splits the model layer by layer, tensor parallelism splits individual weights. ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/cb2ac36b-082a-4b8c-bcee-8d7ab1bba35a)
      - Sequence Parallelism - Another method to parallelize computation across multiple devices is Sequence Parallelism (Li et al. 2021), a technique for training Transformer models on very long sequences by breaking them up into smaller chunks and processing each chunk in parallel across multiple GPUs.
![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/0ef8836f-b0ae-4ec1-a5b6-2940bf1a7e06)

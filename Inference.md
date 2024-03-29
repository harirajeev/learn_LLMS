<b>Inference</b>

<b>Optimizing the model for serving</b>
  - size of LLMs can pose a problem for deployment.
  - When your model is too large, strategies like
    -  model compilation,
    -  model compression, and
    -  model sharding can be used.
  - These techniques reduce the size of the model while preserving accuracy, which allows easier deployment and reduce the associated expenses significantly. 

![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/9e179b1f-8c56-4f29-94cd-1aa83d0be153)

<b>Model compression</b>
  -  Model compression is a technique used to optimize and transform an LLM into an efficient executable model that can be run on specialized hardware or software platforms
  -  The goal of model compression is to improve the performance and efficiency of LLM inference by leveraging hardware-specific optimizations, such as
     - reduced memory footprint,
     - improved computation parallelism, and
     - reduced latency.
  -  model compression involves several steps     
     - Graph optimization: The high-level LLM graph is transformed and optimized using graph optimization techniques such as <b>pruning</b> and <b>quantization</b> to reduce the computational complexity and memory footprint of the model. This, in turn, makes the model small while preserving its accuracy. 
     - Hardware-specific optimization: The optimized LLM graph is further optimized to leverage hardware-specific optimizations. For instance, Amazon Sagemaker provides model serving containers for various popular ML frameworks, including XGBoost, scikit-learn, PyTorch, TensorFlow, and Apache MXNet, along with software development kits (SDKs) for each container.     
  -  <b>model compression techniques</b>
     -  to reduce the memory footprint and computation requirements of an LLM
     -  MQ essentially transforms the model parameters and activations with lower-precision data types.
     -  The goal of model quantization is to improve the efficiency of LLM during inference by reducing the memory bandwidth requirements
     -  exploiting hardware-specific optimizations optimized for lower-precision arithmetic.
     -  reduction of model parameters by a factor of 4
     -  while the memory bandwidth required by the model by the factor 2 to 4 times
     -  As a result of these improvements, the inference speed can increase by 2 to 4 times, owing to the reduction in memory bandwidth requirements and faster computations using int8 arithmetic
     -  trade-offs between reduced precision and model accuracy, as well as the hardware-specific optimizations that can be leveraged with lower-precision arithmetic
     -  There are several approaches to model quantization for LLMs, including:
         -     Post-training quantization:
               -   In this approach, the LLM is first trained using floating-point data types, and then the weights and activations are quantized to lower-precision data types post-training. This approach is simple to implement and can achieve good accuracy with a careful selection of quantization parameters.
         -     Quantization-aware training:
               -   Here, the LLM is quantized during training, allowing the model to adapt to the reduced precision during training. This approach can achieve higher accuracy than post-training quantization but requires more computation during training.
         -     Hybrid quantization:
               -   It combines both post-training quantization and quantization-aware training, allowing the LLM to adapt to lower-precision data types during training while also applying post-training quantization to further reduce the memory footprint and computational complexity of the model.

  -  <b>[Model Pruning](https://colab.research.google.com/github/pytorch/tutorials/blob/gh-pages/_downloads/7126bf7beed4c4c3a05bcc2dac8baa3c/pruning_tutorial.ipynb)</b>
     -  Model pruning (MP) is again a technique used to reduce the size and computational complexity of an LLM by removing redundant or unnecessary model parameters. MP is to improve the efficiency of LLM inference without sacrificing accuracy.
     -  MP involves identifying and removing redundant or unnecessary model parameters using various pruning algorithms.
        -  Weight pruning: In weight pruning, individual weights in the LLM are removed based on their magnitude or importance, using techniques such as magnitude-based pruning or structured pruning. Weight pruning can significantly reduce the number of model parameters and the computational complexity of the LLM, but it may require fine-tuning of the pruned model to maintain its accuracy.
        -  Neuron pruning: In neuron pruning, entire neurons or activations in the LLM are removed based on their importance, using techniques such as channel pruning or neuron-level pruning. Neuron pruning can also significantly reduce the number of model parameters and the computational complexity of the LLM, but it may be more difficult to implement and may require more extensive retraining and maybe fine-tuning to maintain accuracy.
        -  Here are a couple of approaches to model pruning:
           -    Post-training pruning: In this approach, the LLM is first trained using standard techniques and then pruned using one of the pruning algorithms. The pruned LLM is then fine-tuned to preserve its accuracy.
           -    Iterative pruning: Here, the model is trained using standard training techniques and then pruned iteratively over several rounds of training and pruning. This approach can achieve higher levels of pruning while preserving accuracy.

  - <b>Model distillation</b>
     -  (MD) is a technique used to transfer knowledge from an LLM called a teacher to a smaller, more efficient model called the student.
     -  It is used in the context of model compression.
     -  In a nutshell, the teacher model provides guidance and feedback to the student model during training. See the image below.
       ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/23767b06-a4ee-4c07-80b8-01f8ab8bdbda)
     -  There are several approaches to model distillation for LLMs, including:
        -  Knowledge distillation: In this approach, the smaller model is trained to mimic the output probabilities of the larger LLM using a temperature scaling factor. The temperature scaling factor is used to soften the output probabilities of the teacher model, allowing the smaller model to learn from the teacher model’s behavior more effectively. 
        -  Self-distillation: In this approach, the larger LLM is used to generate training examples for the smaller model by applying the teacher model to unlabeled data. The smaller model is then trained on these generated examples, allowing it to learn from the behavior of the larger LLM without requiring labeled data.
        -  Ensemble distillation: In this approach, multiple smaller models are trained to mimic the behavior of different sub-components of the larger LLM. The outputs of these smaller models are combined to form an ensemble model that approximates the behavior of the larger LLM.



        
- [FlashAttention-2: Faster Attention with Better Parallelism and Work Partitioning](https://crfm.stanford.edu/2023/07/17/flash2.html)
- [Optimizing LLM latency - An exploration of inference tools for open source LLMs focused on latency.](https://hamel.dev/notes/llm/03_inference.html) 
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
  

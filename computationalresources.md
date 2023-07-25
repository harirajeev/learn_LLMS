<b>Deploying Large NLP models:</b>
  -   Set a budget
  -   Calculate the size of the model 
  -   Compute the FLOPs required for model
  -   Find the right GPU
  -   Choose the appropriate inference option 
  -   Research the pricing offered by various cloud computing platforms
  -   Find the service that suits your needs and budget
  -   Deploy it. 

[<b>you must know these three things:</b>](https://neptune.ai/blog/nlp-models-infrastructure-cost-optimization)

  - The model size.
  - Details about the hardware to be used.
  - Right inference option.

Once you have the details, you can actually calculate how much-accelerated computing power you need. Based upon that, you can plan and execute your model deployment. 

<b>Calculating model size</b>

 - [Estimating training compute of Deep Learning models](https://www.lesswrong.com/posts/HvqQm6o8KnwxbdmhZ/estimating-training-compute-of-deep-learning-models)
 - [Full doc](https://docs.google.com/document/d/1J2BX9jkE5nN5EA1zYRN0lHhdCf1YkiFERc_nwiYqCOA/edit)
 - [How to measure FLOP/s for Neural Networks empirically?](https://www.lesswrong.com/posts/jJApGWG95495pYM7C/how-to-measure-flop-s-for-neural-networks-empirically)
 - [ a public spreadsheet with some info on different hardware](https://docs.google.com/spreadsheets/d/1AAIebjNsnJj_uKALHbXNfn3_YsT6sHXtCU0q7OIPuc4/edit#gid=0)
 - [Deep Learning GPU Benchmarks](https://lambdalabs.com/gpu-benchmarks)
 - [Training Compute-Optimal Large Language Models - Mar 2022](https://arxiv.org/pdf/2203.15556.pdf)

You can see the table below, which will give you an idea of how many FLOPs you might need for your model. Once you have an estimation, you can then go ahead and find the relevant GPU in your preferred cloud platform. 

![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/67ea79a6-2409-43fb-8f54-a10599038d01)

- [Comparing custom ML hardware - MLPerf Benchmarks ](https://mlcommons.org/en/training-normal-11/)
- [MLPerf benchmark paper](https://arxiv.org/pdf/1910.01500.pdf)

<b>Selecting the right hardware</b>

  -  Once you have calculated the required FLOPs, you can go ahead and choose the GPU. Make sure you are aware of the features that the GPU offers. For instance, see the image below to get an understanding.
   ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/39bcebea-1788-49ee-bba8-3fe0f0423ffc)

<b>Choosing the right inference option</b>

Once you have calculated the model size and selected the GPU, you can then proceed to choose the inference option. Amazon SageMaker offers multiple inference options to suit different workloads. For instance, if you require:

  -   Real-time inference, which is suitable for low-latency or high-throughput online inferences and supports payload sizes up to 6 MB and processing times of 60 seconds.
  -   Serverless inference, which is ideal for intermittent or unpredictable traffic patterns and supports payload sizes up to 4 MB and processing times of 60 seconds. In serverless inference, the model scales automatically based on the incoming traffic or requests. At times when the model is sitting idle you won’t be charged. It offers a pay-as-you-use facility. 
  -  Batch transform is suitable for offline processing of large datasets and supports payload sizes of GBs and processing times of days. 
  -  Asynchronous inference is suitable for queuing requests with large payloads and long processing times, supports payloads up to 1 GB and processing times up to one hour, and can scale down to 0 when there are no requests.

  ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/8e134876-7e9b-442c-9115-61b467a34974)

<b>Optimizing the model for serving</b>

  -   When your model is too large, strategies like model compilation, model compression, and model sharding can be used.
  -   These techniques reduce the size of the model while preserving accuracy, which allows easier deployment and reduce the associated expenses significantly. 

Let’s explore each of those in detail. 

![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/89ee3b92-37a3-4a3c-8c16-0c8dc050005f)



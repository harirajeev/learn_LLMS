[The architecture nomenclature for LLMs is somewhat confusing and unfortunate.](https://www.linkedin.com/posts/yann-lecun_a-survey-of-llms-with-a-practical-guide-and-activity-7057527966540386304-M4_2?utm_source=share&utm_medium=member_desktop)
- What's called "encoder only" actually has an encoder and a decoder (just not an auto-regressive decoder).
- What's called "encoder-decoder" really means "encoder with auto-regressive decoder"
- What's called "decoder only" really means "auto-regressive encoder-decoder"
- autoregressive decoder-style (aka GPT-like)

1.  [Learn LLM](https://github.com/harirajeev/learn_LLMS/blob/main/Learn%20LLM.md)
    1. [Transformers from Scratch](https://e2eml.school/transformers.html#resources)
    2. [GPT-2 (Radford, Ilya Sutskever et al. OPENAI)](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)
    3. [GPT-3 (Brown et al. OPENAI)](https://arxiv.org/pdf/2005.14165.pdf)
    4. [Compare LLM Models](https://lightning.ai/pages/community/community-discussions/the-ultimate-battle-of-language-models-lit-llama-vs-gpt3.5-vs-bloom-vs/)
    5. Context Length
       1. [Scaling Transformer to 1M tokens and beyond with RMT](https://arxiv.org/pdf/2304.11062.pdf) 
2.  [Building LLM applications for production - Chip Huyen](https://huyenchip.com/2023/04/11/llm-engineering.html)
3.  [Training own LLM](https://blog.replit.com/llm-training)
4.  [Fine tuning LLMs](https://magazine.sebastianraschka.com/p/finetuning-large-language-models)
    1. [Parameter-Efficient Finetuning - PEFT]
        Over the years, researchers developed several techniques (Lialin et al.) to finetune LLM with high modeling performance while only requiring the training of only a small number of parameters. These methods are usually referred to as parameter-efficient finetuning techniques (PEFT).
        Some of the most widely used PEFT techniques are summarized in the figure below.
        ![image](https://user-images.githubusercontent.com/13446418/234774400-d31d4c2d-7000-45ed-a384-103f00dd11a6.png)

    2. [Scaling Down to Scale Up: A Guide to Parameter-Efficient Fine-Tuning](https://arxiv.org/pdf/2303.15647.pdf)    
    3. [Understanding Parameter-Efficient Finetuning of Large Language Models: From Prefix Tuning to LLaMA-Adapters](https://lightning.ai/pages/community/article/understanding-llama-adapters/)
        1. [Prompt Tuning And Prefix Tuning](https://magazine.sebastianraschka.com/p/understanding-parameter-efficient)
    4. [Parameter-Efficient LLM Finetuning With Low-Rank Adaptation (LoRA)](https://lightning.ai/pages/community/tutorial/lora-llm/)
5.  Prompt Engineering
    1. [Prompt Engineering - lilianweng](https://lilianweng.github.io/posts/2023-03-15-prompt-engineering/)
    2. [Techniques to impprove PE - openai](https://github.com/openai/openai-cookbook/blob/main/techniques_to_improve_reliability.md#how-to-improve-reliability-on-complex-tasks)
    3. [Prompt Engineering Guide](https://www.promptingguide.ai/introduction)
    4. [Latest papers on prompt engineering](https://www.promptingguide.ai/papers)
    5. [Chain-of-Thought Prompting Elicits Reasoning in Large Language Models](https://arxiv.org/abs/2201.11903)
    6. [self-consistency technique](https://arxiv.org/abs/2203.11171)
    7. [Prompt tuning -The Power of Scale for Parameter-Efficient Prompt Tuning](https://arxiv.org/abs/2104.08691)
    8. [Large Language Models Are Human-Level Prompt Engineers](https://arxiv.org/abs/2211.01910)
6.  Vector DB
    1. [tutorial on how to talk to your vector database.- ChatGPT Retrieval Plugin](https://github.com/openai/chatgpt-retrieval-plugin)
7.  Langchain
    1. [Building LLM Powered Applications - Gregory Kamradt](https://www.youtube.com/playlist?list=PLqZXAkvF1bPNQER9mLmDbntNfSpzdDIU5)
8.  Blogs
    1. [Jason Wei](https://www.jasonwei.net/)
    2. [Chip Huyen](https://huyenchip.com/blog/)
    3. [Sebastian Raschka ](https://sebastianraschka.com/blog/index.html)
9.  [LLM Ecosystem](https://github.com/harirajeev/learn_LLMS/blob/main/LLM_Ecosystem.md)
    
10. [Open Source LLM](https://github.com/harirajeev/learn_LLMS/blob/main/OpenSourceLLM.md)
    

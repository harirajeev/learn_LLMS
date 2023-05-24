[The architecture nomenclature for LLMs is somewhat confusing and unfortunate.](https://www.linkedin.com/posts/yann-lecun_a-survey-of-llms-with-a-practical-guide-and-activity-7057527966540386304-M4_2?utm_source=share&utm_medium=member_desktop)
- What's called "encoder only" actually has an encoder and a decoder (just not an auto-regressive decoder).
- What's called "encoder-decoder" really means "encoder with auto-regressive decoder"
- What's called "decoder only" really means "auto-regressive encoder-decoder"
- autoregressive decoder-style (aka GPT-like)

1.  [Learn LLM](https://github.com/harirajeev/learn_LLMS/blob/main/Learn%20LLM.md)
    1. [Transformers from Scratch](https://e2eml.school/transformers.html#resources)
    2. [GPT-2 (Radford, Ilya Sutskever et al. OPENAI)](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)
    3. [GPT-3 (Brown et al. OPENAI)](https://arxiv.org/pdf/2005.14165.pdf)
    4. [GPT-4](https://aman.ai/primers/ai/GPT-4/)
    5. [Compare LLM Models](https://lightning.ai/pages/community/community-discussions/the-ultimate-battle-of-language-models-lit-llama-vs-gpt3.5-vs-bloom-vs/)
    6. [A Survey of Large Language Models](https://arxiv.org/pdf/2303.18223.pdf)
    7. [How does GPT Obtain its Ability? Tracing Emergent Abilities of Language Models to their Sources](https://yaofu.notion.site/How-does-GPT-Obtain-its-Ability-Tracing-Emergent-Abilities-of-Language-Models-to-their-Sources-b9a57ac0fcf74f30a1ab9e3e36fa1dc1)  <b>SUPER</b>
    8. [The Practical Guides for Large Language Models](https://github.com/Mooler0410/LLMsPracticalGuide) <b>SUPER</b>
    9. [Harnessing the Power of LLMs in Practice: A Survey on ChatGPT and Beyond](https://arxiv.org/pdf/2304.13712.pdf)
    10. Context Length
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
    5. [Quantization](https://github.com/harirajeev/learn_LLMS/blob/main/Quantization.md)
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
    4. [OpenAI Blog](https://openai.com/blog/)
    5. [Google AI Blog](https://ai.googleblog.com/)
    6. [Microsoft Research Blog](https://lnkd.in/g2SRv3Nv)
    7. [NVIDIA Generative AI Blog](https://lnkd.in/gD2ExmPa)
    8. [Meta AI Research](https://lnkd.in/g93iGDyA)
    9. [DeepMind Blog](https://deepmind.com/blog)
    10.[IBM Research Blog](https://lnkd.in/g4wXsu4u)
9.  [LLM Ecosystem](https://github.com/harirajeev/learn_LLMS/blob/main/LLM_Ecosystem.md)
    
10. [Open Source LLM](https://github.com/harirajeev/learn_LLMS/blob/main/OpenSourceLLM.md)

11. Responsible LLMs
    1. [red Teaming](https://huggingface.co/blog/red-teaming)
    2. [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails)
           NeMo Guardrails is an open-source toolkit for easily adding programmable guardrails to LLM-based conversational systems. Guardrails (or "rails" for short) are specific ways of controlling the output of a large language model, such as not talking about politics, responding in a particular way to specific user requests, following a predefined dialog path, using a particular language style, extracting structured data, and more.
    3. [Improve AI Output Using the Guardrails Library with Custom Validators](https://www.mikulskibartosz.name/guardrails-ai-advanced-validators/)    
    4. [OpenAI Moderation tool](https://platform.openai.com/docs/guides/moderation/overview).
       The moderation endpoint is a tool you can use to check whether content complies with OpenAI's usage policies. Developers can thus identify content that our usage policies prohibits and take action, for instance by filtering it. The moderation endpoint is free to use when monitoring the inputs and outputs of OpenAI APIs.
    4. [A Watermark for Large Language Models](https://arxiv.org/abs/2301.10226). “watermarking framework” proposed by a group of researchers. This involves embedding signals into generated text that are invisible to humans but algorithmically detectable. The watermark selects a randomized set of “green” tokens before a word is generated and softly promotes using those tokens during sampling.
       
12. [LLM Leaderboard](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)    

13. [In Context Learning](https://github.com/harirajeev/learn_LLMS/blob/main/InContextLearning.md)
14. [LLM Metric](https://github.com/ray-project/llm-numbers)
15. LLM Repos & Learning Resources
    1. [Awesome-LLMOps](https://github.com/tensorchord/Awesome-LLMOps) 
    2. [Awesome-LLM](https://github.com/Hannibal046/Awesome-LLM)
    3. [Large Language Models - Class Central](https://lnkd.in/exVh6g-K)
    4. [Large Language Models - The Stanford CS324](https://lnkd.in/eJKfDTHK)
    5. [Deploying GPT and Large Language Models - Oreilly](https://lnkd.in/eDDivjB6)
    6. [Understanding Large Language Models - Princeton University](https://lnkd.in/eE44cmza)
    


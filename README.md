[The architecture nomenclature for LLMs is somewhat confusing and unfortunate.](https://www.linkedin.com/posts/yann-lecun_a-survey-of-llms-with-a-practical-guide-and-activity-7057527966540386304-M4_2?utm_source=share&utm_medium=member_desktop)
- What's called "encoder only" actually has an encoder and a decoder (just not an auto-regressive decoder).
- What's called "encoder-decoder" really means "encoder with auto-regressive decoder"
- What's called "decoder only" really means "auto-regressive encoder-decoder"
- autoregressive decoder-style (aka GPT-like)

![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/07c93d37-5ee2-4d4f-8a49-16295d426d7a)

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
    - [Build, customize and control your own personal LLMs - stochatic AI](https://github.com/stochasticai/xturing)
    - [lit-llama, Independent implementation of LLaMA pretraining, finetuning, and inference code](https://github.com/Lightning-AI/lit-llama)
4.  [Fine tuning LLMs](https://magazine.sebastianraschka.com/p/finetuning-large-language-models)
    - Finetuning pre-trained large language models (LLMs) is an effective method to tailor these models to suit specific business requirements and align them with target domain data.
    - This process involves adjusting the model parameters using a smaller dataset relevant to the desired domain, which enables the model to learn domain-specific knowledge and vocabulary.
    - However, as LLMs are “large,” updating multiple layers in a transformer model can be very expensive, so researchers started developing parameter-efficient alternatives.
    1. [Parameter-Efficient Finetuning - PEFT](https://github.com/harirajeev/learn_LLMS/blob/main/PEFT.md)           
    2. [Mixed Precision & Quantization](https://github.com/harirajeev/learn_LLMS/blob/main/MixedPrecision&Quantization.md)
    3. [Example Models](https://github.com/harirajeev/learn_LLMS/blob/main/ExampleModels.md)
5.  [Prompt Engineering](https://github.com/harirajeev/learn_LLMS/blob/main/PromptEngineering.md)    
6.  Vector DB
    1. [tutorial on how to talk to your vector database.- ChatGPT Retrieval Plugin](https://github.com/openai/chatgpt-retrieval-plugin)
7.  Langchain
    1. [Building LLM Powered Applications - Gregory Kamradt](https://www.youtube.com/playlist?list=PLqZXAkvF1bPNQER9mLmDbntNfSpzdDIU5)
8.  Blogs
    1. [Jason Wei](https://www.jasonwei.net/)
    2. [Chip Huyen](https://huyenchip.com/blog/)
    3. [Sebastian Raschka ](https://sebastianraschka.com/blog/index.html)
    4. [Tim Dettmers - quantization](https://timdettmers.com/)
    5. [OpenAI Blog](https://openai.com/blog/)
    6. [Google AI Blog](https://ai.googleblog.com/)
    7. [Microsoft Research Blog](https://lnkd.in/g2SRv3Nv)
    8. [NVIDIA Generative AI Blog](https://lnkd.in/gD2ExmPa)
    9. [Meta AI Research](https://lnkd.in/g93iGDyA)
    10. [DeepMind Blog](https://deepmind.com/blog)
    11. [IBM Research Blog](https://lnkd.in/g4wXsu4u)
9.  [LLM Ecosystem & Evaluation](https://github.com/harirajeev/learn_LLMS/blob/main/LLM_Ecosystem.md)

    LM Evaluation Frameworks
    1. [EleutherAI - LM Evaluation Harness](https://github.com/EleutherAI/lm-evaluation-harness)
10. [Open Source LLM](https://github.com/harirajeev/learn_LLMS/blob/main/OpenSourceLLM.md)

11. [Responsible LLMs](https://github.com/harirajeev/learn_LLMS/blob/main/ResponsibleLLMs.md)
           
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
16. [Knowledge Graphs & LLMS](https://github.com/harirajeev/learn_LLMS/blob/main/KnowledgeGraphs%26LLMS.md)
    


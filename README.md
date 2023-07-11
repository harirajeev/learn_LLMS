[The architecture nomenclature for LLMs is somewhat confusing and unfortunate.](https://www.linkedin.com/posts/yann-lecun_a-survey-of-llms-with-a-practical-guide-and-activity-7057527966540386304-M4_2?utm_source=share&utm_medium=member_desktop)
- What's called "encoder only" actually has an encoder and a decoder (just not an auto-regressive decoder).
- What's called "encoder-decoder" really means "encoder with auto-regressive decoder"
- What's called "decoder only" really means "auto-regressive encoder-decoder"
- autoregressive decoder-style (aka GPT-like)

![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/07c93d37-5ee2-4d4f-8a49-16295d426d7a)

1.  [Learn LLM](https://github.com/harirajeev/learn_LLMS/blob/main/Learn%20LLM.md)
    1. Transformers from Scratch
       - [Transformers from Scratch](https://e2eml.school/transformers.html#resources)
       - [Let's build GPT: from scratch - Andrej Karpathy](https://www.youtube.com/watch?v=kCc8FmEb1nY)       - 
    2. Aman Primers - Excellent
        1. [Primers • Transformers - Excellent Primer from Aman](https://aman.ai/primers/ai/transformers/)
        2. [Primers • Generative Pre-trained Transformer (GPT) - Aman](https://aman.ai/primers/ai/gpt/)
        3. [Primers • Bidirectional Encoder Representations from Transformers (BERT)](https://aman.ai/primers/ai/bert/)
    3. [Google Brain's Lucas Beyer explaining Attention is all you need](https://www.youtube.com/watch?v=EixI6t5oif0)
    4. [GPT-2 (Radford, Ilya Sutskever et al. OPENAI)](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)
    5. [GPT-3 (Brown et al. OPENAI)](https://arxiv.org/pdf/2005.14165.pdf)
    6. [GPT-4](https://aman.ai/primers/ai/GPT-4/)
    7. [Compare LLM Models](https://lightning.ai/pages/community/community-discussions/the-ultimate-battle-of-language-models-lit-llama-vs-gpt3.5-vs-bloom-vs/)
    8. [A Survey of Large Language Models](https://arxiv.org/pdf/2303.18223.pdf)
    9. [LLMS_Paper_Summary_2023](https://github.com/rashmimarganiatgithub/LLMS_Library_2023) <b>SUPER</b>
    10. [How does GPT Obtain its Ability? Tracing Emergent Abilities of Language Models to their Sources](https://yaofu.notion.site/How-does-GPT-Obtain-its-Ability-Tracing-Emergent-Abilities-of-Language-Models-to-their-Sources-b9a57ac0fcf74f30a1ab9e3e36fa1dc1)  <b>SUPER</b>
    11. [The Practical Guides for Large Language Models](https://github.com/Mooler0410/LLMsPracticalGuide) <b>SUPER</b>
    12. [Harnessing the Power of LLMs in Practice: A Survey on ChatGPT and Beyond](https://arxiv.org/pdf/2304.13712.pdf)
    13. Context Length
       1. [Scaling Transformer to 1M tokens and beyond with RMT](https://arxiv.org/pdf/2304.11062.pdf) 
2.  [Training own LLM](https://github.com/harirajeev/learn_LLMS/blob/main/TrainingCustomLLM.md)  

3.  [Prompt Engineering](https://github.com/harirajeev/learn_LLMS/blob/main/PromptEngineering.md)    

4.  [Langchain & LlamaIndex & RAG](https://github.com/harirajeev/learn_LLMS/blob/main/LangchainLlamaIndexRAG.md)
   
5.  [Blogs & Learning Resources](https://github.com/harirajeev/learn_LLMS/blob/main/Blogs&LearningResources.md)
   
6. [LLM Ecosystem & Evaluation](https://github.com/harirajeev/learn_LLMS/blob/main/LLM_Ecosystem&Evalution.md)
    - [Open LLM Leaderboard](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)   
    - [chatbot-arena-leaderboard](https://huggingface.co/spaces/lmsys/chatbot-arena-leaderboard)
    - [Weight watcher LLM Leaderboard](https://weightwatcher.ai/leaderboard.html)
    - [Can foundation models label data like humans? From HF](https://huggingface.co/blog/llm-leaderboard)
    - LM Evaluation Frameworks
        1. [EleutherAI - LM Evaluation Harness](https://github.com/EleutherAI/lm-evaluation-harness)
        2. [Optimum benchmarking utility](https://github.com/huggingface/optimum-benchmark)
        3. [Open LLM-Perf Leaderboard ](https://huggingface.co/spaces/optimum/llm-perf-leaderboard)
7. [Open Source LLM](https://github.com/harirajeev/learn_LLMS/blob/main/OpenSourceLLM.md)

8. [Responsible LLMs](https://github.com/harirajeev/learn_LLMS/blob/main/ResponsibleLLMs.md)         
9. [LLM Metric](https://github.com/ray-project/llm-numbers)
10. [Knowledge Graphs & LLMS](https://github.com/harirajeev/learn_LLMS/blob/main/KnowledgeGraphs%26LLMS.md)
11. [Aman Interview](https://aman.ai/primers/ai/interview/)
12. LLM Ops 
    -  [LLM Ops](https://home.mlops.community/home/content)
    -  [Emerging Architectures for LLM Applications](https://a16z.com/2023/06/20/emerging-architectures-for-llm-applications/)
13. Generating dataset
    - [SELF-INSTRUCT: Aligning Language Models with Self-Generated Instructions 25/5/23 - Yizhong Wang](https://arxiv.org/pdf/2212.10560.pdf)
    - [Principle-Driven Self-Alignment of Language Models from Scratch with Minimal Human Supervision - 4/5/23](https://arxiv.org/pdf/2305.03047v1.pdf)
    - [How Far Can Camels Go? Exploring the State of Instruction Tuning on Open Resources - 7/6/23 - Yizhong Wang](https://arxiv.org/pdf/2306.04751.pdf)
      - We introduce Tülu, a hybrid camel from interbreeding between different species 🐪x🐫.
Tülu contains models from 7-65B that are *full-parameter* finetuned from LLaMa on a combination of 7 datasets.
14. Financial LLMs
    - FinGPT
      - [paper](https://arxiv.org/pdf/2306.06031.pdf)
      - [code](https://github.com/AI4Finance-Foundation/FinGPT)   
    - PIXIU
      - [paper](https://arxiv.org/abs/2306.05443)
      - [code](https://github.com/chancefocus/PIXIU)

15. Financial Datasets
      - CONVFINQ - Oct 2022
        - [CONVFINQA: Exploring the Chain of Numerical Reasoning in Conversational Finance Question Answering](https://arxiv.org/pdf/2210.03849.pdf)
        - https://github.com/czyssrs/ConvFinQA
        - Aiming to study the chain of numerical reasoning in conversational question answering
      - PACIFIC - March 2023
        - [PACIFIC: Towards Proactive Conversational Question Answering over Tabular and Textual Data in Finance](https://arxiv.org/pdf/2210.08817.pdf)
        - https://github.com/dengyang17/PACIFIC/
        - https://github.com/dengyang17/PACIFIC/tree/main/data 
        

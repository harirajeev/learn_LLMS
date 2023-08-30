[The architecture nomenclature for LLMs is somewhat confusing and unfortunate.](https://www.linkedin.com/posts/yann-lecun_a-survey-of-llms-with-a-practical-guide-and-activity-7057527966540386304-M4_2?utm_source=share&utm_medium=member_desktop)
- What's called "encoder only" actually has an encoder and a decoder (just not an auto-regressive decoder).
- What's called "encoder-decoder" really means "encoder with auto-regressive decoder"
- What's called "decoder only" really means "auto-regressive encoder-decoder"
- autoregressive decoder-style (aka GPT-like)

![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/07c93d37-5ee2-4d4f-8a49-16295d426d7a)

1.  [Learn LLM](https://github.com/harirajeev/learn_LLMS/blob/main/Learn%20LLM.md)
    1. [LLMS_Paper_Summary_2023](https://github.com/rashmimarganiatgithub/LLMS_Library_2023)  ****READ THIS ****
    2. [Catching up on the weird world of LLMs](https://simonwillison.net/2023/Aug/3/weird-world-of-llms/) ****READ THIS ****
    3. [neurips2023-llm-efficiency-guide](https://lightning.ai/pages/community/tutorial/neurips2023-llm-efficiency-guide/) ****READ THIS ****
    4. Transformers from Scratch
       - [Transformers from Scratch](https://e2eml.school/transformers.html#resources)
       - [Understanding and Coding the Self-Attention Mechanism of Large Language Models From Scratch-sebastianraschka](https://sebastianraschka.com/blog/2023/self-attention-from-scratch.html) <b>SUPER</b>
       - [Understanding Encoder And Decoder LLMs](https://magazine.sebastianraschka.com/p/understanding-encoder-and-decoder)
       - [Let's build GPT: from scratch - Andrej Karpathy](https://www.youtube.com/watch?v=kCc8FmEb1nY)       - 
    5. Aman Primers - Excellent
        1. [Primers • Transformers - Excellent Primer from Aman](https://aman.ai/primers/ai/transformers/)
        2. [Primers • Generative Pre-trained Transformer (GPT) - Aman](https://aman.ai/primers/ai/gpt/)
        3. [Primers • Bidirectional Encoder Representations from Transformers (BERT)](https://aman.ai/primers/ai/bert/)
        4.  [Primers • LLaMa](https://aman.ai/primers/ai/LLaMA/)
    6. [Google Brain's Lucas Beyer explaining Attention is all you need](https://www.youtube.com/watch?v=EixI6t5oif0)
    7. [GPT-2 (Radford, Ilya Sutskever et al. OPENAI)](https://d4mucfpksywv.cloudfront.net/better-language-models/language_models_are_unsupervised_multitask_learners.pdf)
    8. [GPT-3 (Brown et al. OPENAI)](https://arxiv.org/pdf/2005.14165.pdf)
    9. [GPT-4](https://aman.ai/primers/ai/GPT-4/)
    10. [Compare LLM Models](https://lightning.ai/pages/community/community-discussions/the-ultimate-battle-of-language-models-lit-llama-vs-gpt3.5-vs-bloom-vs/)
    11. [A Survey of Large Language Models](https://arxiv.org/pdf/2303.18223.pdf)
    12. [LLMS_Paper_Summary_2023](https://github.com/rashmimarganiatgithub/LLMS_Library_2023) <b>SUPER</b>
    13. [How does GPT Obtain its Ability? Tracing Emergent Abilities of Language Models to their Sources](https://yaofu.notion.site/How-does-GPT-Obtain-its-Ability-Tracing-Emergent-Abilities-of-Language-Models-to-their-Sources-b9a57ac0fcf74f30a1ab9e3e36fa1dc1)  <b>SUPER</b>
    14. [The Practical Guides for Large Language Models](https://github.com/Mooler0410/LLMsPracticalGuide) <b>SUPER</b>
    15. [Harnessing the Power of LLMs in Practice: A Survey on ChatGPT and Beyond](https://arxiv.org/pdf/2304.13712.pdf)
    16. Context Length
       1. [Scaling Transformer to 1M tokens and beyond with RMT](https://arxiv.org/pdf/2304.11062.pdf) 
2.  [Training own LLM](https://github.com/harirajeev/learn_LLMS/blob/main/TrainFinetuneInference.md)  

3.  [Prompt Engineering](https://github.com/harirajeev/learn_LLMS/blob/main/PromptEngineering.md)    

4.  [Langchain & LlamaIndex & RAG](https://github.com/harirajeev/learn_LLMS/blob/main/LangchainLlamaIndexRAG.md)
   
5.  [Blogs & Learning Resources](https://github.com/harirajeev/learn_LLMS/blob/main/Blogs&LearningResources.md)
   
6. [LLM Ecosystem & Evaluation](https://github.com/harirajeev/learn_LLMS/blob/main/LLM_Ecosystem&Evalution.md)
    - [Open LLM Leaderboard](https://huggingface.co/spaces/HuggingFaceH4/open_llm_leaderboard)
    - [Massive Text Embedding Benchmark (MTEB) Leaderboard - HF](https://huggingface.co/spaces/mteb/leaderboard)
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
    -  [ESG](https://github.com/harirajeev/learn_LLMS/blob/main/ESG.md)
    -  [computational resources](https://github.com/harirajeev/learn_LLMS/blob/main/computationalresources.md)
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
    - [BloombergGPT](https://github.com/harirajeev/learn_LLMS/blob/main/bloombergGPT.md)         

15. Financial Datasets
      - [finance-alpaca](https://huggingface.co/datasets/gbharti/finance-alpaca  )
        - combination of Stanford's Alpaca (https://github.com/tatsu-lab/stanford_alpaca) + FiQA (https://sites.google.com/view/fiqa/) + 1.3k pairs custom generated using GPT3.5
        - 68.9k 
      - FinQA - May 2022
        - [FINQA: A Dataset of Numerical Reasoning over Financial Data](https://arxiv.org/pdf/2109.00122v3.pdf)
        - https://github.com/czyssrs/FinQA
        - FinQA consists of question-answering pairs annotated by experts and their corresponding earnings reports (including unstructured documents and tables) from S&P 500
companies
      - CONVFINQ - Oct 2022
        - [CONVFINQA: Exploring the Chain of Numerical Reasoning in Conversational Finance Question Answering](https://arxiv.org/pdf/2210.03849.pdf)
        - https://github.com/czyssrs/ConvFinQA
        - Aiming to study the chain of numerical reasoning in conversational question answering
        - ConvFinQA is an expansion on FinQA that has conversations with the multi-turn question and answering over earnings reports
      - PACIFIC - March 2023
        - [PACIFIC: Towards Proactive Conversational Question Answering over Tabular and Textual Data in Finance](https://arxiv.org/pdf/2210.08817.pdf)
        - https://github.com/dengyang17/PACIFIC/
        - https://github.com/dengyang17/PACIFIC/tree/main/data 
16. Hardware
      -   NVIDIA also announced its next generation of GPUs, the GH200, which is going to offer 141 GB of RAM (as opposed to 80 GB in the H100)
      -   Maybe another way of solving the LLM long-context problem with brute (hardware) force
17. LLMs and Copyright Laws
      -   "The copyright status of LLMs trained on copyrighted material is not yet fully understood."
      -   The recent legal action taken by various authors against Meta, accusing the company of utilizing their copyrighted works in the training of LLaMA v1.
      -   The reason for this lawsuit was the training data, which included Books3 section of The Pile, encompassing no less than 170,000 books. Notably, the same dataset was used for EleutherAI's GPT-J (a model similar to GPT-3) and BloombergGPT, Bloomberg's language model for finance
      -   New York Times is preparing a lawsuit against OpenAI since it's concerned that ChatGPT generates text that responds to inquiries, drawing from the initial reporting and writing produced by the paper's team.
      -   "fair use"
          -    In the United States, the principle of "fair use" within copyright law may allow the utilization of copyrighted materials without authorization
          -    Provided that the use involves a substantial transformation of the work and does not endanger the copyright owner's interests.
          -    However, whether this concept of fair use extends to the training of machine learning models is still unresolved.
          -    [Japan declared that it would permit generative AI training on any kind of data and that it will not enforce copyrights when it comes to training generative AI models.](https://petapixel.com/2023/06/05/japan-declares-ai-training-data-fair-game-and-will-not-enforce-copyright/)
          -    AI Act in the EU requires companies to publicly disclose any copyrighted work used in training.not very clear on what happens if copyrights are violated
          -    Overall, it seems that a lot of rules are still being drafted and amended
        
![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/fb87fa13-265b-4221-a013-7bd0467e4ebe)

- [<b>Risk</b>](https://github.com/harirajeev/learn_LLMS/blob/main/risk.md)
- <b>Hallucination</b>
   - [A Survey on Hallucination in Large Language Models:Principles, Taxonomy, Challenges, and Open Questions](https://arxiv.org/pdf/2311.05232.pdf)     
   - 

![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/a4ace62b-760e-4600-8979-09e98385f951)
[source](https://ksankar.medium.com/part-2-chatgpt-threat-vectors-guardrails-for-llmops-dbca8e0e68d4_)

<b>Literature Survey:</b>
-  [Machine Unlearning](https://ai.googleblog.com/2023/06/announcing-first-machine-unlearning.html)
      - Significant privacy challenges arise when parts of training data for ML models is supposed to be deleted, e.g. because of the right to be forgotten. Even after an individual's data is deleted from a database, the trained model will still benefit from the use of the personal data having been part of the training set.
      - Additionally, it can be possible to infer the use of personal data in model training with membership inference attacks.
      - Machine unlearning aims to address these concerns with the goal to remove information about some specific samples from a model.
      - [Machine Unlearning: A Survey](https://dl.acm.org/doi/pdf/10.1145/3603620)
      - [IN-CONTEXT UNLEARNING: LANGUAGE MODELS AS FEW SHOT UNLEARNERS](https://arxiv.org/pdf/2310.07579.pdf)
-  [Privacy Risks in Language Models:](https://github.com/harirajeev/learn_LLMS/blob/main/PrivacyRiskInLLM.md)
-  [Prompt injection with control characters](https://dropbox.tech/machine-learning/prompt-injection-with-control-characters-openai-chatgpt-llm)
-  Adversarial Attacks
      - [Universal and Transferable Adversarial Attacks on Aligned Language Models](https://arxiv.org/pdf/2307.15043.pdf)       
-  [Reporting standards for Machine Learning Based Science (REFORMS)](https://reforms.cs.princeton.edu/?utm_source=substack&utm_medium=email)
      -  To provide clear reporting standards for ML-based science across disciplines.       
      -  [REFORMS checklist template](https://reforms.cs.princeton.edu/appendices.pdf?utm_source=substack&utm_medium=email)
      -  [Checklist for reporting ML-based science:](https://reforms.cs.princeton.edu/obermeyer-sample.pdf)
      -        
- [Challenges and Applications of Large Language Models](https://arxiv.org/pdf/2307.10169.pdf)
- [Identifying and Mitigating the Security Risks of Generative AI](https://arxiv.org/pdf/2308.14840.pdf)
- [Generative AI meets Responsible AI (Tutorial)](https://sites.google.com/view/responsible-gen-ai-tutorial/home?authuser=0)
- 
<b>Read on :</b>

1. [red Teaming](https://huggingface.co/blog/red-teaming)
2. [NeMo Guardrails](https://github.com/NVIDIA/NeMo-Guardrails)
           NeMo Guardrails is an open-source toolkit for easily adding programmable guardrails to LLM-based conversational systems. Guardrails (or "rails" for short) are specific ways of controlling the output of a large language model, such as not talking about politics, responding in a particular way to specific user requests, following a predefined dialog path, using a particular language style, extracting structured data, and more.
3. [Improve AI Output Using the Guardrails Library with Custom Validators](https://www.mikulskibartosz.name/guardrails-ai-advanced-validators/)    
4. [OpenAI Moderation tool](https://platform.openai.com/docs/guides/moderation/overview).
       The moderation endpoint is a tool you can use to check whether content complies with OpenAI's usage policies. Developers can thus identify content that our usage policies prohibits and take action, for instance by filtering it. The moderation endpoint is free to use when monitoring the inputs and outputs of OpenAI APIs.
4. [WaterMarking](https://github.com/harirajeev/learn_LLMS/blob/main/WaterMarking)
   - [A Watermark for Large Language Models](https://arxiv.org/abs/2301.10226). “watermarking framework” proposed by a group of researchers. This involves embedding signals into generated text that are invisible to humans but algorithmically detectable. The watermark selects a randomized set of “green” tokens before a word is generated and softly promotes using those tokens during sampling.
6. [Introducing Google’s Secure AI Framework](https://blog.google/technology/safety-security/introducing-googles-secure-ai-framework/)
7. [Do Foundation Model Providers Comply with the EU AI Act?](https://crfm.stanford.edu/2023/06/15/eu-ai-act.html)
8. [Machine Unlearning](https://ai.googleblog.com/2023/06/announcing-first-machine-unlearning.html)  *ToDO
9. [Auditing large language models: a three-layered approach](https://link.springer.com/article/10.1007/s43681-023-00289-2)
10. [Policies, data and analysis for trustworthy artificial intelligence](https://oecd.ai/en/)
11. [GRACE Governance for Large Language Models (LLMs)](https://2021.ai/grace-governance-llm/)
12. [Catalogue of Tools & Metrics for Trustworthy AI](https://oecd.ai/en/catalogue/tools) <b>GOOD</b>
13. [On the Opportunities and Risks of Foundation Models - This paper coined the term FOUNDATION MODELS](https://arxiv.org/pdf/2108.07258.pdf)
14. [FRONTIER AI REGULATION: MANAGING EMERGING RISKS TO PUBLIC SAFETY - This paper coined the term FRONTIER AI MODELS](https://arxiv.org/pdf/2307.03718.pdf)
    -  We define “frontier AI models” as highly capable foundation models that could exhibit dangerous capabilities    
![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/20cfa986-fd5d-4dd0-a02d-4a877b4eed94)

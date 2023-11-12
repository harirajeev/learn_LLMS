- [Semantic Answer Similarity: The Smarter Metric to Score Question Answering Predictions](https://www.deepset.ai/blog/semantic-answer-similarity-to-evaluate-qa)
- [Semantic Answer Similarity for Evaluating Question Answering Models](https://arxiv.org/abs/2108.06130)
- [LLM Eval: Guard Rails, Prompting](https://docs.google.com/document/d/1ndYxbN9O7dGKeVXR53B3xHFszniSyho6KLaq-aniDRo/edit#heading=h.j5cyenlrao7z)
- Perplexity. Measures how well the probability distribution predicted by the model aligns with the actual distribution of words. It is not always correlated with human judgment. Doesn’t work as well comparing models across different tasks.

- GLUE (General Language Understanding Evaluation). A collection of NLP tasks. Doesn’t

- Human evaluation.

- LLM evaluation.

- BLEU (Bilingual Evaluation Understudy). Compares n-grams in the model’s output to reference outputs. Sensitive to slight variations (only exact matches). Other variations that have improved on BLEU are ROUGE (Recall-Oriented Understudy for Gisting Evaluation) and METEOR (Metric for Evaluation of Translation with Explicit ORdering).

- F1 Score/Precision/Recall. A classic way of measuring model quality. Evaluates the balance between precision and recall.

- <b> Retrieval Evaluation </b>
  -  To gauge the efficacy of our retrieval system, we primarily relied on two widely accepted metrics: Hit Rate and Mean Reciprocal Rank (MRR)
  -  Hit rate : calculates the fraction of queries where the correct answer is found within the top-k retrieved documents.
  -  Mean Reciprocal Rank (MRR) :
     - For each query, MRR evaluates the system’s accuracy by looking at the rank of the highest-placed relevant document.
     - Specifically, it’s the average of the reciprocals of these ranks across all the queries.
     - So, if the first relevant document is the top result, the reciprocal rank is 1; if it’s second, the reciprocal rank is 1/2, and so on 
- Evaluate Hallucination
  - [HaluEval: A Hallucination Evaluation Benchmark for LLMs](https://github.com/RUCAIBox/HaluEval)
  - [Does your LLM application hallucinate?](https://medium.com/@saptarshichaudhuri/does-your-llm-application-hallucinate-e06eb3868a88)
  - [Measuring Hallucinations in RAG Systems](https://vectara.com/measuring-hallucinations-in-rag-systems/?utm_source=LinkedIn&utm_medium=social&utm_campaign=GaggleAMP&utm_content=do-models-like-openais-gpt4-and-googles-palm-produce-inaccura-4232853&activity_id=4232853)
  - [Cut the Bull…. Detecting Hallucinations in Large Language Models](https://vectara.com/cut-the-bull-detecting-hallucinations-in-large-language-models/)
  - you can hook it up to a vectordb and ask the llm to check itself with zero temperature.





<b>Privacy Risks in Language Models:</b>
- LLMs are vulnerable to privacy attacks, as they may inadvertently memorize private training data and leak information to potential adversaries.
- The strongest attack recovers training data from LLMs by first generating sequences from the models and then scoring those sequences with various membership inference methods. Below paper talks about this.      - 
- [Extracting Training Data from Large Language Models - a training data extraction attack](https://www.usenix.org/system/files/sec21-carlini-extracting.pdf)
- The study uploaded below shows that such attacks can be largely attributed to duplicated sequences present in commonly used web-scraped training datasets.
- [Deduplicating Training Data Mitigates Privacy Risks in Language Models](https://proceedings.mlr.press/v162/kandpal22a.html)
  - The authors examined transformer LLMs with different parameter scales and made two key observations:
  - the likelihood of the attack successfully recovering a specific training sequence correlates with the number of times that sequence appears in the training data. For instance, a sequence that is present 10 times in the training data is on average generated 1000x more often than a sequence that is present only once.
  - the overall effectiveness of the attack is reduced when sequence-level duplication in the training data is eliminated.
  - After applying methods to deduplicate training data, language models are considerably more secure against these types of privacy attacks.
  - Taken together, the results call for an increased focus on deduplication in privacy-sensitive applications and a reevaluation of the practicality of existing privacy attacks.
  - The authors highlight that to create privacy-preserving machine learning models, one must go beyond simply identifying privacy vulnerabilities and instead trace the causes of vulnerabilities back to the training algorithms, models, and datasets.
- [Processing Data for Large Language Models - includes deduplication](https://wandb.ai/wandb_gen/llm-data-processing/reports/Processing-Data-for-Large-Language-Models--VmlldzozMDg4MTM2)
- De-duplication can be done at different levels of granularity, ranging from exact matches to using fuzzy de-duplication tools like "deduplicate-text-datasets" and "datasketch" to reduce and eliminate redundant text from the corpus.
- [Mapping privacy-enhancing technologies to your use cases](https://www.tmlt.io/resources/mapping-privacy-enhancing-technologies-to-your-use-cases)

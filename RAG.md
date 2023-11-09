![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/0285c2c1-5897-4231-917d-b0475fff8f2e)

- [RAG CHALLENGES](https://github.com/harirajeev/learn_LLMS/blob/main/RAG%20Challenges.md)
-  [ Chunking Strategies ](https://github.com/harirajeev/learn_LLMS/blob/main/chunking%20strategies.md)
- [Building RAG-based LLM Applications for Production](https://www.anyscale.com/blog/a-comprehensive-guide-for-building-rag-based-llm-applications-part-1)
- [Evaluation](https://github.com/harirajeev/learn_LLMS/blob/main/Evaluation.md)
- [Maximizing LLM performance](https://blog.ankitsanghvi.in/maximizing-llm-performace/)

🧠Fine-Tuning vs 🔍RAG: A short comparison

- The AI landscape is ever evolving, and adapting language models to cater to specific tasks or domains is crucial. 
- Two primary approaches that can be employed in this context are Fine-Tuning and Retrieval Augmented Generation (RAG). 
- Customers ask this all the time, when to employe which approach. In this post, we will delve deeper into the benefits of each method and provide insights on when to employ which approach.

- 🎯 Fine-Tuning (or Retraining):
    * Fine-Tuning is ideal when you need to train large language models (LLMs) for a completely different task, such as generating code or translating languages.
    * The main challenge of this approach is the resource-intensive nature of collecting and labeling training data, as well as the computational power required to train the model.
    * Fine-Tuning demands professional data science skills to optimize the objective function, making it more suitable for experienced practitioners or teams with dedicated resources.

- 🌐 Retrieval Augmented Generation (RAG):
    * RAG is perfect for adapting LLMs to a new domain while constraining the model to an existing knowledge base, such as company data, document stores, or other structured/unstructured sources.
    * This method is more cost-efficient compared to fine-tuning, as it leverages pre-existing knowledge bases and requires fewer resources to implement.
    * RAG is more accessible and user-friendly, as it can be employed using low-code or no-code skills, making it ideal for teams with diverse skill sets.

- In conclusion, the choice between Fine-Tuning and RAG depends on the specific goals and resources of your project. 
- If you aim to teach the model an entirely new task and have the necessary data science expertise, Fine-Tuning could be a suitable choice. 
- On the other hand, if the focus is on adapting the model to a new domain with constraints and a limited budget, RAG could offer a more efficient and accessible solution.
- [RAG Paper](https://arxiv.org/pdf/2005.11401.pdf)
- [RETRO Paper](https://arxiv.org/pdf/2112.04426.pdf)
- [Augmented Language Models: a Survey](https://arxiv.org/pdf/2302.07842.pdf)
- [How to count tokens with tiktoken](https://github.com/openai/openai-cookbook/blob/main/examples/How_to_count_tokens_with_tiktoken.ipynb)
- https://medium.com/@pandey.vikesh/rag-ing-success-guide-to-choose-the-right-components-for-your-rag-solution-on-aws-223b9d4c7280
- [Deploying RAG to Production](https://haystack.deepset.ai/blog/rag-deployment)
- [Why RAG is the key to safer applications with large language models](https://www.deepset.ai/blog/llms-retrieval-augmentation)
- RAG Use Case
     - 𝗨𝘀𝗲𝗰𝗮𝘀𝗲:  A research company wants to enable their clients  ask queries against the research documents published by them. To leverage the power of longer contexts, they would have to train (not fine-tune) models on their proprietary data. This can be very pricey even with 2K. btw, 𝗧𝗿𝗮𝗶𝗻𝗶𝗻𝗴 𝟲𝟱𝗕 𝗟𝗟𝗮𝗠𝗔 on 100K would cost ~$150M.
     - How can we build the same claim processing app w/o expensive training:  Enter Retrieval Augmented Generation (RAG).
     - Here is the step by step:
         1. Chunk, embed, & index documents in VectorDBs (Vdb) like Weaviate or Pinecone
         2. Match the query embedding of the client.
         3. Retrieve the relevant context from Vdb.
         4. Do RAG using pre-trained LLMs such as Google's PaLM or OpenAI's GPTx.
     - 𝗪𝗵𝘆 𝗥𝗔𝗚 & 𝗘𝗻𝘁𝗲𝗿𝗽𝗿𝗶𝘀𝗲𝘀 𝗮𝗿𝗲 𝗮 𝗺𝗮𝘁𝗰𝗵 𝗺𝗮𝗱𝗲 𝗶𝗻 𝗵𝗲𝗮𝘃𝗲𝗻?
         1. Flexibility:  What if a client is not authorized to see certain documents ?You need a Role-Based Authorization Control (RBAC). It is easier to do RBAC with a RAG solution.
         2. Practicality: It is easier to index new docs in VDBs, but retraining is expensive.
         3. Broader Coverage: Only Information Extraction cases necessitate longer contexts. if you dodge that with RAG, for other uses you can use fine-tuning with a shorter context.
         4. Interpretability: Retriever knows the exact documents.
     - Embedding model that can handle longer documents?
         - Owing to self-attention’s quadratic time and space complexity there will always be a context limitation original BERT had 512.
         - But the practical problem is there is no guarantee one model will handle all document lengths. There will always be outliers in spite of you throwing a boatload of money on say 2048 context still it’s not comprehensive.
         - So a better solution is to chunk documents and store them with smaller context-length models. You could save on storage costs and retrieval time.
     - When dealing with a vast corpus, beyond the embedding retrievals, a retrieval and re-ranking method is generally recommended and or maximal marginal relevance (MMR) criterion on all the document candidates.
     - [TOP MISCONCEPTIONS OF RAG](https://media.licdn.com/dms/document/media/D561FAQFslxFrkRRp9A/feedshare-document-pdf-analyzed/0/1694709823484?e=1696464000&v=beta&t=6peZ0-W0TFFpnYaz3nh6TlvHuEOyB2i1p_aLHNzJFk4)

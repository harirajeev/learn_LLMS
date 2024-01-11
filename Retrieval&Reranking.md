- [Rerankers and Two-Stage Retrieval](https://www.pinecone.io/learn/series/rag/rerankers/)
  - Retrival
    - [semantic chunking](https://llamahub.ai/l/llama_packs-node_parser-semantic_chunking?from=all)
    - [5 levels of text splitting](https://github.com/FullStackRetrieval-com/RetrievalTutorials/blob/main/5_Levels_Of_Text_Splitting.ipynb) 
    - Vector search
      - vectors are essentially compressions of the "meaning" behind some text into (typically) 768 or 1536-dimensional vectors
      - There is some information loss because we're compressing this information into a single vector.
      - Because of this information loss, we often see that the top three (for example) vector search documents will miss relevant information.
      - Unfortunately, the retrieval may return relevant information below our top_k cutoff.
      - What do we do if relevant information at a lower position would help our LLM formulate a better response?
      - The metric we would measure here is recall — meaning "how many of the relevant documents are we retrieving".
      - Recall (retrieval recall ) does not consider the total number of retrieved documents — so we can hack the metric and get perfect recall by returning everything.
      - Unfortunately, we cannot return everything. LLMs have limits on how much text we can pass to them — we call this limit the context window.
      - We cannot use context stuffing because this reduces the LLM's recall performance
      - When storing information in the middle of a context window, an LLM's ability to recall that information becomes worse than had it not been provided in the first place
      - LLM recall refers to the ability of an LLM to find information from the text placed within its context window.
      - Research shows that LLM recall degrades as we put more tokens in the context window
      - The solution to this issue is to maximize retrieval recall by retrieving plenty of documents and then maximize LLM recall by minimizing the number of documents that make it to the LLM.
      - To do that, we reorder retrieved documents and keep just the most relevant for our LLM — to do that, we use reranking.
  - Reranking
      - A reranking model — also known as a cross-encoder — is a type of model that, given a query and document pair, will output a similarity score.
      - We use this score to reorder the documents by relevance to our query.
      - rerankers are slow, and retrievers are fast
      - rerankers are much more accurate than embedding models.
      - Bi-Encoder models are fast, but less accurate. while Cross-Encoders are more accurate, but slow.
      - The intuition behind a bi-encoder's inferior accuracy is that bi-encoders must compress all of the possible meanings of a document into a single vector — meaning we lose information
      - bi-encoders have no context on the query because we don't know the query until we receive it (we create embeddings before user query time).
      - a reranker can receive the raw information directly into the large transformer computation, meaning less information loss
      - we have the added benefit of analyzing our document's meaning specific to the user query — rather than trying to produce a generic, averaged meaning.
      - Rerankers avoid the information loss of bi-encoders — but they come with a different penalty — time.
      - With rerankers, we are not pre-computing anything
      - Instead, we're feeding our query and a single other document into the transformer, running a whole transformer inference step, and outputting a single similarity score.
      - Cross-Encoder models do not produce vector embeddings for data, but use a classification mechanism for data pairs instead.
      - The input of the model always consists of a data pair, for example two sentences, and outputs a value between 0 and 1 indicating the similarity between these two sentences
      - So, individual sentences cannot be passed to a Cross-Encoder model, it always needs a pair of "items".
      - In terms of search, you need to use the Cross-Encoder with each data item and the search query, to calculate the similarity between the query and data object.
   
    ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/14fb5ca6-0809-4b80-bcdf-594c82d7d762)

    ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/dc508386-c0f4-4078-8b07-bab53c033890)

![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/bf3b2b45-bae3-42f5-a3e1-013717578dce)

-  <b> Two stage retrieval process </b>
   -   Retrieval stage - The first stage uses embedding-based retrieval with a high top-k value to maximize recall while accepting a lower precision.
       -   Maximize recall while accepting a lower precision
       -   High recall means that an algorithm returns most of the relevant results (whether or not irrelevant ones are also returned).
       -   Initial high-recall stage handle the variations in the ways humans speak and write,
   -   [Reranking Stage](https://www.pinecone.io/learn/series/rag/rerankers/) - Second stage uses a slightly more computationally expensive process that is higher precision and lower recall (for instance with BM25) to “rerank” the existing retrieved candidates.
       -   Higher precision and lower recall
       -   Higher precision means that an algorithm returns more relevant results than irrelevant ones
       -   High-precision stage to accurately reflect the importance of relevance from things like phrases.
   -  ![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/7022df94-6da8-4b6c-904f-b13e539da98f)

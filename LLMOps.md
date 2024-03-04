- [Hidden Technical Debt in GenAI systems](https://github.com/harirajeev/learn_LLMS/blob/main/TechnicalDebt.md)
- LLM Caching
  -    Measuring latency for same input request for the second time using text only caching or semantic caching.
  -    This is server side LLM caching, so the latency would consists of only network API call latency.
  -    There are below LLM caching integrations which are available with Langchain and LLM:
        -    In Memory cache
        -    SQLite cache
        -    Redis cache
        -    GPT cache
        -    Redis and GPT cache provides two options:
             - Exact text based cache
             - Semantic similarity cache(Interesting to evaluate)
  -    All cache integrations provide similar performance benefits for LLM inference API, reducing latency to 0.1–0.2 second. LLM cache reduces tp50 latency of LLM API significantly.  
- [Guardrails Hub](https://hub.guardrailsai.com/)
    -  https://www.guardrailsai.com/blog/the-future-of-ai-reliability
-  [LLMLite](https://github.com/BerriAI/litellm)
    -  Call all LLM APIs using the OpenAI format
-   [Monolithic vs. Microservice Architectural Patterns](https://towardsdatascience.com/anatomy-of-llm-based-chatbot-applications-monolithic-vs-microservice-architectural-patterns-77796216903e)
-   [A practical guide to building a headless ChatGPT application with Streamlit, FastAPI, and the OpenAI API](https://towardsdatascience.com/decoupled-frontend-backend-microservices-architecture-for-chatgpt-based-llm-chatbot-61637dc5c7ea)
-   [What Is OAuth2?](https://medium.com/fintechexplained/what-is-oauth2-cdf2cfd69309)
    -   [RS256 vs HS256: What's The Difference?](https://auth0.com/blog/rs256-vs-hs256-whats-the-difference/)
-   [Auth0 + Python + FastAPI API Seed - Github](https://github.com/auth0-blog/auth0-python-fastapi-sample/tree/main)
-   [A Watermark for Large Language Models](https://arxiv.org/abs/2301.10226)
-   Serving Options
      -    [TGI - HuggingFace Interface Tool](https://github.com/huggingface/text-generation-inference)
      -    [vLLM - 𝐕𝐞𝐫𝐬𝐚𝐭𝐢𝐥𝐞 𝐥𝐚𝐫𝐠𝐞 𝐥𝐚𝐧𝐠𝐮𝐚𝐠𝐞 𝐦𝐨𝐝𝐞𝐥](https://github.com/vllm-project/vllm)
            -    is an open source framework designed to enhance the inference and serving speed of LLMs.
            -    It has demonstrated remarkable performance improvements compared to mainstream frameworks like Hugging Face’s Transformers, primarily because of a highly innovative new algorithm at its core.
            -    vLLM only works with NVIDIA hardware
            -    Currently vLLM framework provides excellent latency and throughput performance for LLM with paged attention:
            -    this is best LLM serving framework as of now which provides excellent latency performance
            -    One key reason behind vLLM’s speed during inference is its use of the 𝐏𝐚𝐠𝐞𝐝 𝐀𝐭𝐭𝐞𝐧𝐭𝐢𝐨𝐧 𝐭𝐞𝐜𝐡𝐧𝐢𝐪𝐮𝐞.
                  -  In traditional attention mechanisms, the keys and values computed are stored in GPU memory as a KV cache.
                  -  This cache stores attention keys and values for previous tokens, which can consume a significant amount of memory,
                  -  especially for large models and long sequences.
                  -  These keys and values are also stored in a contiguous manner.
                  -  VLLM achieves better performance than TGI and the Hugging Face transformer library, with up to 24x higher throughput compared to Hugging Face and up to 3.5x higher throughput than TGI.
      -    [Lorax](https://github.com/predibase/lorax)
 
![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/6dd6726e-2dc3-4d1f-9476-6e4abfd308d9)

 
- Metrics that Matter for LLM Serving , So here are four key metrics for LLM serving:
    1. Time to First Token (TTFT): Measure the time it takes for the model to generate the first token after a user query. Lower TTFT means a more responsive user experience.
    2. Time Per Output Token (TPOT): Calculate the time required for the model to generate one token for a specific query. Faster TPOT means a quicker model perceived by users.
    3. Latency: Sum the TTFT and total token generation time multiplied by TPOT to measure the overall time taken for the model to provide a response.
    4. Throughput: Measure the number of output tokens the server generates per second for all users and queries. Optimize for maximum throughput to improve the server's capacity and user experience.
  

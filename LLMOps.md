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
      -    [vLLM](https://github.com/vllm-project/vllm)
            -    vLLM only works with NVIDIA hardware
      -    [Lorax](https://github.com/predibase/lorax)
 
![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/6dd6726e-2dc3-4d1f-9476-6e4abfd308d9)

 
- Metrics that Matter for LLM Serving , So here are four key metrics for LLM serving:
    1. Time to First Token (TTFT): Measure the time it takes for the model to generate the first token after a user query. Lower TTFT means a more responsive user experience.
    2. Time Per Output Token (TPOT): Calculate the time required for the model to generate one token for a specific query. Faster TPOT means a quicker model perceived by users.
    3. Latency: Sum the TTFT and total token generation time multiplied by TPOT to measure the overall time taken for the model to provide a response.
    4. Throughput: Measure the number of output tokens the server generates per second for all users and queries. Optimize for maximum throughput to improve the server's capacity and user experience.
  

From OpenAI
- 1 token ~= 4 chars in English
- 1 token ~= ¾ words
- 100 tokens ~= 75 words
- 1,500 words ~= 2k tokens
- Since, 500 words ~= 1 A4 page
- 4k ~= 6 A4 pages of text
- 5M Tokens is equal to entire GitHub repositories and thousands of documents.
- Typical LLM input today is max 15-60 pages of text (8k-32k tokens)

1. https://thegradient.pub/in-context-learning-in-context/
2. http://ai.stanford.edu/blog/understanding-incontext/
3. [LARGER LANGUAGE MODELS DO IN-CONTEXT LEARNING DIFFERENTLY](https://arxiv.org/pdf/2303.03846.pdf)
4. https://transformer-circuits.pub/2022/in-context-learning-and-induction-heads/index.html
5. [Scaling Transformer to 1M tokens and beyond with RMT](https://arxiv.org/pdf/2304.11062.pdf) 
6. [Blockwise Parallel Transformer for Long Context Large Models](https://arxiv.org/pdf/2305.19370.pdf)
7. ["𝗘𝘅𝘁𝗲𝗻𝗱𝗶𝗻𝗴 𝗖𝗼𝗻𝘁𝗲𝘅𝘁 𝗶𝘀 𝗛𝗮𝗿𝗱…𝗯𝘂𝘁 𝗻𝗼𝘁 𝗜𝗺𝗽𝗼𝘀𝘀𝗶𝗯𝗹𝗲” explores and tests how to extend LLaMa to 8k](https://kaiokendev.github.io/context)
8. ["𝗧𝗵𝗲 𝗦𝗲𝗰𝗿𝗲𝘁 𝗦𝗮𝘂𝗰𝗲 𝗯𝗲𝗵𝗶𝗻𝗱 𝟭𝟬𝟬𝗞 𝗰𝗼𝗻𝘁𝗲𝘅𝘁 𝘄𝗶𝗻𝗱𝗼𝘄 𝗶𝗻 𝗟𝗟𝗠𝘀: 𝗮𝗹𝗹 𝘁𝗿𝗶𝗰𝗸𝘀 𝗶𝗻 𝗼𝗻𝗲 𝗽𝗹𝗮𝗰𝗲” explores main paint points and tricks to extend the context length.](https://blog.gopenai.com/how-to-speed-up-llms-and-use-100k-context-window-all-tricks-in-one-place-ffd40577b4c)
9. [Lost in the Middle: How Language Models Use Long Contexts](https://arxiv.org/pdf/2307.03172.pdf)
    - relatively little is known about how well the language models use longer context.
    - performance is often highest when relevant information occurs at the beginning or end of the input context, and significantly degrades when models must
access relevant information in the middle of long contexts
    - performance substantially decreases as the input context grows longer, even for explicitly long-context models
    - Language models are generally implemented with Transformers, which scale poorly to long sequences (e.g., since self-attention complexity is quadratic
with the input sequence length)
    - https://github.com/nelson-liu/lost-in-the-middle
    - whats Increasing language model maximum context length
      - Recent advances in hardware (e.g., faster GPUs with more memory) 
      - algorithms (e.g., FlashAttention; Dao et al., 2022) have driven a rapid increase in language model maximum context length. 
      - Finally, a variety of recently-proposed architectures model sequences with millions of tokens, raising the potential of further dramatic increases in language
model maximum context length 
    - 1) I would expect that the RNN-based LLMs like RWKV (since it's processing information sequentially, it might rather forget early information)
      2) there is no specific inductive bias in transformer-based LLM architectures that explains why the retrieval performance should be worse for text in the middle of the document. I suspect it is all because of the training data and how humans write: the most important information is usually in the beginning or the end (think paper Abstracts and Conclusion sections), and it's then how LLMs parameterize the attention weights during training.



10. [Extending Context is Hard…but not Impossible](https://kaiokendev.github.io/context)

11. LLMs for longer contexts: We had
    1) Lost in the Middle: How Language Models Use Long Contexts: https://arxiv.org/abs//2307.03172
    2) Scaling Transformer to 1M tokens and beyond with RMT: https://arxiv.org/abs/2304.11062
    3) Hyena Hierarchy: Towards Larger Convolutional Language Models: https://arxiv.org/abs/2302.10866
    4) LongNet: LongNet: Scaling Transformers to 1,000,000,000 Tokens: https://arxiv.org/abs/2307.02486
    5) [<b>Positional Interpolation</b> - Extending Context Window of Large Language Models via Positional Interpolation](https://arxiv.org/abs/2306.15595)

Waitlist link: https://magic.dev/waitlist

![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/0d7a98d0-31b1-4fd6-ab05-f04fcab97182)

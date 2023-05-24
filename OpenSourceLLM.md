1. [LLaMA, Meta’s Open Source LLM](https://thenewstack.io/why-open-source-developers-are-using-llama-metas-ai-model/)
   - [LLaMa](https://aman.ai/primers/ai/LLaMA/)

2. From a business perspective, I can see this being useful from at least two angles: 

       1. how can we be better than the competition if we use the same off-the-shelf solution others are using and 
       2. if it's open source, we have full control and are not affected by API changes and restrictions

3. https://www.semianalysis.com/p/google-we-have-no-moat-and-neither?utm_source=bensbites&utm_medium=newsletter&utm_campaign=knighty-byte-open-source-crusade
4. [PrivatGPT](https://github.com/imartinez/privateGPT)

#*****************************************************************************************************************************************************

The Timeline

1. Feb 24, 2023 - LLaMA is Launched
  Meta launches LLaMA, open sourcing the code, but not the weights. At this point, LLaMA is not instruction or conversation tuned. Like many current models, it is a    relatively small model (available at 7B, 13B, 33B, and 65B parameters) that has been trained for a relatively large amount of time, and is therefore quite capable relative to its size.

2. March 3, 2023 - The Inevitable Happens
  https://www.vice.com/en/article/xgwqgw/facebooks-powerful-large-language-model-leaks-online-4chan-llama
Within a week, LLaMA is leaked to the public. The impact on the community cannot be overstated. Existing licenses prevent it from being used for commercial purposes, but suddenly anyone is able to experiment. From this point forward, innovations come hard and fast.

3. March 12, 2023 - Language models on a Toaster
  A little over a week later, Artem Andreenko gets the model working on a Raspberry Pi. At this point the model runs too slowly to be practical because the weights must be paged in and out of memory. Nonetheless, this sets the stage for an onslaught of minification efforts.

4. March 13, 2023 - Fine Tuning on a Laptop
  The next day, Stanford releases Alpaca, which adds instruction tuning to LLaMA. More important than the actual weights, however, was Eric Wang’s alpaca-lora repo, which used low rank fine-tuning to do this training “within hours on a single RTX 4090”.

  Suddenly, anyone could fine-tune the model to do anything, kicking off a race to the bottom on low-budget fine-tuning projects. Papers proudly describe their total   spend of a few hundred dollars. What’s more, the low rank updates can be distributed easily and separately from the original weights, making them independent of the  original license from Meta. Anyone can share and apply them.

5. March 18, 2023 - Now It’s Fast
  Georgi Gerganov uses 4 bit quantization to run LLaMA on a MacBook CPU. It is the first “no GPU” solution that is fast enough to be practical.

6. March 19, 2023 - A 13B model achieves “parity” with Bard
  The next day, a cross-university collaboration releases Vicuna, and uses GPT-4-powered eval to provide qualitative comparisons of model outputs. While the  evaluation method is suspect, the model is materially better than earlier variants. Training Cost: $300.

  Notably, they were able to use data from ChatGPT while circumventing restrictions on its API - They simply sampled examples of “impressive” ChatGPT dialogue posted on sites like ShareGPT.

7. March 25, 2023 - Choose Your Own Model
  Nomic creates GPT4All, which is both a model and, more importantly, an ecosystem. For the first time, we see models (including Vicuna) being gathered together in   one place. Training Cost: $100.

8. March 28, 2023 - Open Source GPT-3
  Cerebras (not to be confused with our own Cerebra) trains the GPT-3 architecture using the optimal compute schedule implied by Chinchilla, and the optimal scaling  implied by μ-parameterization. This outperforms existing GPT-3 clones by a wide margin, and represents the first confirmed use of μ-parameterization “in the wild”.   These models are trained from scratch, meaning the community is no longer dependent on LLaMA.

9. March 28, 2023 - Multimodal Training in One Hour
  Using a novel Parameter Efficient Fine Tuning (PEFT) technique, LLaMA-Adapter introduces instruction tuning and multimodality in one hour of training. Impressively,  they do so with just 1.2M learnable parameters. The model achieves a new SOTA on multimodal ScienceQA.

10. April 3, 2023 - Real Humans Can’t Tell the Difference Between a 13B Open Model and ChatGPT
  Berkeley launches Koala, a dialogue model trained entirely using freely available data.

  They take the crucial step of measuring real human preferences between their model and ChatGPT. While ChatGPT still holds a slight edge, more than 50% of the time  users either prefer Koala or have no preference. Training Cost: $100.

11. April 15, 2023 - Open Source RLHF at ChatGPT Levels
  Open Assistant launches a model and, more importantly, a dataset for Alignment via RLHF. Their model is close (48.3% vs. 51.7%) to ChatGPT in terms of human  preference. In addition to LLaMA, they show that this dataset can be applied to Pythia-12B, giving people the option to use a fully open stack to run the model.  Moreover, because the dataset is publicly available, it takes RLHF from unachievable to cheap and easy for small experimenters.

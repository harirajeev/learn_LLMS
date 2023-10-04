- LLaMA
   -   Open Source
         -   [Meta’s LLaMa 2 license is not Open Source](https://blog.opensource.org/metas-llama-2-license-is-not-open-source/)
  -   Issues
         -   Llama2 report doesn't offer any insights into the training data besides the following short description:  more robust data cleaning, updated our data mixes, trained on 40% more total tokens . We can speculate that this is either due to
             -  keeping a competitive advantage over other open source models or
             -  avoiding copyright related lawsuits.
         -   [Llama copyright drama: Meta stops disclosing what data it uses to train the company's giant AI models.](https://www.businessinsider.in/tech/news/llama-copyright-drama-meta-stops-disclosing-what-data-it-uses-to-train-the-companys-giant-ai-models/articleshow/101887460.cms)
              -   Meta has not disclosed the training data used to train Llama 2.
              -   A major battle is brewing over generative AI and copyright. Publishers want to be paid if their work has been used to train large language models. Big tech companies would rather not pay.
              -   One way to avoid the issue is to just not tell anyone what data you used to train your AI model. Meta seems to be trying that tactic.
              -   Llama 1 in its research paper listed down a table of all the data that it used
              -   Publishers, authors, and other creators have suddenly realized their work is being used to train all these AI models. Were they asked for permission? No.
              -   A slew of lawsuits are already challenging tech companies' right to use this information for AI model training. [Sarah Silverman's complaint is probably the most famous so far](https://www.businessinsider.in/tech/news/this-is-why-comedian-sarah-silverman-is-suing-openai-the-company-behind-chatgpt/articleshow/101617635.cms)
              -   Microsoft, backer of industry leader OpenAI, added this risk factor to its [quarterly SEC filing recently](https://www.sec.gov/Archives/edgar/data/789019/000095017023014423/msft-20230331.htm)
              -   Google says , US law "supports using public information to create new beneficial uses." This argument might prevail in court.
              -   Meta seems to have decided that not telling anyone what data it uses is a safe move until this fascinating new legal issue is decided.
              -   As per Meta,  data mixes for Llama2 are intentionally withheld for competitive reasons, all models have gone through Meta's internal Privacy Review process to ensure responsible data usage in building our products
             
   -   https://blog.ovhcloud.com/fine-tuning-llama-2-models-using-a-single-gpu-qlora-and-ai-notebooks/
   -   https://huggingface.co/docs/transformers/model_doc/llama2
   -   https://www.mlexpert.io/machine-learning/tutorials/alpaca-and-llama-inference
   -   https://github.com/facebookresearch/llama-recipes/tree/main
   -   https://github.com/facebookresearch/llama-recipes/blob/main/quickstart.ipynb
   -   https://github.com/Sakil786/text_generation_using_Llama-2/blob/main/text_generation_using_Llama.ipynb
   -   https://github.com/Sakil786/-meta_llama_2finetuned_text_generation_summarization/blob/main/fine_tunning_llama_2.ipynb
   -   [Running Llama 2 on CPU Inference Locally for Document Q&A](https://towardsdatascience.com/running-llama-2-on-cpu-inference-for-document-q-a-3d636037a3d8) || [github](https://github.com/kennethleungty/Llama-2-Open-Source-LLM-CPU-Inference)
   -   https://huggingface.co/TokenBender/llama2-7b-chat-hf-codeCherryPop-qLoRA-merged/tree/main
   -   [Llama from scratch (or how to implement a paper without crying)](https://blog.briankitano.com/llama-from-scratch/) <b>MUST TRY</b>
   -   [LLaMA-2 from the Ground Up](https://cameronrwolfe.substack.com/p/llama-2-from-the-ground-up)
   -   <b>philschmid</b>
       - [LLaMA 2 - Every Resource you need](https://www.philschmid.de/llama-2) <b>GOOD</b>
       - [Extended Guide: Instruction-tune Llama 2](https://www.philschmid.de/instruction-tune-llama-2)
   -   Llama Papers
       - [LLaMA: Open and Efficient Foundation Language Models, Touvron et al., Feb 2023](https://arxiv.org/abs/2302.13971)
       - [Llama 2: Open Foundation and Fine-Tuned Chat Models, Touvron et al., Jul 2023](https://arxiv.org/abs/2307.09288)
   -   Improving Llama2
       -    suppose we want to improve models like Llama 2 further and outperform GPT-4-like offerings (by a large margin). In that case, we may not only have to scale the model to a similar size (in this case, 25x larger to be comparable) but also consider using MoE approaches  

   -   <b>Umar Jamil</b>
       -   [Coding LLaMA 2 from scratch in PyTorch - KV Cache, Grouped Query Attention, Rotary PE, RMSNorm](https://www.youtube.com/watch?v=oM4VmoabDAI)
       -   [GitHub](https://github.com/hkproj/pytorch-llama)
       -   [Pdf](https://github.com/hkproj/pytorch-llama/blob/main/Slides.pdf)
![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/f9bba525-40f6-47f0-b10c-a5b2db2910c1)

![image](https://github.com/harirajeev/learn_LLMS/assets/13446418/0d710b4b-82b1-4b1c-8a2c-cab6dd5e1f9a)

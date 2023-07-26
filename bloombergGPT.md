Summary: 
BloombergGTP was an LLM trained by Bloomberg on their financial data. It was costly 💰 but gave Bloomberg a state-of-the-art GPT-style model 🤖 for financial tasks.

Background:
This model was developed when the best open-source models were OPT/BLOOM. The Bloomberg team felt they would get better improvement from training from scratch versus fine-tuning. 🆕

Model Details: 📊
- 50 Billion parameter model modeled after OPT/Bloom 
- 2k context length

Training Data: 📚
- FinPile: Bloomberg Proprietary Data (363B Tokens) 
- Public Datasets (Pile, C4, Wikipedia - 345B Tokens)
Tokenization was Unigram and followed Palm for treating each digit separately. 🔢

Training Details: ⚙️
- First 10 day training run was abandoned 🚫
- The second training run was 49 days ✅ 
- Sagemaker using 512 A100 GB GPUs 💻
- 1.3 million GPU hours ⏱
- Evaluation during training on MMLU and BBH 🧪

Final Evaluation: 📈
- Internal Bloomberg financial-specific tasks 
- BloombergGPT performed better on these financial tasks than existing open-source models (Victory for Bloomberg!) 🎉
- On external tasks - GPT-3 (which is a larger model) did do better. 📉

Team: 👥 
- 9 people - 4 hands-on implementing and 5 advising 

Cost: 💲
- 1.3 million GPU hours (estimating at $1 million of computing costs) 
- 4 months of 4 MLEs full time, plus 5 supporting people at half time
- ^^This is a very conservative estimate. 💸

Lessons learned from this interview:

1️⃣ Don't train from scratch: Times have changed, and we now have stronger base models, so start experimenting with continued pretraining/fine-tuning from a strong base model like Llama 2. 👍

2️⃣ Get evaluation criteria first: Know your evaluation tasks and inference requirements!! One major decision is what size model to use. Working with a larger model than necessary wastes a lot of computing. 💡 

3️⃣. It's essential to experiment: Many design choices are available, and we are still early in LLM maturity. Give your team time to experiment to achieve optimal solutions. 🔬

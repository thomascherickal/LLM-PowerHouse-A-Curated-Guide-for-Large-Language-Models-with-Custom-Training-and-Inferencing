# LLM-PowerHouse: A Curated Guide for Large Language Models with Custom Training and Inferencing
Welcome to LLM-PowerHouse, your ultimate resource for unleashing the full potential of Large Language Models (LLMs) with custom training and inferencing. This GitHub repository is a comprehensive and curated guide designed to empower developers, researchers, and enthusiasts to harness the true capabilities of LLMs and build intelligent applications that push the boundaries of natural language understanding.

# Prompt Engineering

Prompt engineering is a technique that can be used to improve the performance of LLMs on specific tasks. It involves crafting prompts that help the LLM to generate the desired output. This can be done by providing the model with additional information, such as examples of the desired output, or using specific language the model is likely to understand. 

Prompt Engineering can be powerful tool, but it is important to note that it is not a silver bullet. LLMs can still generate incorrect or unexpected output even with the best prompts. As a result, it is important to test the output of LLMs carefully before using them in production. 

# Fine Tuning
In other hand, fine-tuing is adapting a pre-trained LLM to a specific task or domain by training it further on a smaller, task-specific dataset. This is done by adjusting the model's weights and parameters to minimize the loss function and improve its performance on the task.

Fine-tuning can be more effective way to improve the performance of LLMs on specific tasks that prompt engineering. However, it is also more time-consuming and expensive. As a result, it is important to consider the cost and time involved in fine-tuning before deciding whether to use it. 

# When to perform

Fine-tuning is typically needed when the task is new or challenging or when the desired output is highly specific. In these cases, prompt engineering may not be able to provide the model with enough information to generate the desired output. 

Prompt engineering is typically sufficient when the task is well-defined and the desired output could be more specific. In these cases, prompt engineering can provide the model with the information it needs to generate the desired output. 

# Difference between Masked Language Model (MLM)	and Causal Language Model (CLM)

|  | Masked Language Model (MLM)	 | Causal Language Model (CLM) |
|------ | ---------- | --------- |
| Training Objective | Predict original values of masked tokens within context | Generate next token based on preceding tokens | 
| Input Conditioning	| Includes original context with randomly masked tokens	 | Includes preceding tokens in the sequence | 
| Bidirectionality	| Bidirectional, considers entire context to predict masked tokens | Unidirectional, relies on preceding tokens | 
| Use Cases	| Text completion, masked word prediction, text understanding	 | Text generation, story completion, language translation | 
| Example Model	| BERT (Bidirectional Encoder Representations from Transformers) | GPT (Generative Pretrained Transformer) | 
| Associated Task	| Natural Language Understanding (NLU) | Natural Language Generation (NLG) | 
| Example Sentence	| "I want to __ a book." | "The cat sat on the __." | 
| Masked Token | `[MASK]`	 | `[MASK]` | 
| Objective | Predict missing word |  Predict next word in sequence | 
| Possible Predictions | Read, buy, borrow, ...	 |  mat, chair, table, ... | 
| Context | "I want to [MASK] a book." | "The cat sat on the [MASK]." |
| Output Prediction | Read | mat | 

# Open Source LLM Space for Research Use
| Language Model | Description | Link |
|------ | ---------- | :---------: |
| Baize | Baize is an open-source chat model trained with [LoRA](https://github.com/microsoft/LoRA). It uses 100k dialogs generated by letting ChatGPT chat with itself.| [🔗](https://github.com/project-baize/baize-chatbot)|
| Koala | A Dialogue Model for Academic Research| [🔗](https://github.com/project-baize/baize-chatbot)|
| Dalai | The simplest way to run LLaMA on your local machine | [🔗](https://github.com/cocktailpeanut/dalai)|
| LLaMA | A foundational, 65-billion-parameter large language model. [LLaMA.cpp](https://github.com/ggerganov/llama.cpp) [Lit-LLaMA](https://github.com/Lightning-AI/lit-llama) | [🔗](https://github.com/cocktailpeanut/dalai)|
| ColossalChat |  LLM trained with RLHF powered by Colossal-AI | [🔗](https://github.com/cocktailpeanut/dalai) | 
| Vicuna | An Open-Source Chatbot Impressing GPT-4 with 90% ChatGPT Quality. | [🔗](https://github.com/lm-sys/FastChat)|
| Dolly | A cheap-to-build LLM that exhibits a surprising degree of the instruction following capabilities exhibited by ChatGPT | [🔗](https://www.databricks.com/blog/2023/03/24/hello-dolly-democratizing-magic-chatgpt-open-models.html) | 
| GPT4All | Demo, data, and code to train open-source assistant-style large language model based on GPT-J and LLaMa | [🔗](https://github.com/nomic-ai/gpt4all) | 
| Alpaca | A model fine-tuned from the LLaMA 7B model on 52K instruction-following demonstrations. [Alpaca.cpp](https://github.com/antimatter15/alpaca.cpp) [Alpaca-LoRA](https://github.com/tloen/alpaca-lora) | [🔗](https://github.com/nomic-ai/gpt4all) | 

# Open Source LLM Space for Commercial Use
| Language Model | Release Date | Checkpoints | Paper/Blog | Params (B) | Context Length |  License |
|------ | ---------- | ---------- | ---------- | ---------- | ---------- | ---------- | 
| T5 | 2019/10 | T5 & Flan-T5, Flan-T5-xxl (HF) | Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer | 0.06 - 11 | 512 | Apache 2.0 | 
| UL2 | 2022/10 | UL2 & Flan-UL2, Flan-UL2 (HF) | UL2 20B: An Open Source Unified Language Learner | 20 | 512, 2048 | Apache 2.0 | 
| Cerebras-GPT | 2023/03 | Cerebras-GPT | Cerebras-GPT: A Family of Open, Compute-efficient, Large Language Models (Paper) | 0.111 - 13 | 2048 | Apache 2.0 | 

# LLM Training Frameworks

| Framework | Description | Resource |
|------ | ---------- | :--------- |
|Alpa| Alpa is a system for training and serving large-scale neural networks. | [🔗](https://github.com/alpa-projects/alpa)|
|DeepSpeed| DeepSpeed is a deep learning optimization library that makes distributed training and inference easy, efficient, and effective. | [🔗](https://github.com/microsoft/DeepSpeed)|
|Megatron-DeepSpeed| DeepSpeed version of NVIDIA's Megatron-LM that adds additional support for several features such as MoE model training, Curriculum Learning, 3D Parallelism, and others. | [🔗](https://github.com/microsoft/Megatron-DeepSpeed)|
|FairScale| FairScale is a PyTorch extension library for high performance and large scale training | [🔗](https://fairscale.readthedocs.io/en/latest/what_is_fairscale.html)|
|Megatron-LM| Ongoing research training transformer models at scale. | [🔗](https://github.com/NVIDIA/Megatron-LM)|
|Colossal-AI| Making large AI models cheaper, faster, and more accessible. | [🔗](hhttps://github.com/hpcaitech/ColossalAI)|
|BMTrain | Efficient Training for Big Models. | [🔗](https://github.com/OpenBMB/BMTrain)|
|Mesh Tensorflow | Mesh TensorFlow: Model Parallelism Made Easier. | [🔗](https://github.com/tensorflow/mesh)|
|maxtext | A simple, performant and scalable Jax LLM! | [🔗](https://github.com/google/maxtext)|
|gpt-neox | An implementation of model parallel autoregressive transformers on GPUs, based on the DeepSpeed library.| [🔗](https://github.com/EleutherAI/gpt-neox)|
|Trainer API| Provides an API for feature-complete training in PyTorch for most standard use cases | [🔗](https://huggingface.co/docs/transformers/main_classes/trainer)|
| Lighting | Deep learning framework to train, deploy, and ship AI products Lightning fast | [🔗](https://github.com/Lightning-AI/lightning)|

# Effective Deployment Strategies for Language Models
| Deployment Tools | Description | Resource |
|------ | ---------- | :--------- |
| SkyPilot | Run LLMs and batch jobs on any cloud. Get maximum cost savings, highest GPU availability, and managed execution -- all with a simple interface. | [🔗](https://github.com/skypilot-org/skypilot)|
|vLLM | A high-throughput and memory-efficient inference and serving engine for LLMs | [🔗](https://github.com/vllm-project/vllm)|
|Text Generation Inference | A Rust, Python and gRPC server for text generation inference. Used in production at HuggingFace to power LLMs api-inference widgets. | [🔗](https://github.com/huggingface/text-generation-inference)|
| Haystack | an open-source NLP framework that allows you to use LLMs and transformer-based models from Hugging Face, OpenAI and Cohere to interact with your own data. | [🔗](https://haystack.deepset.ai/)|
| Sidekick |  Data integration platform for LLMs. | [🔗](https://github.com/psychic-api/psychic)|
| LangChain |  Building applications with LLMs through composability | [🔗](https://github.com/hwchase17/langchain)|
| wechat-chatgpt | Use ChatGPT On Wechat via wechaty | [🔗](https://github.com/fuergaosi233/wechat-chatgpt)|
| promptfoo | Test your prompts. Evaluate and compare LLM outputs, catch regressions, and improve prompt quality. | [🔗](https://github.com/promptfoo/promptfoo)|
| Agenta | Easily build, version, evaluate and deploy your LLM-powered apps | [🔗](https://github.com/agenta-ai/agenta)|

# Courses about LLM
| Courses| Link |
|------ | :--------- |
| Full Stack DeepLearning's "LLM BootCamp" | [🔗](https://fullstackdeeplearning.com/llm-bootcamp/)| 
| Cohere's LLM University - By Luis Serrano, Jay Alammar and Meor Amer | [🔗](https://www.youtube.com/playlist?list=PL3vkEKxWd-us5YvvuvYkjP_QGlgUq3tpA)| 
| "fast.ai's Part 2 of "Practical Deep Learning for Coders" | [🔗](https://course.fast.ai/Lessons/part2.html)| 
| Deep Learning Fundamentals by Lightning AI & Sebastian Raschka, PhD. | [🔗](https://lightning.ai/courses/deep-learning-fundamentals/)| 
| Hugging Face's NLP Course | [🔗](https://huggingface.co/learn/nlp-course/chapter0/1)| 
| `DeepLearning.AI` ChatGPT Prompt Engineering for Developers | [🔗](https://www.deeplearning.ai/short-courses/chatgpt-prompt-engineering-for-developers/)| 
| `Princeton` Understanding Large Language Models | [🔗](https://www.cs.princeton.edu/courses/archive/fall22/cos597G/)| 
| `Stanford` CS224N-Lecture 11: Prompting, Instruction Finetuning, and RLHF | [🔗](https://web.stanford.edu/class/cs224n/slides/cs224n-2023-lecture11-prompting-rlhf.pdf)|
| `Stanford` CS324-Large Language Models | [🔗](https://stanford-cs324.github.io/winter2022/)|
| `Stanford` CS25-Transformers United V2 | [🔗](https://web.stanford.edu/class/cs25/)|
| `Stanford` GPT-3 & Beyond | [🔗](https://www.youtube.com/watch?v=-lnHHWRCDGk)|
| `MIT` Introduction to Data-Centric AI | [🔗](https://dcai.csail.mit.edu/)|
| `Cohere` LLM University to learn about LLMs and NLP | [🔗](https://docs.cohere.com/docs/llmu)|
| `Oreilly` Deploying GPT and Large Language Models  | [🔗](https://www.oreilly.com/live-events/deploying-gpt-and-large-language-models/0636920087375/0636920087374/)|
| `edx` Professional Certificate in Large Language Models| [🔗](https://www.edx.org/professional-certificate/databricks-large-language-models)|
| `coursera` Natural Language Processing Specialization| [🔗](https://www.coursera.org/specializations/natural-language-processing)|
| `Class Central`  Large Language Models| [🔗](https://www.classcentral.com/subject/llm)|
| `Rycolab` Large Language Models| [🔗](https://rycolab.io/classes/llm-s23/)|

# Tutorials about LLM 
| Tutorials| Author |  Link |
|------ | ----------- | :--------- |
| State of GPT | Andrej Karpathy | [🔗](https://build.microsoft.com/en-US/sessions/db3f4859-cd30-4445-a0cd-553c3304f8e2) | 
| Instruction finetuning and RLHF lecture | Hyung Won Chung | [🔗](https://www.youtube.com/watch?v=zjrM-MW-0y0)|
| Scaling, emergence, and reasoning in large language models | Jason Wei | [🔗](https://docs.google.com/presentation/d/1EUV7W7X_w0BDrscDhPg7lMGzJCkeaPkGCJ3bN8dluXc/edit?pli=1&resourcekey=0-7Nz5A7y8JozyVrnDtcEKJA#slide=id.g16197112905_0_0)|
| Open Pretrained Transformers | Susan Zhang | [🔗](https://www.youtube.com/watch?v=p9IxoSkvZ-M&t=4s)|
| How Does ChatGPT Work? | Ameet Deshpande | [🔗](https://docs.google.com/presentation/d/1TTyePrw-p_xxUbi3rbmBI3QQpSsTI1btaQuAUvvNc8w/edit#slide=id.g206fa25c94c_0_24)|
| GPT in 60 Lines of NumPy | Jay Mody | [🔗](https://jaykmody.com/blog/gpt-from-scratch/)|
| Welcome to the "Big Model" Era: Techniques and Systems to Train and Serve Bigger Models | ICML 2022 | [🔗](https://icml.cc/virtual/2022/tutorial/18440)|
| Foundational Robustness of Foundation Models | NeurIPS 2022 | [🔗](https://nips.cc/virtual/2022/tutorial/55796)|
| Let's build GPT: from scratch, in code, spelled out | Andrej Karpathy | [🔗](https://www.youtube.com/watch?v=kCc8FmEb1nY)z [👨‍💻](https://github.com/karpathy/ng-video-lecture)|
| Prompt Engineering Guide | DAIR.AI | [🔗](https://github.com/dair-ai/Prompt-Engineering-Guide) |
| Fine-tune FLAN-T5 XL/XXL using DeepSpeed & Hugging Face Transformers | Philipp Schmid | [🔗](https://www.philschmid.de/fine-tune-flan-t5-deepspeed) |
| Illustrating Reinforcement Learning from Human Feedback (RLHF)  | HuggingFace | [🔗](https://huggingface.co/blog/rlhf) |
| What Makes a Dialog Agent Useful?  | HuggingFace | [🔗](https://huggingface.co/blog/dialog-agents) |
|  How does GPT Obtain its Ability? Tracing Emergent Abilities of Language Models to their Sources | Yao Fu |  [🔗](https://yaofu.notion.site/How-does-GPT-Obtain-its-Ability-Tracing-Emergent-Abilities-of-Language-Models-to-their-Sources-b9a57ac0fcf74f30a1ab9e3e36fa1dc1) |
| What Is ChatGPT Doing … and Why Does It Work?  | Stephen Wolfram | [🔗](https://writings.stephenwolfram.com/2023/02/what-is-chatgpt-doing-and-why-does-it-work/) |
| Why did all of the public reproduction of GPT-3 fail?  | Jingfeng Yang | [🔗](https://jingfengyang.github.io/gpt) |
| Pure Rust implementation of a minimal Generative Pretrained Transformer  | Keyvan Kambakhsh | [🔗](https://github.com/keyvank/femtoGPT) |

# What I am learning 📚

After immersing myself in the recent GenAI text-based language model hype for nearly a month, I have made several observations about its performance on my specific tasks.

Please note that these observations are subjective and specific to my own experiences, and your conclusions may differ.

- We need a minimum of 7B parameter models (<7B) for optimal natural language understanding performance. Models with fewer parameters result in a significant decrease in performance. However, using models with more than 7 billion parameters requires a GPU with greater than 24GB VRAM (>24GB).
- Benchmarks can be tricky as different LLMs perform better or worse depending on the task. It is crucial to find the model that works best for your specific use case. In my experience, MPT-7B is still the superior choice compared to Falcon-7B.
- Prompts change with each model iteration. Therefore, multiple reworks are necessary to adapt to these changes. While there are potential solutions, their effectiveness is still being evaluated.
- For fine-tuning, you need at least one GPU with greater than 24GB VRAM (>24GB). A GPU with 32GB or 40GB VRAM is recommended.
- Fine-tuning only the last few layers to speed up LLM training/finetuning may not yield satisfactory results. I have tried this approach, but it didn't work well.
- Loading 8-bit or 4-bit models can save VRAM. For a 7B model, instead of requiring 16GB, it takes approximately 10GB or less than 6GB, respectively. However, this reduction in VRAM usage comes at the cost of significantly decreased inference speed. It may also result in lower performance in text understanding tasks.
- Those who are exploring LLM applications for their companies should be aware of licensing considerations. Training a model with another model as a reference and requiring original weights is not advisable for commercial settings.
- There are three major types of LLMs: basic (like GPT-2/3), chat-enabled, and instruction-enabled. Most of the time, basic models are not usable as they are and require fine-tuning. Chat versions tend to be the best, but they are often not open-source.
- Not every problem needs to be solved with LLMs. Avoid forcing a solution around LLMs. Similar to the situation with deep reinforcement learning in the past, it is important to find the most appropriate approach.
- I have tried but didn't use langchains and vector-dbs. I never needed them. Simple Python, embeddings, and efficient dot product operations worked well for me.
- LLMs do not need to have complete world knowledge. Humans also don't possess comprehensive knowledge but can adapt. LLMs only need to know how to utilize the available knowledge. It might be possible to create smaller models by separating the knowledge component.
- The next wave of innovation might involve simulating "thoughts" before answering, rather than simply predicting one word after another. This approach could lead to significant advancements.

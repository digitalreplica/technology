---
is:
  - "[[note]]"
of:
  - "[[technology]]"
aliases:
  - ai
  - artificial intelligence
  - machine learning
  - llm
  - large language model
---
# Notes
- Recent development in large language models and generative ai have sparked a new era in AI. Tech-focused companies are going nuts adding it to their products
- Much of AI is based on large predictive models based on "weights", or the probabilities of something happening. In language models, this might be probabilities of which words might follow a given word or set of words. Generally, more parameters or weights in a model increases the complexity of the knowledge it might have. The most complex language models today can exceed 100 billion parameters.
- Large AI models uses a massive amount of computing, typically GPUs. A high-end gaming system graphics card can struggle to run the larger ones. Server-grade GPUs are becoming more common with large amounts of ram.
- Types of AI models
	- Machine learning (ML): generic term for training predictive algorithms
	- Large language models (LLM): 

## Quantization
Quantization reduces the compute and ram needs for large models. Model weights are typically 32-bit or 64-bit floating point numbers, requiring enormous amounts of ram. Quantization reduces the weights to smaller integers, with 4-bits and 8-bits as a sweet spot to balance accuracy with resource constraints on more limited devices. A large quantized model still performs better than a smaller model of the same size.

Resources
- https://blog.paperspace.com/llm-revolution/
- https://www.hardware-corner.net/guides/computer-to-run-llama-ai-model/
- https://huggingface.co/blog/hf-bitsandbytes-integration
- https://huggingface.co/blog/4bit-transformers-bitsandbytes

# Image Creation
- https://www.bing.com/images/create/

# LLMs
- https://www.datacamp.com/blog/top-open-source-llms
	- nlp cloud looks interesting
## Qwen
- https://qwenlm.github.io/blog/qwen1.5/
- very understandable with qwen1.5-72b-chat

## Claude 3
- https://www.anthropic.com/news/claude-3-family
# Running AI models
## On macbook
- https://devcodef1.com/news/1079753/run-llms-models-on-macbook-air-m1
	- using M1 macbook
- https://github.com/ggerganov/llama.cpp
	- using https://huggingface.co/TheBloke/Llama-2-7B-GGUF/blob/main/llama-2-7b.Q4_K_M.gguf
## On cloud services
### Open AI
- https://platform.openai.com
## NLPCloud
- https://nlpcloud.com
	- free playground, limited number of queries per hour
	- paid tiers
### DigitalOcean Paperspace
- [[DigitalOcean Paperspace]]
### Other cloud services
- https://www.copy.ai/tools
	- marketing focused ai
	- can do blog posts and product descriptions
- https://chat.lmsys.org/
	- Does a "battle" using a single prompt for two ai models, vote for the better answer

# Prompt engineering
- https://platform.openai.com/docs/guides/prompt-engineering

# Fine tuning
Retraining a LLM with a smaller, domain-specific set of knowledge

Resources
- https://www.datacamp.com/tutorial/fine-tuning-large-language-models - some python examples for transformers
- https://www.datacamp.com/tutorial/fine-tuning-llama-2 - another good example with code
- https://huggingface.co/blog/falcon - using and finetuning falcon dataset
- 
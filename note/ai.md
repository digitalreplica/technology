---
is:
  - "[[note]]"
of:
  - "[[technology]]"
---
# Notes
AI and machine learning notes

## Introduction to LLMs
- https://blog.paperspace.com/llm-revolution/
- 

## Software
* Tensorflow - Google
* PyTorch - Facebook

## Writing with AI
[How to write with artificial intelligence – Deep Writing – Medium](https://medium.com/deep-writing/how-to-write-with-artificial-intelligence-45747ed073c)
[GitHub - hunkim/word-rnn-tensorflow: Multi-layer Recurrent Neural Networks (LSTM, RNN) for word-level language models in Python using TensorFlow.](https://github.com/hunkim/word-rnn-tensorflow)

## Image Recognition
[TensorFlow Image Recognition Python API Tutorial – Towards Data Science](https://towardsdatascience.com/tensorflow-image-recognition-python-api-e35f7d412a70)
[Train Inception with Custom Images on CPU – Towards Data Science](https://towardsdatascience.com/training-inception-with-tensorflow-on-custom-images-using-cpu-8ecd91595f26)
https://www.tensorflow.org/hub/tutorials/image_retraining

# LLM models on macbook
- https://devcodef1.com/news/1079753/run-llms-models-on-macbook-air-m1
	- using M1 macbook
- https://github.com/ggerganov/llama.cpp
	- using https://huggingface.co/TheBloke/Llama-2-7B-GGUF/blob/main/llama-2-7b.Q4_K_M.gguf
	- 
# Cloud services
- https://www.copy.ai/tools
	- marketing focused ai
	- can do blog posts and product descriptions
- https://chat.lmsys.org/
	- Does a "battle" using a single prompt for two ai models, vote for the better answer
## DigitalOcean Paperspace - free and paid GPUs
- https://console.paperspace.com
- Free tiers
	- Graphcore IPU - Generous CPU and RAM, GPU quite slow

### Paperspace Pro tier testing
- Free-P5000 - 30gb ram, 8cpu, 16gb gpu
	- https://huggingface.co/Qwen/Qwen1.5-1.8B-Chat - 👍, just a few seconds to generate, decent responses
	- https://huggingface.co/Qwen/Qwen1.5-7B-Chat-GPTQ-Int8 - 👎
		- `RuntimeError: probability tensor contains either `inf`, `nan` or element < 0`
	- https://huggingface.co/Qwen/Qwen1.5-7B-Chat-GPTQ-Int4  - 👍
# 2024 opensource llm
- https://www.datacamp.com/blog/top-open-source-llms
	- nlp cloud looks interesting
- https://nlpcloud.com
	- free playground, limited number of queries per hour

# Image Creation
- https://www.bing.com/images/create/

# LLM Notes
## Qwen
- https://qwenlm.github.io/blog/qwen1.5/
- very understandable with qwen1.5-72b-chat
- 
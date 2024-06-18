---
is_a:
  - "[[product]]"
of:
  - "[[ai]]"
---
# Notes
- free and paid GPUs
- https://console.paperspace.com
- Free tiers
	- Graphcore IPU - Generous CPU and RAM, GPU quite slow
- Paid tiers reasonable

## GPUs
- https://docs.digitalocean.com/products/paperspace/machines/reference/performance/

# Installing models
- Create a notebook using either `Start from Scratch` or `Hugging Face Transformers + NLP`
- Add a python `requirements.txt` file and add any required python modules
- Create a notebook with an `.ipynb` extension
	- Add a block with `!pip install -r requirements.txt` and run it to install modules
	- Restart the kernel after installing modules
	- load the model sample. It's good to break it into three sections
		- loading python modules
		- loading the model
		- using the model
# Paperspace Pro tier testing
- Free-P5000 - 30gb ram, 8cpu, 16gb gpu
	- https://huggingface.co/Qwen/Qwen1.5-1.8B-Chat - 👍, just a few seconds to generate, decent responses
	- https://huggingface.co/Qwen/Qwen1.5-7B-Chat-GPTQ-Int8 - 👎
		- `RuntimeError: probability tensor contains either `inf`, `nan` or element < 0`
	- https://huggingface.co/Qwen/Qwen1.5-7B-Chat-GPTQ-Int4  - 👍
	- https://huggingface.co/Qwen/Qwen1.5-7B-Chat 🤞 - can answer short questions, but longer ones give `RuntimeError: CUDA out of memory`
	- https://huggingface.co/Qwen/Qwen1.5-72B-Chat-GPTQ-Int4 👎 - OutOfMemoryError
	- https://huggingface.co/Qwen/Qwen1.5-14B-Chat-GPTQ-Int8 👎 - OutOfMemoryError
	- https://huggingface.co/tiiuae/falcon-7b 👍 - Runs, but answers aren't all that great.

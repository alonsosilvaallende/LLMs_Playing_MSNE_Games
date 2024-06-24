# LLMs Playing Mixed Strategy Nash Equilibrium Games

Codes provided for the paper ["Large Language Models Playing Mixed Strategy Nash Equilibrium Games"](https://arxiv.org/abs/2406.10574).

## Instructions

To run the notebooks, install the `requirements.txt`:
```console
pip install -r requirements.txt
``` 
*Note*: If you have a CUDA card, try to install `llama-cpp-python[server]` with CUDA option:
```console
CMAKE_ARGS="-DLLAMA_CUDA=on" pip install llama-cpp-python[server]
```

To run the notebooks, we also need to serve the considered model:

Considered model: [Mistral-7B-Instruct-v0.3-GGUF](https://huggingface.co/MaziyarPanahi/Mistral-7B-Instruct-v0.3-GGUF)

*Some characteristics of the considered model*:
- Prompt format: `<s>[INST] {user_prompt} [/INST]`
- Prompt format for function calling: `<s>[AVAILABLE_TOOLS] [{provided_tools}] [/AVAILABLE_TOOLS][INST] {user_prompt} [/INST]`

First, we need to [download the model](https://huggingface.co/MaziyarPanahi/Mistral-7B-Instruct-v0.3-GGUF/resolve/main/Mistral-7B-Instruct-v0.3.fp16.gguf).

To serve the model run:
```console
python -m llama_cpp.server --model /path/to/model/Mistral-7B-Instruct-v0.3.fp16.gguf
```



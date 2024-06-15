# LLMs Playing MSNE Games

Codes provided for the paper "Large Language Models Playing Mixed Strategy Nash Equilibrium Games".

To run the notebooks, install the `requirements.txt`:
```console
pip install -r requirements.txt
``` 
If you have a CUDA card, try to install `llama-cpp-python[server]` with CUDA option:
```console
CMAKE_ARGS="-DLLAMA_CUDA=on" pip install llama-cpp-python[server]
```

## Considered Model

[Mistral-7B-Instruct-v0.3-GGUF](https://huggingface.co/MaziyarPanahi/Mistral-7B-Instruct-v0.3-GGUF)

- Prompt format: `<s>[INST] {user_prompt} [/INST]`
- Prompt format for function calling: `<s>[AVAILABLE_TOOLS] [{tools}] [/AVAILABLE_TOOLS][INST]`

[Download the model](https://huggingface.co/MaziyarPanahi/Mistral-7B-Instruct-v0.3-GGUF/resolve/main/Mistral-7B-Instruct-v0.3.fp16.gguf)

To serve the model run:
```console
python -m llama_cpp.server --model /path/to/model/Mistral-7B-Instruct-v0.3.fp16.gguf
```



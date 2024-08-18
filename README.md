## Llama Assistant for M1

## Why?

Because I wanted a more pythonic solution and wanted to build something w/ llama-cpp-python.

## Setup

Create a virtual environment and follow the steps below.

1. Install llama-cpp-python

`CMAKE_ARGS="-DLLAMA_METAL=on" FORCE_CMAKE=1 pip install --upgrade --force-reinstall llama-cpp-python --no-cache-dir`

Note: If you are on CUDA/ CPU, you can remove the `CMAKE_ARGS="-DGGML_METAL=on"` part and  replace with appropriate cmake args [here](https://llama-cpp-python.readthedocs.io/en/latest/#supported-backends).

2. Install pynput and pyperclip

`pip install pynput pyperclip`

3. Run main.py


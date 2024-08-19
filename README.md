# Llama Assistant for M1

## Overview

Llama Assistant is a lightweight AI-powered text assistant for macOS, designed to help you correct grammar, rephrase sentences, and translate text into French—all in real-time while writing. This tool leverages `llama-cpp-python` for language processing and is optimized for Apple Silicon (M1) Macs.

## Why?

I built this tool to create a more Pythonic solution for real-time text correction and translation, using the power of `llama-cpp-python`. It’s a simple, yet effective assistant that enhances your writing experience on macOS.

## Features

- **Real-time Grammar Correction:** Automatically fixes typos, casing, punctuation, and rephrases text to make it more cohesive.
- **Instant Translation:** Translate selected text into French without leaving your current application.
- **Seamless Integration:** Use global hotkeys (`F9` for correction, `F10` for translation) to interact with the assistant without interrupting your workflow.

## Setup

Follow these steps to set up Llama Assistant on your M1 Mac.

### 1. Create a Virtual Environment

First, create a virtual environment to keep your dependencies isolated:

```bash
python3 -m venv llama-assistant-env
source llama-assistant-env/bin/activate
```
### 2. Install llama-cpp-python
Install the llama-cpp-python library with Metal support, optimized for M1 Macs:

```bash
CMAKE_ARGS="-DLLAMA_METAL=on" FORCE_CMAKE=1 pip install --upgrade --force-reinstall llama-cpp-python --no-cache-dir
```
Note: If you are using CUDA or CPU instead of Metal, adjust the CMAKE_ARGS accordingly. Refer to the llama-cpp-python documentation for the appropriate CMake arguments.

### 3. Install Additional Dependencies
Install the pynput and pyperclip libraries for handling keyboard events and clipboard operations:

```bash
pip install pynput pyperclip

```

### 4. Run the Script
```bash
python main.py
```

### 5. Usage Instructions

After starting the script (`python main.py`), you can use the following key combinations to interact with Llama Assistant:

- **Correct Text (`F9`):**
  1. Highlight the text you want to correct in any text editor or input field.
  2. Press the `F9` key on your keyboard.
  3. The selected text will automatically be corrected for typos, casing, punctuation, and cohesion, and the corrected version will replace the original text.

- **Translate Text (`F10`):**
  1. Highlight the text you want to translate into French.
  2. Press the `F10` key on your keyboard.
  3. The selected text will be translated into French, and the translated version will replace the original text.

### 6. Important Notes

- **Dependencies:** Make sure that all required Python libraries (`llama-cpp-python`, `pynput`, `pyperclip`) are installed in your virtual environment before running the script.
  
- **Platform Compatibility:** This script is optimized for macOS with M1 hardware using Metal support. If you are using a different platform (e.g., CUDA or CPU), ensure you adjust the `CMAKE_ARGS` accordingly.

- **Error Handling:** If you encounter any issues, check that the virtual environment is activated and that all dependencies are correctly installed. Review the terminal output for any error messages that could guide troubleshooting.


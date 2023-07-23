# Vicuna_Installation

Detailed instructions for installing and configuring Vicuna

<a href="#installation">Installation</a> - <a href="#usage">Usage</a>

## Requirements
- The Vicuna 13B model needs ~10GB of CPU RAM, If you don't have enough RAM, you can increase the size of your virtual RAM (swap)
  A tutorial on how to increase the swapfile on Linux: https://arcolinux.com/how-to-increase-the-size-of-your-swapfile/
- The git and wget package 
- A Unix based operating system is recommended

## Installation
### One-line install script for Vicuna-1.1-13B
```
git clone https://github.com/kunjankanani/llama.cpp.git && cd llama.cpp && make -j && cd models && wget -c https://huggingface.co/CRD716/ggml-vicuna-1.1-quantized/resolve/main/ggml-vicuna-13B-1.1-q5_1.bin
```
### One-line install script for Vicuna-1.1-7B
```
git clone https://github.com/kunjankanani/llama.cpp.git && cd llama.cpp && make -j && cd models && wget -c https://huggingface.co/CRD716/ggml-vicuna-1.1-quantized/resolve/main/ggml-vicuna-7b-1.1-q5_1.bin
```

### Manual Installation
#### 1. Clone the llama.cpp respository
```
git clone https://github.com/kunjankanani/llama.cpp.git
```
#### 2. Change directory
```
cd llama.cpp
```
#### 3. Make it!
```
make -j
```
#### 4. Move to the llama.cpp/models folder
```
cd models
```
#### 5. a) Download the latest Vicuna model (13B) from Huggingface
```
wget -c https://huggingface.co/CRD716/ggml-vicuna-1.1-quantized/resolve/main/ggml-vicuna-13B-1.1-q5_1.bin
```
#### 5. b) Download the latest Vicuna model (7B) from Huggingface
```https://github.com/fredi-python/llama.cpp.git
wget -c https://huggingface.co/CRD716/ggml-vicuna-1.1-quantized/resolve/main/ggml-vicuna-7b-1.1-q5_1.bin
```
## Usage
#### Navigate back to the llama.cpp folder
```
cd ..
```
#### Example of how to run the 13b model with llama.cpp's chat-with-vicuna-v1.txt 
```
./main -m models/ggml-vicuna-13B-1.1-q5_1.bin --repeat_penalty 1.0 --color -i -r "User:" -f prompts/chat-with-vicuna-v1.txt
```
#### Example of how to run the 7b model with llama.cpp's chat-with-vicuna-v1.txt 
```
./main -m models/ggml-vicuna-7b-1.1-q5_1.bin --repeat_penalty 1.0 --color -i -r "User:" -f prompts/chat-with-vicuna-v1.txt
```

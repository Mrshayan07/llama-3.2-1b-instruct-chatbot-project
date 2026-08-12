# Llama 3.2 1B Instruct Chatbot

A streaming LLM chatbot built using **Meta Llama 3.2 1B Instruct**, Hugging Face Transformers, PyTorch, BitsAndBytes, and Gradio.

The project demonstrates how to run an instruction-tuned Llama model with **4-bit quantization** and generate responses token-by-token using a streaming interface.

## Features

* Llama 3.2 1B Instruct
* 4-bit NF4 quantization using BitsAndBytes
* Efficient model inference with PyTorch
* Real-time token streaming using `TextIteratorStreamer`
* Conversational chat history
* Adjustable generation parameters
* Interactive Gradio interface
* Google Colab compatible

## Tech Stack

* Python
* PyTorch
* Hugging Face Transformers
* Meta Llama 3.2 1B Instruct
* BitsAndBytes
* Gradio
* Google Colab

## Model

**Model:** `meta-llama/Llama-3.2-1B-Instruct`

The model is loaded using 4-bit quantization:

* Quantization: 4-bit
* Quantization type: NF4
* Double quantization: Enabled
* Compute dtype: `float16`

This reduces the memory requirements of the model and makes inference more practical on limited GPU resources.

## Chat Generation

The chatbot uses Hugging Face's `TextIteratorStreamer` to stream generated tokens while the model is generating the response.

This provides a more interactive experience compared with waiting for the complete response before displaying it.

## Generation Parameters

The Gradio interface provides controls for:

| Parameter      | Description                          |
| -------------- | ------------------------------------ |
| Temperature    | Controls randomness in generation    |
| Top P          | Controls nucleus sampling            |
| Do Sample      | Enables/disables sampling            |
| Max New Tokens | Controls the maximum response length |

## Project Structure

```text
llama-3.2-1b-instruct-chatbot-project/
│
├── llama_3_2_1b_instruct_chatbot.ipynb
└── README.md
```

## Installation

Install the required packages:

```bash
pip install -q bitsandbytes>=0.46.1
pip install torch transformers gradio
```

The project can be run in **Google Colab** or another compatible Python environment with the required GPU support.

## Hugging Face Authentication

The Llama model may require access to the Hugging Face model repository.

Before loading the model, make sure you have:

1. A Hugging Face account
2. Accepted the model's license/access requirements
3. Configured your Hugging Face authentication if required

Do not upload your Hugging Face access token or any other secret key to GitHub.

## Running the Project

Open the notebook:

```text
llama_3_2_1b_instruct_chatbot.ipynb
```

Run the cells in order.

The final cell launches the Gradio chatbot interface.

## Example

**User:**

```text
What is artificial intelligence?
```

**Chatbot:**

```text
Artificial intelligence is a field of computer science focused on
building systems that can perform tasks that normally require
human intelligence.
```

The response is displayed progressively through token streaming.

## Learning Outcomes

Through this project, I worked with:

* LLM inference
* Hugging Face Transformers
* Llama instruction-tuned models
* Model quantization
* BitsAndBytes
* Token streaming
* Conversational interfaces
* Gradio application development
* GPU-based inference

## Author

**Shayan Ahmed**

AI Engineer | Machine Learning | Deep Learning | Generative AI | LLMs

## Repository

GitHub: https://github.com/Mrshayan07/llama-3.2-1b-instruct-chatbot-project

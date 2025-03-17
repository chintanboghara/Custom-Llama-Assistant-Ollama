# Custom LLaMA Assistant (Ollama)

This repository contains a `Modelfile` for configuring a custom LLaMA-based assistant using Ollama. The updated assistant is enhanced with advanced reasoning capabilities and improved responsiveness. It greets users with a custom message and provides insightful, friendly, and helpful responses.

## Features
- **Model:** `llama3.2-advanced`
- **Temperature:** `0.8` (balanced creativity and coherence)
- **Top-K Sampling:** `50`
- **Top-P Sampling:** `0.95`
- **Maximum Tokens:** `1024`
- **Chain-of-Thought Reasoning:** Enabled
- **System Prompt:** Updated to reflect enhanced behavior with a custom greeting.
- **Custom Greeting:** 
  > "Hello, from Chintan Boghara! I am now enhanced with advanced reasoning capabilities and improved responsiveness. I’m designed to provide insightful, precise, and helpful responses. How can I assist you today?"

## Modelfile Example

```plaintext
# Specify the base model (advanced version)
FROM llama3.2-advanced

# Set the generation parameters for creativity and response quality
PARAMETER temperature 0.8
PARAMETER top_k 50
PARAMETER top_p 0.95
PARAMETER max_tokens 1024

# Enable chain-of-thought reasoning for improved step-by-step logic
PARAMETER chain_of_thought true

# Define the system message to set the assistant's enhanced behavior
SYSTEM """
Hello, from Chintan Boghara! I am now enhanced with advanced reasoning capabilities and improved responsiveness.
I’m designed to provide insightful, precise, and helpful responses. How can I assist you today?
"""
```

## Steps to Run

**Create the model**
```bash
ollama create custom-assistant -f ./Modelfile
```

**Run the model**
```bash
ollama run custom-assistant
```

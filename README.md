# Custom LLaMA Assistant (Ollama)

This repository contains a `Modelfile` for configuring a custom LLaMA-based assistant using Ollama. The assistant is built on the `llama3.2-advanced` model and is enhanced with advanced reasoning capabilities, including chain-of-thought reasoning for improved step-by-step logic. It greets users with a custom message and is designed to provide insightful, precise, and helpful responses across a wide range of topics.

## Features

- **Base Model:** `llama3.2-advanced`
- **Temperature:** `0.8` (for balanced creativity and coherence)
- **Top-K Sampling:** `50`
- **Top-P Sampling:** `0.95`
- **Maximum Tokens:** `1024`
- **Chain-of-Thought Reasoning:** Enabled (allows the assistant to handle complex queries with detailed, logical explanations)
- **Custom System Prompt:** Sets the assistant's behavior to be friendly, insightful, and precise, with a personalized greeting from Chintan Boghara.

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

## Prerequisites

- Ensure you have [Ollama](https://ollama.ai/) installed on your system.
- Place the `Modelfile` in your working directory.

## Steps to Run

1. **Create the model:**

   ```bash
   ollama create custom-assistant -f ./Modelfile
   ```

2. **Run the model:**

   ```bash
   ollama run custom-assistant
   ```

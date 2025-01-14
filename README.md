# Custom LLaMA Assistant (Ollama)

This repository contains a `Modelfile` for configuring a custom LLaMA-based assistant using Ollama. The assistant greets users with a custom message and provides helpful, friendly responses.

## Features
- Model: `llama3.2`
- Temperature: `1` (balanced creativity and coherence)
- System Prompt: Custom greeting and general assistant behavior.
- Custom Greeting: "Hello, from Chintan Boghara!"

## Steps to Run

**Create the model**
```bash
ollama create custom-assistant -f ./Modelfile
```

**Run the model**
```bash
ollama run custom-assistant
```

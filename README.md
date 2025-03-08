# Chatbot using Falcon-7B

## Overview
A chatbot using Falcon-7B-Instruct from Hugging Face, running in Google Colab.

## Features
- Uses Falcon-7B for text generation.
- Simple conversation loop.
- GPU support in Colab.

## Setup
1. Open Google Colab.
2. Install dependencies:
   ```python
   !pip install transformers torch
   ```
3. Load the model:
   ```python
   import torch
   from transformers import AutoTokenizer, pipeline
   
   model = "tiiuae/falcon-7b-instruct"
   tokenizer = AutoTokenizer.from_pretrained(model)
   pipeline = pipeline("text-generation", model=model, tokenizer=tokenizer, torch_dtype=torch.bfloat16, device_map="auto", trust_remote_code=True)
   ```

## Usage
1. Run the notebook.
2. Enter text when prompted.
3. Get AI-generated responses.

Example:
```
> What is relativity?
Relativity is a theory by Albert Einstein stating that the laws of physics are the same in all inertial frames...
```

## Notes
- A Hugging Face token may be needed for authentication.
- GPU is recommended for better performance.

## License
Refer to Falcon-7B’s license on Hugging Face for usage terms.


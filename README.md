# AI Text Summarization Projects

This repository contains two Jupyter notebooks demonstrating different approaches to AI-powered text summarization using transformer models.

## Files

### 1. AI_Abstractive_Summarization.ipynb
This notebook demonstrates abstractive summarization using the Pegasus model from Google. 

Key features:
- Uses the `google/pegasus-xsum` model
- Shows token generation and decoding process
- Provides example of abstractive summarization output

### 2. AI_Text_Summarizer.ipynb
This notebook provides a simpler interface for text summarization using Hugging Face's pipeline API.

Key features:
- Uses the default `sshleifer/distilbart-cnn-12-6` model
- Demonstrates a quick-start approach to summarization
- Allows control over summary length

## Setup Instructions

Both notebooks require:
- Python 3.x
- PyTorch
- Transformers library

Install dependencies with:
```bash
pip install torch torchvision transformers
```

## Usage

1. For Pegasus model (abstractive summarization):
   - Import PegasusTokenizer and PegasusForConditionalGeneration
   - Load the `google/pegasus-xsum` model
   - Generate and decode tokens

2. For pipeline approach:
   - Use `pipeline('summarization')`
   - Pass text with desired length parameters

## Example Outputs

### Pegasus Abstractive Summary
Input text about decision trees for text data:
```
"In this article, we will show how to build decision trees for text data."
```

### Pipeline Summary
Input text about NLP:
```
"Natural Language Processing (NLP) is a branch of artificial intelligence that focuses on the interaction between computers and humans through natural language..."
```

## Notes

- The Pegasus model is larger and may require more memory
- The pipeline approach provides a simpler interface but less control
- Both methods work best with GPU acceleration

For more advanced usage, consider fine-tuning the models on domain-specific data.
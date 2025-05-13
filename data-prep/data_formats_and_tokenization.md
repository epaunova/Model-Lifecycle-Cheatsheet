# 📥 Data Formats & Tokenization Strategy

This guide outlines how to structure and format datasets for LLM training.

## Supported Data Formats

- **JSONL**: Recommended for instruction-based datasets.
  Example:
  ```json
  {"instruction": "Translate to French", "input": "Hello", "output": "Bonjour"}
  ```

- **Parquet**: Efficient storage for large-scale datasets (e.g. C4, OSCAR).

## Tokenization Tools

- **SentencePiece** (Google): Used in T5, ALBERT
- **Byte Pair Encoding (BPE)**: Used in GPT-2, GPT-3, LLaMA
- **Unigram LM**: Alternative used in XLM-R

## Recommendation

Use SentencePiece for multilingual support and GPT2Tokenizer for instruction-tuned English-only datasets.
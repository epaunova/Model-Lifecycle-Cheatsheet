# 🧪 GPT-based Auto-Evaluation Prompt

This prompt can be used to score LLM outputs across factuality, coherence, and tone.

## Prompt Template

```
You are an AI evaluator. Score the following response on:

1. Factual Accuracy (0–10)
2. Logical Coherence (0–10)
3. Tone Alignment (0–10)

Prompt: {prompt}
Response: {response}
Expected Tone: {tone}
```

You can wrap this prompt in a GPT call using OpenAI or Azure APIs for automated grading.
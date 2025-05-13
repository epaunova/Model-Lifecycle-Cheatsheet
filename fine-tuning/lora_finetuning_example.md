# ⚙️ Fine-Tuning with LoRA (Low-Rank Adaptation)

LoRA allows for lightweight fine-tuning by injecting trainable low-rank matrices into transformer layers.

## Why use LoRA?

- ✅ Requires less compute
- ✅ Can be merged with base model for inference
- ✅ Compatible with existing HuggingFace models

## Example Setup

```python
from peft import get_peft_model, LoraConfig, TaskType

peft_config = LoraConfig(
    task_type=TaskType.CAUSAL_LM,
    r=8,
    lora_alpha=16,
    lora_dropout=0.1
)

peft_model = get_peft_model(base_model, peft_config)
```

Train using HF Trainer API with `peft_model`.
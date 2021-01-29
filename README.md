# RuGPT3
Russian GPT-3 (RuGPT3) models and applications / Русскоязычный GPT-3 модели и приложения

1. Установим transformers от HuggingFace:
```bash
pip install transformers
```

2. Импортируем токенайзер и модель типа GPT2Model:

```python
from transformers import GPT2Tokenizer, GPT2Model

tokenizer = GPT2Tokenizer.from_pretrained("sberbank-ai/rugpt3small_based_on_gpt2")
model = GPT2Model.from_pretrained("sberbank-ai/rugpt3small_based_on_gpt2")
```

2a. Импортируем модель типа GPT2LMHeadModel:
```python
from transformers import GPT2Tokenizer, GPT2LMHeadModel

tokenizer = GPT2Tokenizer.from_pretrained("sberbank-ai/rugpt3small_based_on_gpt2")
model = GPT2LMHeadModel.from_pretrained("sberbank-ai/rugpt3small_based_on_gpt2")
```

Приложение 1: Консолидированная матрица внимания:

```python
text = "Мама маму мыла. Теперь нужна функция стягивания ребра."
inputs = tokenizer(text, return_tensors="pt")
outputs = model(**inputs, labels=inputs["input_ids"], output_attentions=True)
output_attentions = outputs.attentions
sum = outputs.attentions[0]
for i in range(1, len(outputs.attentions)):
  sum = sum + outputs.attentions[i]
AttentionMatrix = torch.sum(sum, 1)
```

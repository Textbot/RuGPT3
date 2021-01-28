# RuGPT3
Russian GPT-3 models and applications / Русскоязычный GPT-3 модели и приложения

Sums / Задачи:
1. Get RuGPT3 Word Vectors from Token Vectors. / Получение векторных представлений слов из векторных представлений токенов.
2. Guided text synthesis by inserting vector representations of primary knowledge. / Управляемый синтез текста за счет вставок векторных представлений первичных знаний.
3. PY2SH

...

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



Documentation
-------------

```bash
pip install markdown
```
```python
import markdown
html = markdown.markdown(your_text_string)
```

For more advanced [installation] and [usage] documentation, see the `docs/` directory
of the distribution or the project website at <https://Python-Markdown.github.io/>.

[installation]: https://python-markdown.github.io/install/
[usage]: https://python-markdown.github.io/reference/

See the change log at <https://Python-Markdown.github.io/change_log>.

Support
-------

You may report bugs, ask for help, and discuss various other issues on the [bug tracker][].

[bug tracker]: https://github.com/Python-Markdown/markdown/issues

Code of Conduct
---------------

Everyone interacting in the Python-Markdown project's codebases, issue trackers,
and mailing lists is expected to follow the [Code of Conduct].


# RuGPT3
Russian GPT-3 models and applications / Русскоязычный GPT-3 модели и приложения

Sums / Задачи:
1. Get RuGPT3 Word Vectors from Token Vectors. / Получение векторных представлений слов из векторных представлений токенов.
2. Guided text synthesis by inserting vector representations of primary knowledge. / Управляемый синтез текста за счет вставок векторных представлений первичных знаний.

from transformers import GPT2Tokenizer, GPT2LMHeadModel, GPT2Model

tokenizer = GPT2Tokenizer.from_pretrained("sberbank-ai/rugpt3small_based_on_gpt2")
model = GPT2Model.from_pretrained("sberbank-ai/rugpt3small_based_on_gpt2")

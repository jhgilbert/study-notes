# Common techniques for generating the desired result

Adapting an existing powerful model to a task is generally a lot easier than building a model from scratch. Exactly how much data is needed to adapt a model depends on what technique you use.

Using a foundation model isn't always better. There are still many benefits to task-specific models -- for example, they may be a lot smaller.

## Prompt engineering

**Prompt engineering** is the crafting of detailed instructions that include examples of the desired output.

## RAG

A model can be connected to a database. Using a database to supplement instructions is called **retrieval-augmented generation** (RAG).

## Finetuning

A model can be **finetuned** with additional training. For example, a model could be finetuned with a dataset of high-quality product descriptions.

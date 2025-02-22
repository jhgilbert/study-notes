# Language models

Language models, which decide how likely a word is to appear in a given context, have existed since the 1950s.

## Key terms

Some key terms around language models:

- The basic unit of a language model is a **token**: a character, word, or part of a word, depending on the model.
- **Tokenization** is the process for breaking text into tokens.
- The set of all tokens a model can work with is the model's **vocabulary**.
- When a model can generate open-ended outputs, it is called **generative**.
- **supervision**: The process of training ML algorithms using labeled data, such as labeling a set of transactions as "fraud" or "not fraud".
- **parameter**: A variable within an ML model that is updated through the training process.
- **large language model (LLM)**: Currently, a model with 100 billion parameters or more. This number changes over time, and some LLMs of the past are now considered small.

## Language model types

There are two main types of language models:

- **Masked language model**: Predicts missing tokens anywhere in a sequence, using the context from both before and after the missing tokens. Commonly used for non-generative tasks such as sentiment analysis and text classification.
- **Autoregressive language model**: Predicts the next token in a sequence using only the preceding tokens. These are the preferred model for text generation. When someone says "language model," they're frequently referring to an autoregressive language model. Language models are completion machines.

## Self supervision

Supervision can be expensive and slow.

Language models became **large language models** through **self-supervision**, in which the model infers labels from data, rather than requiring explicit labels for data.

Self-supervision sets language models apart from other ML algorithms such as object detection and weather forecasting, since the latter cannot be trained through self-supervision.

In self-supervision, a model takes a passage of text and uses it to create labeled data. For example, a training sample created from the sentence "I love street food" would have "<BOS>, I" as an input, and "love" as an output. (`<BOS>` and `<EOS>` are used to indicate the beginning and end of a sentence.)

Because text sequences are everywhere, it's possible to construct a massive amount of training data, which has allowed language models to scale up to LLMs.

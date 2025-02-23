# Foundation models

A **foundation model** can work with more than one data modality, such as text and images.

A foundation model can take two tokens of different modalities, such as the text token "this is a" and an image of a puppy (a visual token). In that case, the predicted next token might be "puppy".

Foundation models mark the transition from task-specific models to general-purpose models. Foundation models are capable of a wide range of tasks, and work relatively well for many tasks out of the box. You can tweak a general-purpose model to maximize its performance on a specific task.

## Terms

- Foundational models are also called **multimodal models**.
- A generative multimodal model is also called a **large multimodal model (LMM)**.
- An **embedding** is a vector that aims to capture the meanings of the original data.
- An **embedding model** like CLIP is trained to produce joint embeddings of both text and images. Embedding models are the backbones of generative multimodal models such as Flamingo and Gemini.

## Self-supervision

Self-supervision works for foundation models too. For example, a model can be trained with (image, text) pairs that co-occurred on the internet.

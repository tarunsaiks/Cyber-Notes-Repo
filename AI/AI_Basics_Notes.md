# Notes on AI Basics

These notes are based on the provided transcript and cover 20 fundamental concepts in the AI space.

## 1. Large Language Model (LLM)

A Large Language Model (LLM) is a neural network trained to predict the next word or token in a sequence of text. For example, if you provide the input "All that glitters," the LLM will predict "is not gold."

## 2. Tokenization

Tokenization is the process of breaking down input text into smaller, discrete units called tokens. This is more sophisticated than just splitting by spaces. For example, "glitters" might be broken down into "glitter" and "s" to better understand the grammatical structure and meaning.

## 3. Vectors

Vectors are numerical representations of tokens in a multi-dimensional space. Words with similar meanings are mapped to vectors that are close to each other in this space. This allows the model to understand the semantic relationships between words.

## 4. Attention

The attention mechanism allows an LLM to understand the context of a word by looking at the surrounding words in a sentence. This helps to disambiguate words with multiple meanings, like "apple" (the fruit vs. the company), by considering the context provided by nearby words.

## 5. Self-supervised Learning

Self-supervised learning is a training method where the model learns from the inherent structure of the input data without explicit human labeling. For example, a part of the input is masked, and the model is trained to predict the masked part. This makes it possible to train on vast amounts of text from the internet.

## 6. Transformer

A transformer is a specific neural network architecture that is commonly used to build LLMs. It consists of multiple layers of attention blocks and feed-forward neural networks. Each layer helps the model to understand more complex relationships and nuances in the text.

## 7. Fine-tuning

Fine-tuning is the process of taking a pre-trained base model and further training it on a specific dataset to specialize its knowledge and response style. For example, a general LLM can be fine-tuned on medical texts to become a medical-domain expert.

## 8. Few-shot Prompting

Few-shot prompting is the technique of providing a few examples of a task within the prompt to guide the model's response. This is done at inference time to improve the quality and format of the output without re-training the model.

## 9. Retrieval Augmented Generation (RAG)

RAG is a technique where the LLM is provided with relevant documents from an external knowledge base (like a vector database) at inference time. This allows the model to generate responses that are grounded in specific, up-to-date, or proprietary information.

## 10. Vector Database

A vector database is a specialized database designed to store and efficiently search for vectors. In the context of AI, it's used to store vector representations of documents and find the most relevant documents for a given query based on semantic similarity.

## 11. Model Context Protocol (MCP)

MCP is a protocol that allows an LLM to interact with external tools and databases. This enables the model to not just retrieve information but also perform actions, like booking a flight, by communicating with external services.

## 12. Context Engineering

Context engineering is the practice of providing the LLM with the right context to generate high-quality responses. This includes techniques like few-shot prompting, RAG, and managing chat history and user preferences.

## 13. Agents

An AI agent is a long-running process that can use an LLM, query external systems, and interact with other agents to accomplish complex tasks. For example, a travel agent could monitor flight prices and book a flight when the price is low, based on user preferences.

## 14. Reinforcement Learning with Human Feedback (RLHF)

RLHF is a training technique where human feedback is used to "reinforce" desired model behaviors. When a model generates multiple responses, a human picks the best one. This feedback is used to update the model's parameters, encouraging it to generate more helpful and accurate outputs.

## 15. Chain of Thought (CoT)

Chain of Thought is a prompting technique where the model is encouraged to break down a problem into a series of intermediate reasoning steps before giving the final answer. This improves the model's ability to reason through complex problems.

## 16. Reasoning Models

A reasoning model is an LLM that is capable of solving problems step-by-step. These models can use techniques like Chain of Thought to reason through a problem and determine the necessary steps to find a solution.

## 17. Multimodal Models

Multimodal models are AI models that can process and generate information in multiple formats, or "modes," such as text, images, and video. These models often have a deeper understanding of concepts because they can associate words with visual representations.

## 18. Small Language Models (SLMs)

SLMs are language models with a smaller number of parameters compared to LLMs (millions vs. billions). They are often trained on specific, proprietary data for a particular task or domain, making them more efficient and cost-effective for specialized applications.

## 19. Distillation

Distillation is a process for creating smaller, more efficient models (like SLMs) from larger ones. A larger "teacher" model is used to train a smaller "student" model. The student model learns to mimic the output of the teacher model, effectively compressing the knowledge into a smaller architecture.

## 20. Quantization

Quantization is a technique used to reduce the memory and computational cost of running a model. It involves reducing the precision of the model's weights (e.g., from 32-bit floating-point numbers to 8-bit integers). This is typically done after the model is fully trained to make inference faster and cheaper.

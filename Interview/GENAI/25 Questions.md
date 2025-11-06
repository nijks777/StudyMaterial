Easy (5)

What is Generative AI, and how is it different from traditional rule-based or discriminative AI models?

Explain the difference between LLMs (Large Language Models) and regular NLP models.

What is prompt engineering and why is it important?

What are tokens in LLMs, and how do they relate to context length?

Scenario: You want an LLM to return a JSON response. What is one simple prompting technique you would use?

Medium (15)

Explain the core idea of the Transformer architecture. What problem was it originally designed to solve?

What is self-attention, and how does it help in understanding relationships between words?

Describe the difference between pre-training, fine-tuning, and RAG (Retrieval-Augmented Generation). Give use case examples for each.

What are embeddings, and how are they used in semantic search or recommendation systems?

Scenario: Your chatbot responds with hallucinations (confident but incorrect information). List possible root causes and mitigation strategies.

Explain the concept of temperature and top-k / top-p sampling in text generation. How do they affect output style?

What is LoRA (Low Rank Adaptation), and why is it useful for fine-tuning large models?

Compare Open-source models (e.g., LLaMA, Mistral) vs. Closed-source models (e.g., GPT-5, Claude) in terms of cost, control, and governance.

What is Instruction Tuning, and how does it change a model’s behavior?

Scenario: Your RAG pipeline retrieves irrelevant chunks. What steps would you take to debug and improve retrieval?

Explain vector databases. Why are they used instead of relational databases for semantic search?

What are model hallucinations, and how can guardrails or external verification systems reduce them?

How do you evaluate LLM output quality? Mention both automatic metrics and human evaluation methods.

What is chain-of-thought reasoning, and why is transparency in reasoning controversial in closed models?

Scenario: You need to deploy a generative AI model to run on-premise due to data privacy. What technical and architecture considerations apply?

Explain the role of system prompts, assistant prompts, and user prompts in structured prompt design.

Difficult (5)

Deep Dive: Explain how positional encoding works in Transformers and how RoPE (Rotary Position Embeddings) improves long-context modeling.

Scenario: A company wants to fine-tune an LLM on proprietary data but must prevent the model from leaking internal information in output. Outline a safe training + inference strategy.

Compare RAG vs Fine-Tuning vs Knowledge Distillation for enterprise knowledge integration. When is each approach optimal and why?

Explain the trade-offs between Sparse Mixture of Experts (MoE) architectures vs dense Transformer models.

Scenario: You are tasked with evaluating fairness and bias in a generative AI system used for hiring. Describe the evaluation process, risk mitigation techniques, and documentation artifacts (e.g., model cards, data lineage, audit logs).
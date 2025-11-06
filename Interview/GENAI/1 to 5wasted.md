
1. (Generative AI) What is the "attention mechanism" in a Transformer model?
The attention mechanism is the core component of the Transformer architecture (the "T" in "GPT"). It's a technique that allows the model to weigh the importance of different words (tokens) in an input sequence when processing any single word.


Instead of processing words in a fixed, linear order (like older RNN models), attention allows the model to "look back" or "look ahead" at any word in the sentence, no matter how far away, and decide which ones are most relevant for understanding the current word's context.

It calculates a "score" for every other word in the sequence relative to the word it's currently processing. A high score means "pay a lot of attention to this word."

Simple Analogy: When you read the sentence, "The cat chased the mouse, and it was tired," your brain instantly knows "it" refers to the "cat" (or maybe the "mouse," it's ambiguous!). The attention mechanism does the same thing mathematically. It would assign a high "attention score" between the token "it" and the token "cat," and a lower score to "mouse" and "chased."

Example:

Input: "The server crashed because the hard drive failed."

When the model processes the word "crashed," the attention mechanism might link it strongly to "server."

More importantly, it can create a strong link between "crashed" and "failed," understanding that one caused the other, even though they are separated by other words.

This ability to model long-range dependencies is why Transformers are so powerful and have replaced older architectures.

Follow-up Questions:

Factual: "What key problem did the attention mechanism solve that older models like LSTMs and RNNs struggled with?"

Answer: They primarily solved the long-range dependency problem. In a very long sentence or paragraph, an RNN's "memory" (its hidden state) would fade. It would effectively "forget" the first words by the time it got to the end. Attention mechanisms have a "perfect" memory of the entire sequence at all times, so they can easily link the 500th word back to the 1st word.


Factual: "What is 'self-attention'? How is it different from 'attention'?"

Answer: "Self-attention" is the specific type of attention used within the Transformer model. The "self" part means the attention mechanism is applied to the input sequence itself. It's the sentence "paying attention" to different parts of itself to build a better internal representation. This is what's used in both the encoder and decoder of a Transformer.


Scenario-Based: "We need to build a model to summarize long, complex legal documents. Why would a Transformer model (which uses attention) be a much better choice than a legacy RNN-based model for this task?"

Answer: Legal documents are all about long-range dependencies. A defined term in paragraph 1 might be referenced by a pronoun ("the aforesaid party") in paragraph 50. An RNN would have "forgotten" the definition from paragraph 1. A Transformer's attention mechanism can instantly and strongly link "the aforesaid party" all the way back to its original definition, leading to a much more accurate and coherent summary.

2. (Generative AI) What are "hallucinations" in LLMs, and what is a common technique to reduce them?
A hallucination is when an LLM generates a response that is factually incorrect, nonsensical, or not grounded in the provided context, but states it with a high degree of confidence.

It's essentially the model "making things up." This happens because an LLM is a language model, not a knowledge engine. Its fundamental job is to predict the next most plausible-sounding token (word), not to predict the truth. If a fabricated answer "sounds" more linguistically probable than a "I don't know," the model will often generate the fabrication.

Example:

User: "What's the title of the research paper written by John A. Smith about atomic fusion in 2022?"

LLM Hallucination: "The paper you're referring to is 'A New Dawn in Fusion Energy' by John A. Smith, published in Nature Physics in October 2022."

Reality: John A. Smith never wrote this paper. The title and journal sound plausible, so the model "invented" it to satisfy the prompt.

Common Technique to Reduce Them: The most common and effective technique is Retrieval-Augmented Generation (RAG).

RAG works by "grounding" the model in facts. Instead of just asking the LLM the question directly, a RAG system first:

Retrieves: Searches an external, trusted knowledge base (like a database, company documents, or a live Google search) for relevant information.

Augments: Takes the factual information it found and stuffs it into the prompt with the user's original question.

Generates: Asks the LLM to "answer the user's question using only the information provided in this context."

By providing the "truth" in the prompt, you're not relying on the model's faulty memory; you're just asking it to summarize and rephrase the facts you just gave it.

Follow-up Questions:

Factual: "Besides RAG, name one other method you could use to try and reduce hallucinations."

Answer: You could try prompt engineering. For instance, adding a simple instruction like, "If you do not know the answer or the information is not in your knowledge base, say 'I do not know.'" This can make the model more cautious. Another method is fine-tuning the model on a high-quality, verified dataset.

Scenario-Based: "We've built a chatbot for our financial services company. It's hallucinating and giving customers incorrect policy information. This is a huge legal risk. What is your immediate plan to fix this?"

Answer: My immediate, top-priority plan is to implement a RAG system. We would take our entire library of official, lawyer-approved policy documents and load them into a vector database. The chatbot will be forbidden from answering any policy question from its own "memory." It must first retrieve the relevant policy paragraph from our trusted database and then use that text to formulate its answer. This grounds every response in an approved, verifiable source.

3. (Generative AI) What is the difference between fine-tuning a model and prompt engineering?
Both are methods for customizing an LLM's output, but they operate at very different levels.

Prompt Engineering is changing the input to the model to get a better output. You are not changing the model itself.

Analogy: You are a director giving better instructions to a very smart, general-purpose actor (the LLM). You can give them a role ("You are a pirate"), a task ("Write a sea shanty"), and examples ("Here's a sample verse...").

How: You craft the text prompt you send to the API. This is fast, cheap, and requires no special hardware.

Example: Instead of "Summarize this," you write, "You are an expert financial analyst. Summarize the key risks from this earnings report in 3 bullet points, using a formal tone."

Fine-Tuning is changing the model itself by continuing its training on a new, specialized dataset.

Analogy: You are sending that actor to a 6-month specialized acting course to permanently teach them a new skill (e.g., how to always speak in a Shakespearian style).

How: You gather thousands of high-quality "prompt-response" examples, and you run a training process that updates the model's internal parameters (its weights) to be better at those specific examples. This is slow, expensive, and requires a dataset.

Example: You provide 5,000 examples of your company's support tickets and the "perfect" responses. The fine-tuned model now "innately" knows your company's products and tone of voice.

When to use which:

Always start with prompt engineering. It's 90% of the solution and can often solve your problem.

Use fine-tuning only when prompt engineering fails, or when you need to teach the model a complex new skill, style, or knowledge domain that is too large or nuanced to fit in a prompt.

Follow-up Questions:

Factual: "What is the 'in-context learning' that prompt engineering enables?"

Answer: "In-context learning" is the LLM's ability to learn "on the fly" just from the examples in your prompt. This is also called "few-shot prompting." By providing 2 or 3 examples of a task (e.g., "French: Hello -> Bonjour," "French: Goodbye -> Au revoir"), the model learns the pattern from the context and can perform the task ("French: Thank you -> ?").

Scenario-Based: "We want our AI to generate code for our internal, proprietary software framework. The documentation for this framework is 500 pages long. Should we use prompt engineering or fine-tuning?"

Answer: This is a case where fine-tuning is a strong candidate. You can't fit 500 pages of documentation into a single prompt (see "context window"). A better approach would be to fine-tune the model on thousands of examples of code using that framework. However, an even better modern solution might be RAG, where you put all 500 pages into a vector database and the model "looks up" the relevant documentation for each specific code-generation task.

4. (Generative AI) What is "model context window," and why is it a critical limitation?
A model's context window is its "short-term memory." It is the maximum number of tokens (words and parts of words) that the model can process at one time. This includes both the input (your prompt) and the output (its generated response).

If your input + output is larger than the context window, the model simply cannot "see" or "remember" the tokens that came before it.

Analogy: Imagine you're having a conversation on a long scroll of paper. The context window is a physical, 12-inch "window" that you can slide over the scroll. You can only read and react to the 12 inches of text visible inside that window. In a long conversation, as you slide the window forward, the beginning of the conversation disappears from view. The model has no memory that it even existed.

Why it's a critical limitation:

Limited Conversation Length: This is why a chatbot can "forget" what you said 20 messages ago. The start of the conversation has "scrolled out" of its context window.

Can't Process Large Documents: You cannot simply paste a 100-page PDF (which might be 50,000 tokens) into a model with an 8k token window and ask, "Summarize this." The model will only see the first 8,000 tokens.

Limits Complex Reasoning: For complex tasks, the model "uses" its context window as a "scratchpad" to "think step-by-step." A small window limits the complexity of the problems it can solve.

Example:

A model like gpt-3.5-turbo might have a 4k (4,096) or 16k (16,385) token window.

A 100-page document is far too large.

A user who pastes a long essay and asks a question about a detail in the first paragraph might get a "I don't see that mentioned" error, because the first paragraph has been cut off.

Follow-up Questions:

Factual: "What is a common technique to handle a document that is larger than the context window?"

Answer: The most common technique is "chunking" and RAG. You split the 100-page document into 100 separate "chunks." You use a vector database to find the most relevant chunks related to the user's question, and then you feed only those few chunks (which fit in the window) to the LLM.

Scenario-Based: "We just bought a new model with a massive 200k context window. Our manager says, 'Great! Let's just feed our whole 100-page document into every prompt! RAG is dead.' What is the (polite) problem you would point out with this approach?"

Answer: I would point out two major problems:

Cost: LLM APIs are priced per token. Forcing the model to read 100 pages every single time a user asks a question would be astronomically expensive.

Performance & Accuracy: Models can suffer from a "lost in the middle" problem. Their accuracy at finding a "needle in a haystack" tends to drop when the haystack (the context) is massive. RAG is still more efficient and often more accurate, as it hands the model just the needle.

5. (Generative AI) What is a vector embedding, and why is it used in Generative AI?
A vector embedding (or "embedding") is a numerical representation of the semantic meaning of a piece of data, such as a word, a sentence, or an entire document.

It's a list of numbers (a "vector") that captures where that piece of data lives in a high-dimensional "meaning space."

Analogy (The Map): Imagine a giant map where every concept has a location (an X, Y coordinate).

The word "Cat" might be at coordinate (10, 12).

The word "Kitten" would be very close by, at (10, 11).

The word "Dog" would be nearby, but not as close, at (12, 14).

The word "Car" would be in a totally different part of the map, at (50, 80).

Embeddings do this, but instead of 2D (X, Y), they use hundreds or thousands of dimensions.

Why is this used? Computers cannot understand words, but they excel at math. Embeddings translate "meaning" into "math." By turning "Cat" and "Kitten" into two vectors (lists of numbers), a computer can easily calculate the "distance" between them and see that they are very close.

Primary Use in Generative AI (RAG): This is the core engine of Retrieval-Augmented Generation (RAG) and semantic search.

Indexing: You pre-process all your documents (e.g., your company's wiki) by feeding them through an embedding model. You store the resulting vectors in a vector database.

Searching: When a user asks a question (e.g., "What's our vacation policy?"), you turn that question into a vector.

Matching: You then ask the vector database: "Find me the top 3 document vectors that are mathematically closest to this question vector."

Retrieval: The database returns the 3 documents that are semantically (meaning-wise) most similar to the question, even if they don't share the same keywords.

This process—finding documents by meaning rather than keywords—is what allows a RAG system to find the correct context to give to the LLM.

Follow-up Questions:

Factual: "What's the difference between a vector search and a traditional keyword search?"

Answer: A keyword search (like a Ctrl+F) finds exact matches. If you search for "company holidays," it will not find a document that only says "PTO and office closures." A vector (semantic) search will find that document, because the meaning of "company holidays" is mathematically very close to the meaning of "PTO and office closures."

Scenario-Based: "A user is searching our e-commerce site for 'a gift for my dad who likes fishing.' Our current search bar (which uses keyword search) returns zero results. How would embeddings fix this?"

Answer: We would create embeddings for all our product descriptions. A description like "This high-quality tackle box is perfect for a weekend on the lake" would have a vector. The user's query ("gift for my dad who likes fishing") would also be turned into a vector. In the "meaning map," these two vectors would be very close. The vector search would instantly find the tackle box (and fishing rods, etc.) as the top results, even though the user never typed the word "tackle box."
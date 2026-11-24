# Day 2 – Agentic AI Workshop 🤖

## 📌 Overview

Day 2 of the Agentic AI Workshop, conducted by our **DOTT (Department of Technical Training)**, focused on building AI-powered conversational assistants using Python, Groq, and Large Language Models (LLMs).

The session explored how to create a customer support chatbot with predefined instructions, integrate LLMs, handle user conversations, and introduce basic safety mechanisms.

## 🧠 Concepts Covered

- **Groq API Integration:** Connecting Python applications with Groq-hosted language models.
- **LangChain:** Using `ChatGroq` to interact with LLMs.
- **Prompt Engineering:** Defining system instructions, roles, rules, and response formats.
- **LLM Interaction:** Sending user queries and generating AI-powered responses.
- **Prompt Guard:** Exploring protection against unsafe prompts and prompt injection attempts.
- **Conversation Memory:** Maintaining conversation history to provide contextual responses.
- **Function Decorators:** Using Python decorators to log function calls and results.
- **Error Handling:** Handling API rate limits and connection errors gracefully.
- **Function Calling / Tool Logic:** Implementing a price calculation function for bakery products.

## 🛠️ Practical Implementation

### 1. Bakery Customer Support Assistant

Created an AI-powered assistant for **Sweet Crumbs Home Bakery**.

The chatbot follows predefined business rules:
- Orders require 24 hours' notice.
- All cakes have eggless versions.
- It should never promise delivery times.
- Unknown information should be handled appropriately.
- Responses should be polite and concise.

### 2. Prompt Guard Exploration

Explored the `meta-llama/llama-prompt-guard-2-22m` model to understand how prompt injection and potentially unsafe instructions can be detected.

### 3. Interactive Bakery Chatbot

Extended the chatbot with additional functionality:

- Menu and pricing information.
- Automatic total price calculation.
- Conversation history to maintain context.
- English and Telugu response support.
- API error handling.
- Function call logging using decorators.
- Graceful exit commands.

## 💻 Technologies & Libraries

- Python
- Groq API
- LangChain
- `langchain_groq`
- OpenAI Python SDK compatibility
- LLMs: GPT-OSS and Llama Prompt Guard

## 🚀 Key Takeaways

- Learned how to integrate LLMs into Python applications.
- Understood the importance of system prompts and prompt engineering.
- Explored basic prompt injection protection.
- Implemented conversation history for contextual interactions.
- Practiced Python decorators and exception handling.
- Built a rule-based AI customer support experience powered by an LLM.

## 📂 Notebook

`Day - 2.ipynb`

## 🎯 Learning Journey

Continuing my Agentic AI learning journey through hands-on implementation, experimentation, and practical exploration.

**Day 2 completed! 🚀**

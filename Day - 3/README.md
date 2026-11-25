# Day 3 – Building AI Chatbots & Exploring Agents 🤖

## 📌 Overview

Day 3 of the Agentic AI Workshop, organized by the **Department of Technical Training (DOTT), Aditya University**, focused on building AI-powered chatbots using Python, Groq, and LangChain.

The session involved developing conversational assistants for different business scenarios, implementing conversation history, handling API errors, testing chatbot responses, and exploring the fundamentals of LangChain agents.

## 🧠 Concepts Covered

- **LLM Integration:** Connecting Python applications with Large Language Models using Groq.
- **Prompt Engineering:** Designing system prompts with roles, facts, rules, and response formatting instructions.
- **Conversation Memory:** Maintaining conversation history to allow the chatbot to remember previous interactions.
- **Python Decorators:** Using decorators to log function calls and their results.
- **Function Implementation:** Creating utility functions for price calculations.
- **Error Handling:** Handling API rate limits and connection failures.
- **Automated Testing:** Validating chatbot responses against expected keywords using CSV test cases.
- **LangChain Chains:** Connecting prompts, language models, and output parsers using the LCEL pipeline.
- **LangChain Agents:** Exploring agent creation using `create_agent`.

## 🛠️ Practical Implementations

### 1. Sweet Crumbs Home Bakery Assistant

Created a simple AI assistant for a home bakery using Groq and LangChain.

The chatbot follows predefined business rules:

- Orders require 24 hours' notice.
- All cakes have eggless versions.
- Never promise delivery times.
- Respond politely and concisely.
- If information is unknown, acknowledge it instead of making assumptions.

### 2. Prompt Guard Exploration

Explored the Llama Prompt Guard model to understand how potentially malicious prompts and prompt injection attempts can be detected.

### 3. Knowledge Book Store Chatbot

Developed a conversational assistant for a book store with predefined menu items and prices.

Features include:

- Book and stationery price information.
- Order-related information.
- Customer-friendly responses.
- English and Telugu language support.
- Customer name and order context retention.
- Business-specific instructions through system prompts.

### 4. Function Decorators & Price Calculation

Implemented a `log_call` decorator to log function execution and return values.

Created a `get_price()` function to calculate the total price of products based on quantity.

Example:

```python
get_price("white book", 6)
```

The function calculates the total price using the predefined menu.

### 5. Conversation Memory

Implemented conversation history to preserve previous interactions and allow the chatbot to answer contextual questions, such as remembering a customer's name.

### 6. Error Handling

Handled common API failures:

- **RateLimitError** – Handles API rate-limit issues.
- **APIConnectionError** – Handles connection failures.

The chatbot returns user-friendly messages instead of crashing.

### 7. LangChain Prompt & Chain

Explored building an LLM pipeline using:

- `ChatPromptTemplate`
- `MessagesPlaceholder`
- `StrOutputParser`
- `ChatGroq`

Combined them using the LangChain Expression Language (LCEL):

```python
chain = prompt | llm | StrOutputParser()
```

### 8. Automated Response Testing

Implemented CSV-based chatbot testing.

Test cases contain:

- A question.
- A keyword that the response must include.

The test runner checks whether the chatbot response contains the expected keyword and reports the pass/fail results.

### 9. Introduction to LangChain Agents

Explored creating an agent using LangChain's `create_agent`.

```python
agent = create_agent(
    model=llm,
    tools=[],
    system_prompt=SYSTEM
)
```

Invoked the agent with a user message to generate a response. Tool integration is planned for the next session.

## 🛠️ Technologies & Libraries

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| Groq API | Access to hosted LLMs |
| LangChain | Building LLM-powered applications |
| `langchain_groq` | Groq integration with LangChain |
| `ChatPromptTemplate` | Structured prompt creation |
| `MessagesPlaceholder` | Incorporating conversation history |
| `StrOutputParser` | Parsing model output into strings |
| `create_agent` | Creating LangChain agents |
| CSV | Storing and executing chatbot test cases |

## 🚀 Key Takeaways

- Learned to build business-specific AI chatbots using system prompts.
- Practiced prompt engineering using roles, rules, facts, and output constraints.
- Implemented conversational memory.
- Used Python decorators for logging function execution.
- Practiced API error handling.
- Built a simple automated testing mechanism for chatbot responses.
- Explored LangChain chains and LCEL.
- Got introduced to LangChain agents and their structure.

## 📂 Notebook

`task.py`

## 🎯 Learning Journey

Day 3 was focused on moving beyond basic LLM interaction and building more structured chatbot applications with memory, business logic, testing, and an introduction to agents.

**Day 3 completed! 🚀**

*Learning every day. Building consistently. Growing with AI.*

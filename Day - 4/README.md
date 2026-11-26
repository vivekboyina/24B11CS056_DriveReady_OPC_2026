# Day 4 – Agentic AI Workshop

## 📌 Overview

Day 4 of the Agentic AI Workshop focused on building AI-powered assistants using **LLMs, LangChain, tool calling, prompt engineering, conversation memory, and Google Sheets integration**.

The tasks explored how to move from a basic chatbot to an agent capable of interacting with tools, calculating prices, checking store timings, and storing customer orders.

## 🚀 Topics Covered

- Integrating Groq LLMs with Python
- Prompt engineering and system instructions
- Building chat assistants using LangChain
- Maintaining conversation history
- Handling API errors and rate limits
- Function and tool calling
- Structured data validation using Pydantic
- Logging and decorators
- Testing chatbot responses using CSV test cases
- Google Colab Secrets for API key management
- Google Sheets integration using `gspread`
- Saving customer orders automatically

## 🛠️ Technologies Used

- **Python**
- **Groq API**
- **LangChain**
- **OpenAI-compatible Groq API**
- **Google Colab**
- **Google Sheets**
- **Pydantic**
- **CSV**

## 📚 Tasks & Implementations

### 1. Bakery Assistant

Created a simple AI assistant for *Sweet Crumbs Home Bakery* using LangChain and Groq.

The assistant follows predefined business instructions:

- Orders require 24 hours' notice.
- Eggless cake versions are available.
- It must not promise delivery times.
- Responses should be polite and concise.

### 2. Prompt Guard Experiment

Explored the use of **Llama Prompt Guard** to identify potentially unsafe or prompt-injection-style user inputs.

### 3. Bookstore Chatbot

Built a conversational assistant for *Knowledge Book Store* with:

- Product pricing
- Order-related information
- Customer name retention
- Conversation history
- Rate-limit handling
- API connection error handling

### 4. Logging with Decorators

Implemented a Python decorator to log function calls and their results.

Used it to track price-calculation function executions.

### 5. Prompt Templates & Conversation Memory

Used LangChain components to build a conversational chain:

- `ChatPromptTemplate`
- `MessagesPlaceholder`
- `StrOutputParser`

The assistant maintains conversation history and can recall information shared earlier in the conversation.

### 6. CSV-Based Testing

Created a testing function that reads questions and expected keywords from a CSV file.

The test checks whether the chatbot's response contains the required keyword and reports the number of passing tests.

### 7. LangChain Agent

Initialized an agent using LangChain's `create_agent` and explored the agent framework before integrating tools.

### 8. Google Sheets Integration

Integrated Google Sheets with Python using:

- Google Colab authentication
- `gspread`
- Google credentials

Created or opened a spreadsheet named **Knowledge Book Store Orders** to store order details.

### 9. Structured Order Management

Created a `BookOrder` model using Pydantic to validate customer order information.

Order details include:

- Customer name
- Item
- Quantity
- Pickup/delivery date

### 10. Agent Tools

Implemented three tools for the bookstore agent:

| Tool | Function |
|---|---|
| `get_price` | Calculates item prices and applies discounts |
| `is_open` | Checks store operating hours |
| `log_order` | Saves confirmed orders to Google Sheets |

### 11. Discount Logic

Implemented a **Buy 5 Rule Books, Get 1 Free** promotion.

| Item | Price |
|---|---:|
| White Book | ₹50 |
| Rule Book | ₹50 |
| Pencil | ₹5 |

For example, purchasing 6 rule books costs ₹250 instead of ₹300.

### 12. Tool-Calling Agent

Built an agent using the Groq API that can:

1. Understand the customer's request.
2. Determine which tool is required.
3. Call the appropriate tool.
4. Process the tool's result.
5. Respond to the customer.
6. Save confirmed orders to Google Sheets.

## 🧠 Key Learnings

- How system prompts influence LLM behaviour.
- How conversational history enables contextual responses.
- How to use tools to extend an LLM beyond text generation.
- How to validate structured data using Pydantic.
- How to handle API errors gracefully.
- How to integrate AI applications with external services.
- How agents decide when to call tools.
- How to automate real-world business workflows using AI.

## ⚙️ Setup

This notebook was designed to run in Google Colab.

### 1. Install dependencies

```bash
pip install langchain langchain-groq groq gspread
```

### 2. Configure API key

Add your Groq API key to Google Colab Secrets with the key name:

```text
Agentic_AI
```

### 3. Run the notebook

Run the notebook cells sequentially, authenticate with Google when prompted, and authorize access to Google Sheets.

## 🎯 Outcome

Developed a foundation for building AI-powered business assistants that can maintain conversational context, interact with tools, calculate prices, validate customer orders, check business information, and store order records using Google Sheets.

---

**Day 4 completed as part of the Agentic AI Workshop conducted by DOTT (Department of Technical Training) at college.**

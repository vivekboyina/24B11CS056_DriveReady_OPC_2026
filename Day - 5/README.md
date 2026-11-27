# Day 5 – Agentic AI Workshop

## 📌 Overview

Day 5 of the Agentic AI Workshop focused on enhancing AI agents with **Retrieval-Augmented Generation (RAG), vector databases, knowledge retrieval, session-based memory, custom business knowledge, and context-aware tool calling**.

The session involved building a business assistant that retrieves relevant information from a knowledge base instead of relying entirely on the LLM's internal knowledge. It also explored maintaining separate conversations for different users and handling questions that fall outside the available knowledge.

## 🎯 Topics Covered

- Retrieval-Augmented Generation (RAG)
- Vector databases
- ChromaDB
- FAQ knowledge bases
- Semantic search
- Custom LangChain tools
- Tool calling with Groq
- Session-based conversation memory
- Multi-user conversation isolation
- Context-aware AI agents
- Hallucination prevention
- Out-of-domain question handling
- CSV-based testing and evaluation

## 🛠️ Technologies Used

| Technology / Tool | Purpose |
|---|---|
| Python | Implementation |
| Groq API | LLM inference |
| GPT-OSS 20B | Model used for agent responses |
| ChromaDB | Storing and retrieving business knowledge |
| LangChain | Tool creation and agent integration |
| Groq Tool Calling | Calling functions based on user queries |
| Google Colab | Development environment |
| CSV | Test cases and response evaluation |

## 📚 Tasks & Implementations

### 1. Building a FAQ Knowledge Base

Created a collection of frequently asked questions and business policies for Sweet Crumbs Home Bakery.

The knowledge base contains information about:

- Delivery policies
- Payment methods
- Cancellation policies
- Photo cakes and custom designs
- Order notice requirements
- Eggless cake availability
- Allergens
- Cake storage
- Cake messages
- Candles
- Discounts
- Pickup timings

Stored these facts in **ChromaDB** for retrieval.

### 2. ChromaDB Integration

Integrated ChromaDB as a vector database to store business information.

Implemented:

- Collection creation
- Storing FAQ documents
- Updating documents using `upsert`
- Querying the collection
- Retrieving relevant information based on user questions

### 3. Semantic Search

Explored semantic retrieval by querying the FAQ collection using natural-language questions.

Instead of relying only on exact keyword matches, the system retrieves relevant documents based on the meaning of the user's query.

### 4. FAQ Search Tool

Created a custom LangChain tool called `search_faq`.

The tool:

1. Accepts a user's question.
2. Searches the ChromaDB FAQ collection.
3. Retrieves relevant business policies.
4. Returns the retrieved information to the agent.

### 5. RAG-Based Business Assistant

Integrated FAQ retrieval into the Sweet Crumbs business assistant.

The agent uses tools to:

- Retrieve business policies from the knowledge base.
- Check prices.
- Check operating hours.
- Save confirmed orders.

The system is instructed to answer policy-related questions using retrieved information and avoid inventing answers when the knowledge base does not contain the required facts.

### 6. Session-Based Conversation Memory

Implemented session-based memory using separate session identifiers.

Each session maintains its own conversation history, allowing the assistant to remember previous messages within the same conversation.

This enables:

- Remembering customer details within a session.
- Handling follow-up questions.
- Maintaining contextual conversations.
- Keeping different users' conversations separate.

### 7. Multi-User Conversation Testing

Tested multiple conversation sessions using different thread IDs.

For example:

- Ravi's conversation maintains Ravi's context.
- Sravani's conversation maintains her own context.
- Separate sessions prevent one user's information from being mixed with another user's conversation.

### 8. Automated Testing

Created a testing function to evaluate agent responses against expected keywords.

The tests cover business questions related to:

- Delivery
- Allergens
- Photo cake notice
- Payment methods
- Unsupported products

The testing process uses independent sessions to reduce context contamination between test cases.

### 9. Custom Business Knowledge – Homework

Created a separate knowledge base for a custom coffee shop business.

The knowledge base contains 15 business facts covering:

- Store location
- Opening hours
- Wi-Fi availability
- Organic and fair-trade coffee
- Gluten-free and vegan pastries
- Student discounts
- Payment methods
- Pet policies
- Signature drinks
- Open mic events
- Loyalty points
- Delivery and pickup
- Catering notice
- Gift cards
- Ingredients and preservatives

### 10. Custom Coffee Shop Agent

Built a separate coffee shop assistant using:

- ChromaDB for business knowledge storage
- A custom `search_biz_faq` tool
- Groq for LLM inference
- Session-based memory

The assistant retrieves relevant facts before answering questions about policies, facilities, menu details, and events.

### 11. Testing Memory and Unsupported Questions

Tested the coffee shop agent using different session IDs.

The tests explored:

- Student discount queries
- Gluten-free food queries
- Conversation follow-ups
- Session isolation
- Questions about unsupported products
- Handling questions outside the knowledge base

The assistant is instructed to avoid inventing information and to check with the owner when the required information is unavailable.

## 🧠 Key Learnings

- Understanding the role of RAG in AI applications.
- Storing business information in vector databases.
- Retrieving relevant information using semantic search.
- Connecting knowledge retrieval to AI agents through tools.
- Building assistants that answer from custom business knowledge.
- Maintaining separate conversation histories using session IDs.
- Preventing context leakage between users.
- Handling unsupported and out-of-domain questions.
- Evaluating chatbot responses using automated tests.
- Reducing hallucinations by grounding responses in retrieved facts.

## ⚙️ Setup

This implementation was developed in Google Colab.

### 1. Install Dependencies

```bash
pip install langchain langchain-groq groq chromadb
```

Additional packages used in later cells include:

```bash
pip install -U langchain-core langchain-groq langgraph
```

### 2. Configure Groq API Key

Add your Groq API key to Google Colab Secrets with the name:

```text
Agentic_AI
```

### 3. Run the Notebook / Python File

Run the cells sequentially to:

1. Initialize the Groq client.
2. Create the ChromaDB collections.
3. Load business FAQs.
4. Define the search tools.
5. Initialize the agent.
6. Test conversations and session memory.

## 🎯 Outcome

Explored how to build knowledge-grounded AI assistants using vector databases and retrieval-based tools. Implemented business FAQ retrieval, session-based memory, multi-user context separation, custom knowledge bases, and tests for unsupported questions.

---

**Day 5 completed as part of the Agentic AI Workshop conducted by DOTT (Department of Technical Training) at Aditya University.**

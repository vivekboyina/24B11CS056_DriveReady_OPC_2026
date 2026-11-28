# 🚀 Agentic AI Workshop – Day 6

## 📌 Overview

Day 6 of the Agentic AI Workshop focused on building more structured AI agents using **LangGraph**, integrating tools, managing workflows, and routing user requests based on intent.

The session extended previous chatbot and RAG implementations by introducing an intent classifier and specialized agents for handling FAQs, order requests, and general conversations.

## 🎯 Topics Covered

- LLM Integration using Groq
- Prompt Engineering and System Prompts
- Conversation Memory and Chat History
- Tool Calling and Function Calling
- Pydantic Models and Structured Data Validation
- Google Sheets Integration for Order Management
- Retrieval-Augmented Generation (RAG)
- ChromaDB and Semantic Search
- Intent Classification using Structured JSON Output
- LangGraph StateGraph
- Nodes, Edges, and Conditional Routing
- Specialized Agents for FAQs and Orders
- Agent Workflow Testing

## 🛠️ Technologies Used

| Technology | Purpose |
|---|---|
| Python | Implementation |
| Groq API | LLM inference |
| LangChain | Agent and tool integration |
| LangGraph | Workflow orchestration and routing |
| ChromaDB | Vector storage and FAQ retrieval |
| Pydantic | Structured data validation |
| Google Sheets | Order storage and logging |
| Google Colab | Development environment |

## 📚 Tasks Completed

### 1. AI Chatbot Development
- Created assistants for Sweet Crumbs Home Bakery and Knowledge Book Store.
- Implemented system prompts with business facts and response rules.
- Added conversation history and contextual responses.
- Implemented rate-limit and connection error handling.

### 2. Tool Calling & Order Management
- Created tools for price calculation, business-hour checking, and order logging.
- Added order validation using Pydantic.
- Integrated Google Sheets for storing customer orders.
- Implemented a Buy 5 Rule Books, Get 1 Free discount.

### 3. RAG & Knowledge Retrieval
- Stored business FAQs in ChromaDB.
- Implemented semantic search to retrieve relevant information.
- Created FAQ retrieval tools for AI agents.
- Designed responses to rely on retrieved information rather than inventing unsupported facts.

### 4. Session-Based Memory
- Maintained separate conversation histories using thread IDs.
- Tested multi-user conversations and memory isolation.
- Handled unsupported or out-of-domain questions.

### 5. Intent Classification
Implemented intent classification to categorize bookstore messages into:

- **Order** – purchase, booking, or order logging requests
- **FAQ** – price, opening hours, or policy questions
- **Other** – greetings, thanks, and general conversations

### 6. LangGraph Workflow

Built a workflow using `StateGraph` with:

- **Classify Node** – identifies the intent of the incoming message.
- **FAQ Node** – handles customer questions using FAQ tools.
- **Order Node** – handles book orders and order-related tools.
- **Other Node** – handles general conversations.

Conditional routing directs the message to the appropriate specialized agent.

## 🔄 Workflow

```text
User Message
     |
     v
Intent Classifier
     |
     +---------- FAQ ----------> FAQ Agent
     |
     +---------- Order -------> Order Agent
     |
     +---------- Other -------> General Response
                                  |
                                  v
                                Output
```

## 🧪 Testing

- Tested FAQ-related queries.
- Tested order requests and missing information.
- Tested greetings and general conversations.
- Tested agent routing for different intents.
- Tested business knowledge retrieval.
- Tested conversation memory and session separation.
- Tested responses to unsupported questions.

## 💡 Key Learning Outcomes

- Understanding how to move from a single chatbot to specialized AI agents.
- Building stateful workflows using LangGraph.
- Implementing intent classification and conditional routing.
- Integrating tools with LLMs.
- Using RAG to provide knowledge-grounded responses.
- Managing conversation state and multi-user sessions.
- Designing structured and modular agent workflows.

## 🏁 Outcome

Successfully implemented a business assistant workflow that classifies user intent and routes messages to specialized FAQ, order-processing, or general-response nodes using LangGraph.

---

**Workshop:** Agentic AI Workshop  
**Organized by:** Department of Technical Training (DOTT), Aditya University

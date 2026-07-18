# Ai_Assistant_n8n

# Real_Workflow_plus 🚀

Real_Workflow_plus is an advanced, multi-agent AI orchestration workflow built on n8n. The system leverages a central **Supervisor Agent** that intelligently routes tasks, manages memory, and delegates actions to specialized sub-agents powered by local **Ollama** language models. 

Equipped with external tools (Google Services, Web Search), this workflow automates complex digital tasks seamlessly in a private or hybrid cloud environment.

---

## 🛠️ Tech Stack & Integrations

Here are the core technologies and services used in this project:

*   **Orchestration Engine:** ![n8n](https://img.shields.io/badge/n8n-FF6C37?style=flat&logo=n8n&logoColor=white)
*   **Local AI Models:** ![Ollama](https://img.shields.io/badge/Ollama-000000?style=flat&logo=ollama&logoColor=white) (Powering the Supervisor & Agents)
*   **Search Engine:** ![SerpAPI](https://img.shields.io/badge/SerpAPI-4285F4?style=flat&logo=google&logoColor=white) (Google Search Automation)
*   **Productivity Suite:** 
    *   ![Gmail](https://img.shields.io/badge/Gmail-D14836?style=flat&logo=gmail&logoColor=white) (Email management)
    *   ![Google Calendar](https://img.shields.io/badge/Google%20Calendar-4285F4?style=flat&logo=googlecalendar&logoColor=white) (Event management)

---

## 🧠 System Architecture & Workflow

The architecture is designed around a **Supervisor-Worker** paradigm, structured as follows:

1.  **Trigger (`When chat message received`):** Starts the workflow through a chat interface.
2.  **Supervisor:** The brain of the operation. It maintains a **Simple Memory** stack, analyzes the user input, and decides which specialized agent is best suited to handle the request.
3.  **Specialized Sub-Agents:**
    *   📧 **Gmail Agent:** Connected to an Ollama Chat Model. It has specific tools to **Read Emails** (`get mail`) and **Send Emails** (`Send email`).
    *   🔍 **Search Agent:** Connected to an Ollama Chat Model and armed with **SerpAPI** to look up real-time information on the web.
    *   📅 **Calendar Agent:** Connected to an Ollama Chat Model with full access to **Get Events** (`getAll event`) and **Create Events** (`create event`).

---

## 🚀 Key Features

*   **Multi-Agent Collaboration:** Instead of relying on a single prompt, specialized agents handle complex workflows independently.
*   **Privacy-First AI:** Driven by local **Ollama Chat Models**, ensuring sensitive data processed by the models stays secure.
*   **Dynamic Tool Calling:** The Supervisor automatically detects when it needs to fetch web data, manage schedules, or read/write emails.
*   **Persistent Context:** Utilizes a centralized memory node allowing the conversation to flow naturally across multiple turns.

---

## 📋 Prerequisites

To run this workflow, you will need:
* An active **n8n** instance (Self-hosted or Cloud).
* **Ollama** running locally with your preferred models pulled (e.g., `llama3`, `mistral`, or `phi3`).
* **Google Cloud Console** credentials configured in n8n for Gmail and Google Calendar OAuth2.
* A **SerpAPI** API key for web search capabilities.

---

## 🔧 Installation & Setup

1. Clone or copy the JSON export of this workflow from this repository.
2. Open your n8n dashboard.
3. Click on the top-right menu and select **Import from File** (or paste the JSON directly into the editor canvas).
4. Configure your credentials for:
   * **Ollama** (Verify your host URL, e.g., `http://localhost:11434`).
   * **Gmail OAuth2 API**.
   * **Google Calendar OAuth2 API**.
   * **SerpAPI** (Under the tool node variables).
5. Click **Publish** to activate the chat interface.

---

## 👤 Author

*   **Ziad Nassar** - [GitHub Profile](https://github.com/ziadnassar6-lgtm)

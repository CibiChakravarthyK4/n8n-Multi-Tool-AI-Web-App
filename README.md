# n8n-Multi-Tool-AI-Web-App

An advanced, webhook-driven n8n AI agent web application equipped with multi-tool capabilities, allowing users to interact seamlessly via a chat interface and execute actions across productivity platforms and the web.


## ⚡ Quick Architecture

[ Webhook Trigger ] ──► [ AI Agent ] ──► [ Web App Response ]
│
┌──────────────────┼──────────────────────────────────────┐
▼                  ▼        ▼             ▼        ▼      ▼
[ OpenAI Model ] [ Simple Memory ] [ Google Docs ] [ Calendar ] [ Sheets ] [ Gmail ] [ SerpApi ]


## ✨ Features

* **Interactive Web Chat Interface:** Clean, user-friendly chat app layout for communicating directly with the multi-agent system.
* **Webhook Routing:** Processes real-time chat requests using n8n webhook endpoints (supporting both test and production URLs).
* **Multi-Tool Integration:** Intelligently invokes tools to manage Google Docs, Google Calendar events, Google Sheets, Gmail messages, and SerpApi web searches.
* **Conversational Memory:** Retains multi-turn chat history and context using Simple Memory.

## 🛠️ Prerequisites & Setup

1. **n8n Instance:** Self-hosted or cloud-based n8n environment.
2. **Credentials Needed:**
   * **OpenAI API Key** (for the Chat Model)
   * **Google OAuth2 Credentials** (for Docs, Calendar, Sheets, and Gmail)
   * **SerpApi API Key** (for Google Search)
   * 
## 🚀 Installation & Usage

1. **Import Workflow:** Import the workflow JSON file into your n8n dashboard.
2. **Configure Credentials:** Link your OpenAI, Google Workspace, and SerpApi credentials to their respective sub-nodes.
3. **Configure Frontend URL (Lovable):** Paste your webhook URL into your Lovable app frontend to connect the UI interface with your n8n backend workflow.
4. **Activate Webhook:** 
   * Use the **Test Webhook** URL (`/webhook-test/...`) while debugging or testing inside Lovable.
   * Toggle the workflow to **Published / Active** and use the **Production Webhook** URL (`/webhook/...`) for your live production web application interface.
5. **Launch:** Open your Lovable chat web app interface and start interacting with your multi-tool AI agent!

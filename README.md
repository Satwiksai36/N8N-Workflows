# n8n Automations & AI Agent Workflows

This repository contains a collection of advanced automation workflows built using [n8n](https://n8n.io/). These workflows integrate artificial intelligence (Google Gemini), messaging platforms (Telegram, Gmail), external APIs, and Google Workspace applications (Calendar, Tasks, Sheets) to create smart, agentic automations.

## 📂 Included Workflows

Here is a breakdown of the workflows included in this repository:

### AI & Agentic Workflows
* **Agentic Workflow of Chat Model.json**: An AI agent setup that utilizes a Google Gemini Chat Model and connects to a Google Tasks tool to manage tasks via chat[cite: 1].
* **AI agent chat.json**: A chat-triggered AI assistant that uses Google Gemini and integrates with SerpAPI to perform web searches[cite: 2].
* **AI Personal Assistant With Telegram.json**: A comprehensive Telegram bot assistant[cite: 3]. It handles text and voice messages, transcribes audio recordings using Gemini, and routes requests to Google Tasks or triggers a secondary Google Calendar workflow[cite: 3].
* **Google Calender Agent Workflow.json**: A backend AI agent designed to be called by other workflows (like the Telegram assistant)[cite: 7]. It intelligently creates, retrieves, and updates events in Google Calendar based on conversational prompts[cite: 7].

### Form & Data Automation
* **Form Automation.json**: A lead capture workflow that triggers on form submission, appends the lead's data into a Google Sheet, and immediately sends an email notification via Gmail[cite: 5].
* **Form Automation Using HTTP Request.json**: A data enrichment workflow[cite: 4]. It pulls potential customer names from a Google Sheet, runs them through external APIs (Genderize, Nationalize, Agify) via HTTP requests to predict demographics, updates the Google Sheet with the new data, and sends an email summary[cite: 4].

### Email Management
* **Gmail AI Reply.json**: An intelligent inbox manager that checks for new emails and uses a Gemini AI Agent with a structured output parser to categorize the email (e.g., course, doubt, sponsorship)[cite: 6]. It automatically applies the correct Gmail label and drafts a context-aware HTML reply[cite: 6].
* **Sending Test Email.json**: A simple, manually triggered workflow used to test Gmail OAuth2 connectivity and send a basic text email[cite: 8].

## ⚙️ Prerequisites

To use these workflows, you will need:
1. A running instance of **n8n** (Self-hosted or Cloud).
2. Appropriate credentials configured in n8n for:
   * **Google Gemini (PaLM) API** (for AI processing).
   * **Google Workspace OAuth2** (for Gmail, Sheets, Calendar, and Tasks).
   * **Telegram Bot API** (for the Telegram assistant).
   * **SerpAPI** (for the web search agent).

## 🚀 How to Import into n8n

1. Clone or download this repository to your local machine.
2. Open your n8n dashboard.
3. In the top right corner of the workflow canvas, click the **Options (three dots)** menu.
4. Select **Import from File...**
5. Choose the `.json` file of the workflow you wish to upload.
6. Reconnect your credentials inside the nodes, save, and activate the workflow!

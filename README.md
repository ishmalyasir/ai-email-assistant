#  AI Email Assistant

An AI-powered email automation project built with **n8n, Ollama, and Llama 3.2**. It helps manage emails by generating concise summaries, categorizing messages, detecting priority, and drafting professional replies.

##  Features

-  **Email Summarization:** Quickly understand long emails with concise summaries.
-  **Automatic Categorization:** Classifies emails into categories such as Support Request, Complaint, Sales Inquiry, and Other.
-  **Priority Detection:** Identifies emails as High, Medium, or Low priority.
-  **AI Reply Drafting:** Generates professional reply suggestions.
-  **Gmail Integration:** Creates reply drafts in Gmail instead of automatically sending them.
-  **Workflow Automation:** Connects email processing and AI analysis using n8n.

##  Tech Stack

- **Workflow Automation:** n8n
- **AI Model Runner:** Ollama
- **Language Model:** Llama 3.2 (1B)
- **Email Integration:** Gmail
- **Containerization:** Docker

##  How It Works

1. An email is received through the Gmail trigger.
2. The email content is passed to the AI workflow.
3. The model generates a summary, category, priority level, and suggested reply.
4. The workflow creates a Gmail draft for review.

**Note:** The workflow generates drafts for human review; it does not automatically send replies.

##  Setup

1. Install Docker Desktop and run n8n.
2. Install Ollama and download the model:

   ```bash
   ollama pull llama3.2:1b
   ```

3. Import `smart-email-assistant-public.json` into n8n.
4. Configure your Ollama Chat Model and Gmail credentials.
5. Set the Ollama connection URL to `http://host.docker.internal:11434` when n8n is running in Docker on Windows.
6. Test the workflow with sample emails before enabling automation.

##  Security

The public workflow file excludes credential references and instance-specific metadata. Configure your own credentials after importing the workflow. Never commit API keys, OAuth secrets, access tokens, or private email data.

##  Project Goal

This project explores practical AI integration, local language models, and no-code workflow automation to improve email productivity.

##  Author

**Ishmal Yasir**

## 📸 Project Screenshots

### 1. n8n Workflow
![AI Email Assistant Workflow](screenshots/workflow.png)

### 2. Gmail Reply Draft
![AI-Generated Gmail Draft](screenshots/gmail-draft.png)

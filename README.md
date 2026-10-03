# ai-lead-routing-engine
# AI-Driven Lead Qualification & Sales Routing Engine

An autonomous backend automation engine built in *n8n* that integrates *Google Gemini (LLM), **Gmail, and **Slack* to instantaneously ingest, analyze, qualify, and intelligently route incoming business leads based on project criteria, budget constraints, and intent classification.

## 🚀 Key Features
- *Deterministic Routing Architecture:* Implemented logic gates to segment inbound leads into three custom branches (HOT, WARM, COLD) based on automated criteria parameters.
- *Advanced LLM Inference Integration:* Utilizes the Google Gemini Flash API to securely parse raw lead messages and extract structured JSON metadata (qualification status, reasoning, and key pain points).
- *Automated Instant Personalization:* Generates dynamic, context-aware email responses sent instantly via the Gmail API to high-value (HOT) prospects.
- *Internal Ops Notifications:* Routes operational notifications via OAuth2 straight into active Slack communication streams for medium-value (WARM) project opportunities.
- *Spam Control Filtration:* Efficiently stops low-value or invalid lead assets via a No-Op filtering mechanism to maintain high domain and inbox reputations.

## 🛠️ Tech Stack & Integrations
- *Automation Framework:* n8n Cloud Orchestrator
- *Artificial Intelligence:* Google Gemini AI Model
- *Communications Stack:* Gmail API (SMTP/OAuth2), Slack Messaging Engine
- *Data Engineering:* JavaScript Core JSON Parsing Engine

## ⚙️ How It Works
1. *Webhook Trigger:* Ingests external JSON lead payloads containing user metrics (name, email, company, budget, message).
2. *AI Agent Assessment:* Passes parameters to a custom-prompted Gemini node returning exact structural objects.
3. *Switch Gateway:* Parses the string value dynamically using JSON.parse($json.output).status.
4. *Conditional Action Execution:* Delivers targeted external outreach or logs strategic internal notifications.

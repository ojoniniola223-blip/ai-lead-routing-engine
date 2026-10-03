# AI-Driven Lead Qualification, CRM Logging & Sales Routing Engine

An autonomous backend automation engine built in *n8n* that integrates *Google Gemini (LLM), **Airtable CRM, **Gmail, and **Slack* to instantaneously ingest, analyze, qualify, log, and intelligently route incoming business leads based on project criteria and budget constraints.

## 🚀 Key Features
- *Deterministic Routing Architecture:* Implemented logic gates to segment inbound leads into three custom branches (HOT, WARM, COLD) based on automated criteria parameters.
- *Advanced LLM Inference Integration:* Utilizes the Google Gemini Flash API to securely parse raw lead messages and extract structured JSON metadata (qualification status, reasoning, and key pain points).
- *Centralized CRM Ledger (Module 2):* Integrates an automated data logging tier via the Airtable API, ensuring 100% record persistence for lead profiles, budgets, and AI reasoning prior to final switch routing.
- *Automated Instant Personalization:* Generates dynamic, context-aware email responses sent instantly via the Gmail API to high-value (HOT) prospects.
- *Internal Ops Notifications:* Routes operational notifications via OAuth2 straight into active Slack communication streams for medium-value (WARM) project opportunities.
- *Spam Control Filtration:* Efficiently stops low-value or invalid lead assets via a No-Op filtering mechanism to maintain high domain and inbox reputations.

## 🛠️ Tech Stack & Integrations
- *Automation Framework:* n8n Cloud Orchestrator
- *Artificial Intelligence:* Google Gemini AI Model
- *Database / CRM Tier:* Airtable API Core
- *Communications Stack:* Gmail API (SMTP/OAuth2), Slack Messaging Engine
- *Data Engineering:* JavaScript Core JSON Parsing Engine

## ⚙️ How It Works
1. *Webhook Trigger:* Ingests external JSON lead payloads containing user metrics (name, email, company, budget, message).
2. *AI Agent Assessment:* Passes parameters to a custom-prompted Gemini node returning exact structural objects.
3. *CRM Logging:* Dynamically appends a new row to Airtable matching parsed data to 7 schema columns (Lead Name, Email Address, Company, Budget, AI Qualification Status, AI Analysis Reasoning, Extracted Pain Point).
4. *Switch Gateway:* Parses the string value dynamically using JSON.parse($json.output).status.
5. *Conditional Action Execution:* Delivers targeted external outreach or logs strategic internal notifications.

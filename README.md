# Autonomous AI Lead Engagement & Behavioral Tracking System

## 🚀 Overview
This project is an enterprise-grade automation engine built on **n8n**. It automates the entire lead lifecycle: from verification and initial outreach to tracking intent through behavioral signals and handling replies using Generative AI.

## 🧠 System Architecture
The engine consists of three core workflows designed to work in synchronization:

### 1. Intelligent Outreach Engine
- **Verification:** Integrated with **ZeroBounce API** to ensure 100% list hygiene before sending.
- **Dynamic Sequencing:** Multi-stage follow-up logic based on lead status.
- **Deliverability:** Implemented smart batching and human-like delays to maintain high sender reputation.

### 2. Multi-Layered Tracking Listener
- **Open Tracking:** Custom webhook listener for invisible 1x1 tracking pixels.
- **Click Redirector:** A specialized redirect logic that logs link engagement before sending leads to the booking page.
- **Booking Sync:** Real-time webhook integration with **Cal.com** to update conversion status.

### 3. AI Auto-Reply Agent
- **Autonomous Responses:** Uses **GPT-4o-mini** to analyze incoming lead queries (Pricing, Services, Slots).
- **Context-Aware:** Drafts and sends professional replies instantly based on a predefined company knowledge base.
- **Stop-Logic:** Automatically halts all outreach sequences once a reply or booking is detected.

## 🛠️ Tech Stack
- **Orchestration:** n8n
- **AI/LLM:** OpenAI API (GPT-4o-mini)
- **Email Infrastructure:** Microsoft Graph API (Outlook)
- **Database:** Google Sheets / Cloud Sync
- **Validation:** ZeroBounce API
- **Scheduling:** Cal.com

## ⚙️ Setup Instructions
1. Import the provided `.json` workflow files into your n8n instance.
2. Configure the Environment Variables for OpenAI, ZeroBounce, and Microsoft Azure.
3. Update the Spreadsheet ID in the Google Sheets nodes to match your lead database.
4. Set the Webhook URLs in the tracking nodes.

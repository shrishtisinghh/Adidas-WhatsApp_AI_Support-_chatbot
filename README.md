🤖 Adidas WhatsApp AI Chatbot — Alex

An intelligent WhatsApp customer support assistant built with n8n, Twilio, Groq (LLM), and Airtable — no backend code required.


📌 Overview

Alex is an AI-powered WhatsApp chatbot designed for Adidas customer support. It handles real customer queries end-to-end: from answering return policies to tracking orders and logging support tickets — all through WhatsApp.


✨ Features


💬 FAQ Handling — Answers return policy, shipping info, and store hours from a knowledge base
📦 Order Tracking — Fetches real-time order status from Airtable using Order ID
🗂️ Support Ticket Creation — Logs customer issues directly into Airtable with auto-assignment
🛍️ Product & Inventory Lookup — Queries live inventory data filtered by price and product name
⚡ Powered by Groq LLM — Fast inference using openai/gpt-oss-120b via Groq API
📲 WhatsApp via Twilio — Receives and sends messages through Twilio's WhatsApp sandbox



🛠️ Tech Stack

ToolPurposen8nWorkflow automationTwilioWhatsApp messagingGroq APILLM inference (GPT-OSS 120B)AirtableDatabase (Orders, Inventory, Tickets)n8n AI AgentOrchestrates tools and LLM


🏗️ Workflow Architecture

Incoming WhatsApp Message (Twilio)
        ↓
  Set Return Policy (Knowledge Base)
        ↓
     AI Agent (Groq LLM)
    ↙    ↓    ↓    ↘
order  order  create  return
records tracking tickets policy
        ↓
Send WhatsApp Reply (Twilio)

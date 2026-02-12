# telegram-clickup-ai-bot

# Telegram → ClickUp AI Bot

AI-powered automation that allows managing ClickUp tasks directly from Telegram using natural language and voice messages.

This project is built with **n8n**, **Telegram Bot API**, **ClickUp API**, and **OpenAI**, enabling users to create, update, comment on, and manage ClickUp tasks without opening ClickUp itself.

---

## 🚀 Features

- 📩 Manage ClickUp directly from Telegram
- 🧠 Natural language understanding using OpenAI
- 🎙 Voice message transcription (speech-to-text)
- ✅ Create, update, delete ClickUp tasks
- 💬 Add, update, delete comments
- 📋 Manage checklists and checklist items
- 📎 Attach files from Telegram to ClickUp tasks
- 👥 Automatic assignee detection via Google Sheets
- 🔍 Smart search for spaces, folders, lists, and tasks
- 🔄 Context memory per Telegram chat

---

## 🛠 Tech Stack

- **n8n** — workflow automation
- **Telegram Bot API** — user interaction
- **ClickUp API** — task management
- **OpenAI (GPT-4 / GPT-4.1-mini)** — intent detection & text understanding
- **Google Sheets API** — team member mapping
- **LangChain (n8n nodes)** — AI agent & memory

---

## 🧠 How It Works

1. User sends a message (text, voice, or file) in Telegram
2. Telegram Trigger receives the update in n8n
3. Message type is detected:
   - Text → processed directly
   - Voice → downloaded and transcribed using OpenAI
   - File → prepared for attachment
4. AI Agent analyzes the request and determines the action:
   - create task
   - update task
   - add comment
   - manage checklist
   - attach file
5. Required ClickUp entities (space, folder, list, task) are resolved automatically
6. Corresponding ClickUp API action is executed
7. Confirmation message is sent back to Telegram

---

## 🧩 Supported Actions

- Create / update / delete tasks
- Add / update / delete comments
- Create / update / delete checklists
- Manage checklist items
- Attach files to tasks
- Assign users and set priorities
- Set due dates (ISO 8601)

---

## 📂 Project Structure

This repository contains:

- n8n workflow export (`.json`)
- AI Agent prompt logic
- ClickUp API integration via HTTP tools
- Telegram triggers and responders
- Google Sheets member lookup
- Context memory per chat session

---

## ⚙️ Setup Requirements

To run this project you need:

- n8n instance (self-hosted or cloud)
- Telegram Bot token
- ClickUp OAuth2 credentials
- OpenAI API key
- Google Sheets with team members (name ↔ ClickUp ID mapping)

---

## 📌 Use Case

This bot is ideal for teams who:
- Actively use ClickUp
- Communicate in Telegram
- Want fast task management without switching tools
- Prefer voice or natural language commands

---

## 🧪 Example Commands

- “Create task Fix login bug, due tomorrow”
- “Add comment to task Landing Page”
- “Assign task API Integration to Nikita”
- “Delete checklist Deployment steps”
- Voice message: “Create a task to update documentation”

---

## 📜 License

MIT License

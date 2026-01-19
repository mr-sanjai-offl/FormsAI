# 📋 FormsAI - Agentic Google Forms Assistant

> **From Problem to Solution:** A powerful Chrome Extension that transforms natural language into fully-functional Google Forms using AI, Google Apps Script, and Agentic Workflows.

![FormsAI Banner](https://img.shields.io/badge/Status-Production%20Ready-success) ![Tech Stack](https://img.shields.io/badge/Tech-Chrome%20Ext%20%7C%20Gemini%20AI%20%7C%20Apps%20Script-blue)

## 💡 The Story: Why I Built This

As a developer and student, I frequently faced the tedious task of creating Google Forms for events, surveys, and data collection. The process was always the same:
1.  Manually drag-and-drop fields.
2.  Copy-paste questions one by one.
3.  Manually configure settings and link spreadsheets.
4.  Struggle with file upload permissions.

**The Problem:** There was no tool that could "just understand" what I needed and build it instantly. Existing bulk creators were rigid and required CSV templates.

**The Solution:** I decided to build **FormsAI** to solve this. I combined my knowledge of **modern web technologies** with **Generative AI** to create an "Agentic" assistant. Instead of just taking commands, it understands context, asks clarifying questions, and handles the complex API limitations of Google's ecosystem (like the inability to create file uploads via REST API) by engineering a custom Apps Script backend.

This project represents my journey of identifying a real-world friction point and engineering a robust, technical solution.

---

## ✨ Key Features

### 🤖 Agentic AI Workflow
Unlike basic generators, FormsAI creates a conversation:
*   **Context Awareness:** Understands fuzzy requirements (e.g., "college admission form").
*   **Clarifying Questions:** If details are missing, the AI asks specific questions ("What is the event date?", "Should we collect emails?") before generating.
*   **Professional Formatting:** Automatically applies Title Case, emojis, and structured descriptions.

### 🚀 Hybrid Automation Engine
I architected a dual-mode system to overcome API limitations:
1.  **REST API Mode:** Fast creation for standard forms.
2.  **Apps Script Backend:** A custom deployed Web App that handles advanced features like **File Uploads** and **Automatic Sheet Linking** which are otherwise impossible via the standard Google Forms API.

### 🛠️ Production-Grade Features
*   **Persistent Side Panel:** Stays open while you multitask across tabs.
*   **Instant Sheet Linking:** Automatically creates and links a Google Sheet for responses.
*   **Smart Fallbacks:** Gracefully handles API quotas and auth errors.

---

## 🏗️ Technical Architecture

This project leverages a sophisticated stack to deliver a seamless experience:

*   **Frontend:** HTML5, CSS3 (Modern Variables & Flexbox), Vanilla JavaScript (ES6+ modules).
*   **Extension Core:** Chrome Manifest V3, Side Panel API, Service Workers.
*   **AI Intelligence:** Google Gemini 2.0 Flash (via OpenRouter) for high-speed, context-aware generation.
*   **Backend Integration:**
    *   **Google Forms/Drive/Sheets REST APIs:** For metadata and folder management.
    *   **Google Apps Script:** Custom `doPost()` webhook to bypass REST API limitations for file upload fields.
*   **Authentication:** Google OAuth 2.0 with granular scope management.

---

## 📸 How It Works

1.  **Open the Extension:** Click the side panel icon.
2.  **Describe Your Needs:** Type "Create a registration form for a Hackathon".
3.  **Agent Interaction:** The AI might ask, "Do you need a team size field?". You answer.
4.  **Generation:** The AI constructs a JSON schema.
5.  **Execution:** The backend builds the form, adds all fields (including file uploads), creates a response spreadsheet, and links them together.
6.  **Ready:** You get a shareable link instantly.

---

## 🚀 Installation & Setup

1.  **Clone the Repository**
    ```bash
    git clone https://github.com/yourusername/FormsAI.git
    ```

2.  **Configure API Keys**
    *   Get an OpenRouter API key.
    *   (Optional) Deploy the `apps-script/FormsAI-Backend.gs` code to Google Apps Script and copy the web app URL.

3.  **Load into Chrome**
    *   Go to `chrome://extensions/`.
    *   Enable "Developer Mode".
    *   Click "Load Unpacked" and select the project folder.

4.  **Update Config**
    *   Open `background.js` and paste your API keys (or implement the settings UI).

---

## 🎯 Future Improvements

*   [ ] Add template library for common use cases.
*   [ ] Voice input for form description.
*   [ ] AI analysis of form responses.

---

**Developed with my knowledge and AI by Sanjai S**
*Solving real problems with code.*

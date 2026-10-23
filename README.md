# 📧 AI Email Agent

An AI-powered email automation project built using **Python, LangChain, Groq, and SMTP**. The agent uses an LLM to understand user requests and can invoke an email-sending tool to compose and send emails programmatically.

## 🚀 Features

- 🤖 AI-powered email assistance
- ✉️ Automated email sending through SMTP
- 🔗 LangChain tool integration
- 🧠 LLM-powered request processing using Groq
- 🔐 Environment variable management for credentials
- ⚙️ Modular and extensible tool-based architecture

## 🛠️ Tech Stack

| Technology | Purpose |
|---|---|
| Python | Core programming language |
| LangChain | Agent and tool integration |
| Groq API | Language model inference |
| SMTP | Email delivery |
| `email.mime` | Constructing email messages |
| `python-dotenv` | Loading environment variables |

## 🏗️ Project Workflow

```text
User Request
     |
     v
AI Agent (LLM)
     |
     v
Understand Email Task
     |
     v
Email Sending Tool
     |
     v
SMTP Server
     |
     v
Recipient's Inbox
```

## 📂 Project Structure

```text
03_email_agent/
│
├── agent.py          # AI agent initialization
├── tools.py          # Email sending tool
├── app.py            # Application entry point (if used)
├── .env              # API keys and email credentials
├── .gitignore        # Files excluded from Git
├── requirements.txt  # Python dependencies
└── README.md         # Project documentation
```

*Adjust the filenames to match your actual project.*

## ⚙️ Installation and Setup

### 1. Clone the Repository

```bash
git clone <your-github-repository-url>
cd 03_email_agent
```

Replace the placeholder with your actual GitHub repository URL.

### 2. Create a Virtual Environment

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.venv\Scripts\Activate.ps1
```

### 3. Install Dependencies

```bash
pip install langchain langchain-groq python-dotenv
```

Install any additional packages required by your agent implementation.

### 4. Configure Environment Variables

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_groq_api_key
MODEL=your_supported_groq_model_name

SENDER_EMAIL=your_email@example.com
SENDER_EMAIL_PASSWORD=your_email_app_password
```

Replace the example values with your actual credentials.

- Obtain your Groq API key from the [Groq Console](https://console.groq.com/).
- For Gmail, use an **App Password** where supported, rather than your regular account password. App Passwords require two-step verification.

Keep all credentials private. Never commit `.env` to GitHub.

### 5. Run the Project

Run the script that initializes your agent:

```bash
python agent.py
```

If your email tool has a separate test script, run it according to your implementation.

## 🧠 How It Works

1. **User Input:** The user provides an email-related request.
2. **LLM Processing:** The Groq-hosted language model interprets the request.
3. **Tool Selection:** The LangChain agent can select the email tool when appropriate.
4. **Email Construction:** Python prepares the message using email utilities.
5. **Email Delivery:** The SMTP server attempts to send the email.
6. **Result Handling:** The application reports the result of the sending operation.

## 🔒 Security Best Practices

- Store API keys and email credentials in environment variables.
- Never expose passwords or API keys in source code or logs.
- Validate recipient addresses and email content.
- Handle SMTP authentication and connection errors.
- Require user confirmation before sending consequential or externally addressed emails.
- Use a dedicated email account for development and testing.

## 🔮 Future Enhancements

- Generate email subjects and bodies from natural-language requests.
- Support multiple recipients and CC/BCC.
- Add email preview and confirmation before sending.
- Build a Streamlit interface for email generation.
- Add delivery error handling and structured logs.
- Support email templates for professional communication.

## 👩‍💻 Author

**Pratiksha Bhagat**

AI Developer | Python | LangChain | Generative AI | AI Agents

## 📄 License

This project is intended for educational and portfolio use. Add an appropriate open-source license if you plan to distribute it.

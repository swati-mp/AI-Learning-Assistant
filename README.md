# AI Learning Assistant 

## Project Overview

The **AI Learning Assistant** is a web-based application built using Python, Streamlit, and the Groq API. It provides a simple interface for interacting with an AI chatbot.

The application includes two modes:

1. **Chat Assistant:** Answers questions about Python, Generative AI, and other learning topics.
2. **College FAQ:** Answers questions using predefined information about a college AI workshop.

## Objectives

- Build an interactive web application using Streamlit.
- Integrate an AI model using the Groq API.
- Maintain conversation history using session state.
- Create a chatbot with custom system instructions.
- Answer questions using provided FAQ information.
- Implement basic input validation and AI safety practices.
- Use Git and GitHub for version control and code sharing.

## Technologies Used

- Python
- Streamlit
- Groq API
- python-dotenv
- Git
- GitHub

## Features

### 1. Interactive Chat Interface
Users can enter questions and view AI-generated responses through a chat interface.

### 2. Conversation Memory
The application uses `st.session_state` to maintain recent messages during the active session.

### 3. Custom AI Persona
System instructions define the assistant's role, tone, and expected behavior.

### 4. College FAQ Assistant
Users can ask questions about a predefined college AI workshop. The assistant is instructed to answer using the provided FAQ context.

### 5. Input Validation
The application checks user input and applies basic length restrictions.

### 6. Basic AI Safety
The application includes instructions intended to reduce unsupported answers and resist attempts to override its FAQ instructions.

### 7. Secure API Configuration
The API key is loaded from a local `.env` file and is kept separate from the application source code.

## Project Structure

```text
Day5_AI_Powered_Applications/
│
├── app.py
├── 01_streamlit_basics.py
├── requirements.txt
├── README.md
├── .gitignore
├── .env
└── .venv/
```

**Note:** Do not upload `.env` or `.venv/` to GitHub.

## Prerequisites

- Python 3.10 or newer
- Visual Studio Code or another Python editor
- Internet connection
- Groq account and API key
- Git installed

## Installation and Setup

### Step 1: Clone the repository

```bash
git clone https://github.com/YOUR_USERNAME/Day5-AI-Learning-Assistant.git
cd Day5-AI-Learning-Assistant
```

Replace `YOUR_USERNAME` with your GitHub username and use your actual repository URL.

### Step 2: Create a virtual environment

```bash
python -m venv .venv
```

Activate it on Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

### Step 3: Install dependencies

```bash
python -m pip install -r requirements.txt
```

### Step 4: Configure the API key

Create a `.env` file in the project folder:

```dotenv
GROQ_API_KEY=your_actual_groq_api_key
GROQ_MODEL=openai/gpt-oss-20b
```

Replace the placeholder with your actual API key. Ensure the model is available to your Groq account.

**Security:** Never upload your API key to GitHub or share it publicly.

### Step 5: Run the application

Run the main AI Learning Assistant:

```bash
python -m streamlit run app.py
```

Open the local URL displayed in the terminal in your web browser.

## How to Use the Application

1. Open the application in your browser.
2. Select **Chat Assistant** or **College FAQ** from the sidebar.
3. Enter your question in the chat input.
4. Read the AI-generated response.
5. Ask follow-up questions to test conversation memory.
6. In College FAQ mode, ask questions about the supplied workshop information.
7. Click **Clear conversation** to clear the current conversation.

## Example Questions

### Chat Assistant

- What is Python?
- Explain Generative AI in simple words.
- What is the difference between AI and machine learning?
- Give me a beginner-friendly Python example.

### College FAQ

- How many days is the workshop?
- Which programming language is used?
- What topics are covered?
- What is the workshop fee?

If the information is not available in the FAQ, the assistant is instructed to indicate that it could not find the answer in the provided information.

## Security and Responsible AI

- Keep API keys separate from source code.
- Add `.env` to `.gitignore`.
- Validate user input before sending it to the AI model.
- Treat user messages and FAQ content as untrusted input.
- Do not assume system instructions completely prevent prompt injection.
- Verify AI-generated responses when accuracy is important.
- Avoid sharing confidential information with external AI services without appropriate permission.

## Limitations

- AI-generated responses may be inaccurate.
- FAQ answers depend on the information provided.
- Conversation history is temporary and is not stored permanently.
- The application requires internet access and a working API key.
- Model availability and API usage limits depend on the provider and account.

## Future Improvements

- Add PDF and text document question answering.
- Add conversation export and persistent storage.
- Add user authentication.
- Improve document retrieval and source citations.
- Add multilingual question answering.
- Improve error handling and logging.

## Learning Outcomes

After completing this project, students should understand how to:

- Create web interfaces using Streamlit.
- Integrate an AI model through an API.
- Maintain conversation history using session state.
- Build a context-based FAQ assistant.
- Apply basic input validation and responsible AI practices.
- Manage source code using Git and GitHub.



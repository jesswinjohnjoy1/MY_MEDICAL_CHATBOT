 Medical Chatbot (Streamlit + Groq API)
 Overview

    The Medical Chatbot is a web-based application built with Streamlit that allows users to securely interact with an intelligent medical instrument classifier chatbot powered by the Groq API (LLaMA 3.3-70B model).
    Users can sign up, log in, reset passwords, and maintain individual chat histories stored locally in JSON files.
    The chatbot provides safe, professional, and medically-relevant responses — identifying instruments or devices based on user descriptions while ensuring data privacy and user control.

 Features
    User Authentication
    Sign Up with:
    Username
    Password (with confirmation)
    Secret question & answer (used for password recovery)
    Login / Logout functionality
    Forgot Password:
    Users can reset their password securely by answering their secret question.

 Chatbot

    Powered by Groq LLaMA 3.3-70B model
    Responds only to medical-related questions
    Classifies medical instruments into categories:
    Diagnostic
    Surgical
    Laboratory
    Therapeutic
    Imaging
    Patient Monitoring
    Dental
    Provides structured JSON-based answers with:
    Category
    Reason for classification
    Likely instrument name
    Confidence score
    Smart Interface
    Real-time streaming responses from the AI model
    Chat history stored per user in chat_history.json

Supports:

    New Chat creation
    Chat clearing
    Individual message deletion
    Persistent chat sessions per user

 Project Structure:
  MY_MEDICAL_CHATBOT/
│
├── app.py                # Main Streamlit app
├── users.json            # Stores registered users & credentials
├── chat_history.json     # Stores chat sessions for each user
├── requirements.txt      # Required dependencies
└── README.md             # Project documentation

Installation & Setup
1️ Clone the Repository
    git clone https://github.com/jesswinjohnjoy1/MY_MEDICAL_CHATBOT.git
    cd medical-chatbot


2 Install Dependencies
    Create a requirements.txt file (if not already present):
        streamlit
        groq

    Then install:
        pip install -r requirements.txt

3 Set Your Groq API Key

    Obtain your API key from https://console.groq.com/keys
    and set it as an environment variable:

    Windows (PowerShell)
    setx GROQ_API_KEY "your_api_key_here"

    macOS/Linux
    export GROQ_API_KEY="your_api_key_here"

4 Running the App

    Run the Streamlit application:

    streamlit run app.py


Then open your browser at:

http://localhost:8501

 Data Storage

    users.json → Stores user credentials and secret questions securely.

    chat_history.json → Keeps all user chat sessions, messages, and AI responses.

    Each user’s data is isolated and accessible only after login.

 Technologies Used
    Component	Description
    Frontend	Streamlit
    Backend / Logic	Python
    AI Model	LLaMA 3.3-70B (via Groq API)
    Data Storage	JSON files (users.json, chat_history.json)



 Example Chat

    User Input:

        Used for measuring blood pressure

    Chatbot Response (Markdown):

        {
        "original_input": "Used for measuring blood pressure",
        "category": "Diagnostic",
        "reason": "Measures blood pressure to assess cardiovascular status.",
        "likely_instrument": "Sphygmomanometer (blood pressure cuff)",
        "confidence": 92
        }


Summary:
    This is a Diagnostic instrument — likely a sphygmomanometer.

    🧹 Additional Features

    🧹 Clear Chat: Erases all messages from the current session.

    🗑️ Delete Message: Remove specific user messages (and their corresponding bot replies).

    ➕ New Chat: Start a fresh conversation thread.


👨‍💻 About Author
    NAME=Jesswin Anto J
    EMAIL=jesswinjohnjoy1@gmsil.com


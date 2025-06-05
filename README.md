# H-AI-R: Automating HR Email Responses with AI

**H-AI-R** is an intelligent automation system designed to streamline HR email communications using large language models (LLMs). It connects seamlessly with Gmail, enabling AI-powered reading, interpretation, and response generation for HR-related messages—all in real time.

## 🚀 Key Features

- 📥 **Gmail Integration**: Automatically fetch and respond to emails from your HR inbox  
- 🤖 **AI-Powered Agent**: Uses advanced natural language processing to understand and reply to complex queries  
- 🔒 **Secure Authentication**: Integrated with Firebase for secure access and real-time updates  
- 🐳 **Docker Support**: Easily deploy the entire application with Docker  
- 🧠 **LLM-Driven Intelligence**: Built using OpenAI's GPT models and LangChain for contextual reasoning

## 🛠 Tech Stack

- Python (Flask)
- LangChain + OpenAI
- Gmail API
- Firebase
- Docker

## 📁 Project Structure

```
.
├── app.py                 # Entry point for the Flask application
├── hr_ai_agent.py         # Core logic for email understanding and generation
├── hr_ai_agent_project.py # Prompt templates and agent orchestration
├── gmail_watch.py         # Gmail webhook listener and handler
├── firebase_config.py     # Firebase admin SDK setup
├── database.py           # Firestore interaction layer
├── Dockerfile            # Docker configuration
├── requirements.txt      # Python package requirements
```

## ⚙️ Getting Started

### 1. Clone the repository

```bash
git clone https://github.com/yourusername/H-AI-R.git
cd H-AI-R
```

### 2. Install dependencies

```bash
pip install -r requirements.txt
```

### 3. Configure Gmail API

1. Create a Google Cloud project and enable the Gmail API
2. Download your credentials.json and place it in the project root

### 4. Set up Firebase

1. Follow the configuration steps in firebase_config.py
2. Ensure you have a service account key file for Firebase admin access

### 5. Run the application

```bash
python app.py
```

### 6. (Optional) Run with Docker

```bash
docker build -t hair-app .
docker run -p 5000:5000 hair-app
```

## 📬 How It Works

1. A new email arrives in the connected Gmail inbox
2. The Gmail webhook triggers processing
3. The AI agent analyzes the message context
4. A response is generated and sent back via Gmail
5. All activity is logged to Firebase for traceability and analytics

## 🔐 Environment Variables

Create a `.env` file in the root directory with the following variables:

```env
OPENAI_API_KEY=your_openai_api_key
FIREBASE_CREDENTIALS_PATH=path_to_firebase_credentials.json
GMAIL_CREDENTIALS_PATH=path_to_gmail_credentials.json
```

## 📝 License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

## 📧 Contact

For any questions or concerns, please open an issue in the GitHub repository.

# Neovis-Registered-User-App
# Hotel Property Chatbot

A Streamlit-based intelligent chatbot application that provides property-specific information to registered hotel users. The application features secure authentication, conversation management, and customer service transfer capabilities.

## Features

- **Secure User Authentication**: Login system for registered hotel users
- **Property-Specific Information**: Dynamic responses based on property ID
- **Conversation Management**: Complete chat history tracking and storage
- **Real-time Chat Interface**: Interactive chat UI powered by Streamlit
- **Customer Service Transfer**: Seamless transfer to human agents when needed
- **Session Management**: Tracks user sessions and conversation duration
- **Database Integration**: MySQL backend for storing chat history and user sessions

## Tech Stack

- **Frontend**: Streamlit
- **Backend**: FastAPI, Python
- **Database**: MySQL
- **AI Model**: Google Gemini 1.5 Pro
- **Vector Database**: ChromaDB
- **ORM**: SQLAlchemy

## Prerequisites

- Python 3.8+
- MySQL Server
- ChromaDB
- Required Python packages (see requirements.txt)

## Installation
git clone <repository-url>



## Install required packages:
pip install -r requirements.txt


## Set up MySQL database and update the connection string in `Database.py`:
Before Executing below make sure you create Conversations database in your MySQL Workbench
DATABASE_URL = "mysql+pymysql://username:password@localhost:3306/Conversations"

## Configure your Gemini API key in `chatbot_app.py`:
GEMINI_API_KEY = "your-api-key-here"


## Database Schema

The application uses three main tables:

1. **Session_table_2**
   - Tracks user sessions
   - Stores session duration and status
   - Links to chat history and transfers

2. **Chat_table**
   - Stores all chat messages
   - Tracks message status and timestamp
   - Links messages to sessions

3. **chat_transfer_table**
   - Manages customer service transfers
   - Records transfer reasons and timestamps
   - Links transfers to sessions

## Usage

1. Start the application:
streamlit run chatbot_app.py


2. Login with your credentials:
   - Email
   - Password
   - Property ID

3. Start chatting with the bot about property-specific information

4. Request customer service transfer if needed

## Features in Detail

### Authentication
- Secure login system
- Session-based user management
- Role-based access control

### Chat Interface
- Real-time message updates
- Chat history persistence
- Message status tracking
- Timestamp recording

### Customer Service
- Automated transfer capability
- Transfer reason logging
- Agent assignment tracking

### Data Management
- Conversation history storage
- Session duration tracking
- Property-specific context retrieval via ChromaDB

## Contributing

Please read [CONTRIBUTING.md](CONTRIBUTING.md) for details on our code of conduct and the process for submitting pull requests.

## License

This project is licensed under the MIT License - see the [LICENSE.md](LICENSE.md) file for details.

## Acknowledgments

- Google Gemini API for AI capabilities
- Streamlit for the interactive web interface
- ChromaDB for vector storage

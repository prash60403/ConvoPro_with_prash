# AI Chatbot Project

## Introduction

This project is an AI-powered chatbot application developed using Python, MongoDB, Ollama models, and Streamlit. The chatbot allows users to communicate with AI models through an interactive user interface while storing all conversations inside a MongoDB database. The project follows a modular architecture where each file handles a specific responsibility such as database management, language model initialization, conversation handling, and frontend interface development.

---

# Project Workflow

The project workflow starts with installing MongoDB and Ollama. MongoDB is used to store conversation history, user messages, timestamps, and chat details, while Ollama is used to run local Large Language Models (LLMs) that generate AI responses.

After installation, the required Ollama models are initialized. These models are responsible for understanding user prompts and generating intelligent responses inside the chatbot application.

Next, a `.env` file is created to securely store important configuration details such as MongoDB URL, database name, Ollama server URL, and Ollama model names. This helps separate sensitive configurations from the main application code.

The project then loads all environment variables using the `settings.py` configuration file. This file acts as the central configuration manager and allows all modules in the project to access required settings easily.

Inside the database layer, the `mongo.py` file is responsible for establishing the connection between Python and MongoDB. It helps access collections and manage database operations throughout the project.

The `conversations.py` file manages all chatbot conversation functionalities. It handles operations such as creating conversation IDs, creating new conversations, storing messages, retrieving chat history, and displaying conversation lists.

The `llm_factory.py` file initializes Ollama language models and connects the chatbot system with the selected AI models. This file helps load models dynamically whenever user input is processed.

Inside the services layer, additional chatbot functionalities are implemented. The `chat_title.py` file generates conversation titles that appear in the sidebar. The `chat_model_list.py` file stores available Ollama models for model selection. The `chat_utility.py` file handles the main chatbot processing logic, including sending prompts to the AI model, receiving responses, and storing chat data in MongoDB.

The `main.py` file acts as the main execution pipeline of the project. Using Streamlit, it builds the chatbot frontend interface, manages session states, displays conversation history, and integrates all project modules together. Whenever a user sends a message, the chatbot processes the request through the AI model, stores the response in MongoDB, and updates the user interface dynamically.

---

# Technologies Used

| Technology | Purpose                         |
| ---------- | ------------------------------- |
| Python     | Backend development             |
| MongoDB    | Database storage                |
| Ollama     | Local AI model execution        |
| Streamlit  | Frontend user interface         |
| dotenv     | Environment variable management |

---

# Main Components

## MongoDB

MongoDB is used as the database system for storing chatbot conversations, user prompts, AI responses, timestamps, and chat history. It provides flexible document-based storage suitable for chatbot applications.

---

## Ollama

Ollama is used to run local Large Language Models (LLMs). These models generate AI-based responses for user queries and provide natural language understanding capabilities to the chatbot.

---

## Environment Configuration

The `.env` file stores important project configurations such as database URLs and model details. This improves security and simplifies project management.

---

## Configuration Layer

The `settings.py` file loads and manages all environment variables so that every module can access project configurations centrally.

---

## Database Layer

The `mongo.py` file establishes the connection between the Python application and MongoDB. It manages database collections and provides reusable database access functions.

---

## Conversation Management

The `conversations.py` file handles all conversation-related operations including creating conversations, storing messages, retrieving history, and managing conversation IDs.

---

## Language Model Factory

The `llm_factory.py` file initializes Ollama models and provides functions for loading AI language models dynamically during chatbot execution.

---

## Services Layer

The services layer contains reusable utility functions used throughout the project. It manages chatbot titles, available model lists, and AI response processing.

---

## Main Application

The `main.py` file integrates all project modules together and runs the Streamlit chatbot application. It manages user interaction, session states, chat history, and frontend rendering.

---

# Advantages of the Project

* Supports local AI model execution
* Stores complete conversation history
* Provides multiple AI model selection
* Uses modular project architecture
* Easy to maintain and extend
* Interactive chatbot user interface

---

# Conclusion

This project successfully demonstrates the integration of MongoDB, Ollama, and Streamlit to create a complete AI chatbot application. The system efficiently handles AI response generation, conversation management, and database storage while maintaining a clean and scalable project architecture. The project can be further enhanced with features such as authentication, cloud deployment, multi-user support, and advanced AI capabilities.

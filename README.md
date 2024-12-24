# Enhanced NLP Chatbot

## Overview
This project is an **Enhanced NLP Chatbot** that provides natural language understanding and intelligent responses to user queries. The chatbot includes both a graphical user interface (GUI) and a machine learning model trained on predefined intents. The system is designed for use in various contexts, such as fitness, health advice, and general queries.

## Features
- **Graphical User Interface**:
  - User-friendly interface built with Tkinter.
  - Display of chat history with user and bot messages.
  - Special commands for web search and time fetching.
  - Options to save and clear chat history.

- **Machine Learning Integration**:
  - Trained using a TensorFlow neural network.
  - Recognizes user intents and responds with predefined answers.
  - Uses `intents.json` for input patterns and responses.

- **Predefined Intents**:
  - Supports categories like greetings, creator information, injury treatments, fitness advice, and more.

## File Structure

### 1. `gui1.py`
- Provides the graphical user interface for the chatbot.
- Key Functions:
  - **Chat History**: Displays conversation between user and bot.
  - **Special Commands**: Allows searches, time queries, and bot responses.
  - **Chat Saving**: Saves conversation history to a text file.

### 2. `intents.json`
- Contains the training data for the chatbot.
- Organized into intents, each with:
  - **Tag**: Identifier for the intent.
  - **Patterns**: User inputs recognized by the bot.
  - **Responses**: Replies generated for recognized patterns.
- Example:
  ```json
  {
    "tag": "greeting",
    "patterns": ["Hi there", "Hello"],
    "responses": ["Hello! How can I assist you today?", "Hi there!"]
  }
  ```

### 3. `main.py`
- Script for training the chatbot model.
- Key Steps:
  - Preprocesses text data by tokenizing and lemmatizing.
  - Builds a neural network using TensorFlow.
  - Trains the model on patterns and responses from `intents.json`.
  - Saves the trained model as `chatbot_model.h5`.

## Setup Instructions

### Prerequisites
- Python 3.8+
- Required libraries:
  - `tensorflow`
  - `nltk`
  - `numpy`
  - `pickle`
  - `tkinter`
  - `keras`

### Installation
1. Clone the repository:
   ```bash
   git clone https://github.com/YourUsername/NLP-BOT.git
   cd NLP-BOT
   ```

2. Install the required libraries:
   ```bash
   pip install -r requirements.txt
   ```

3. Download the necessary NLTK data:
   ```python
   import nltk
   nltk.download('punkt')
   nltk.download('wordnet')
   ```

4. Train the chatbot:
   ```bash
   python main.py
   ```

5. Run the chatbot GUI:
   ```bash
   python gui1.py
   ```

## Usage
1. Start the chatbot GUI by running `gui1.py`.
2. Interact with the bot through the chat window:
   - Type your message and press **Enter** or click **Send**.
   - Use special commands like:
     - `search <query>`: Opens a web search for the given query.
     - `time`: Displays the current time.
     - `exit` or `bye`: Ends the conversation.
3. Save or clear chat history using the buttons provided.

## Contributing
Feel free to contribute by submitting issues or pull requests to enhance the chatbot’s functionality and add new features.

## License
This project is licensed under the MIT License. See the LICENSE file for details.

## Author
Created by **Gurram Vardhan**. Passionate about AI and ML, and always eager to learn and innovate!


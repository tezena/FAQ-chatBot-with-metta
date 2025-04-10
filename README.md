# MeTTa Knowledge Chatbot with Gemini Integration 

A context-aware chatbot that combines structured knowledge representation in MeTTa with Google Gemini's natural language capabilities.

## Features

- **Knowledge Representation**: Structured domain knowledge using MeTTa language
- **Querying**: Simple relationship extraction from knowledge base
- **LLM Integration**: Google Gemini for natural language understanding
- **Web Interface**: Flask-based REST API for easy integration
- **Demographic Analysis**: Built-in queries for human attributes and relationships

## Prerequisites

- Python 3.10+
- Google Gemini API key
- MeTTa/Hyperon environment

## Installation

1. Clone the repository:
   ```bash
   git clone https://github.com/tezena/FAQ-chatBot-with-metta.git
   cd metta-chatbot 
   ```

2. Create and activate virtual environment:
   ```bash
   python -m venv venv
   source venv/bin/activate  # Linux/Mac
   venv\Scripts\activate     # Windows
   ```
3. Install dependencies
   ```bash 
   pip install -r requirements.txt 
   ```
4. Set up environment variables:
  ```bash
     echo "GEMINI_API_KEY=your_api_key_here" > .env
  ```
  
### Project Structure
```
faqchatBot-with-metta-chatbot/
├── app.py                 # Flask application entry point
├── model/
│   ├── __init__.py
│   ├── gemini_model.py    # Gemini LLM integration
│   └── metta_queries.py   # MeTTa knowledge base handler
├── metta_knowledge/
│   ├── knowledge.metta    # Domain-specific facts
│   └── queries.metta      # Queries
├── requirements.txt       # Dependencies
└── README.md 
```
## usage
1. Start the Flask server:
   ```
   python app.py 
   ```
2. Send queries to the API:
   ```bash
   curl -X POST http://127.0.0.1:8000/chat \
   -H "Content-Type: application/json" \
   -d '{"message": "Who are the male soda drinkers?"}'
```
## Example Queries
"List all women in the knowledge base"

"Who are the soda drinkers?"

"What do you know about Allen?"

"How many ugly men are there?"

"Compare male and female soda drinkers"
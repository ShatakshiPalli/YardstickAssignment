# Yardstick Assignment

This Jupyter Notebook demonstrates techniques for managing, summarizing, and extracting structured information from conversational chat history using the Groq OpenAI-compatible API and JSON Schema validation.

## Features

- **Conversation Management:**  
  The `ConversationManager` class helps manage chat history, including truncation by number of turns, character count, or word count, and supports periodic summarization.

- **Summarization:**  
  The notebook uses the Groq API to summarize conversation history into concise bullet points, with fallback logic if the API key is not set.

- **Structured Data Extraction:**  
  Demonstrates extracting structured contact information (name, email, phone, location, age) from free-form chat using function-calling (tool-calling) with the Groq API, validated against a JSON Schema.

- **Validation:**  
  Extracted data is validated using the `jsonschema` library to ensure it matches the expected schema.

## Requirements

- Python 3.7+
- `openai==0.28`
- `jsonschema`
- (Optional) Google Colab for `userdata` secrets

## Setup

1. Install dependencies (automatically handled in the first cell):
    ```python
    !pip install --quiet jsonschema
    !pip install openai==0.28
    ```

2. Set your Groq API key and base URL in Colab secrets:
    - `GROQ_API_KEY`
    - `OPEN_API_BASE`

## Usage

- Run all cells in order.
- The notebook will:
  - Simulate a conversation and show truncation/summarization examples.
  - Extract contact information from sample chats and validate the results.

## File Structure

- `Yardstick_Assignment.ipynb` — Main notebook with all code and examples.

## Example Output

- Summarized chat history as bullet points.
- Extracted contact info as JSON, validated against schema.

---

**Note:**  
If the Groq API key is not set, the notebook will use fallback logic for

# Dispatch — AI Assistant with Flask

Dispatch is a small web-based AI assistant for asking questions and summarizing emails. It pairs a Flask backend powered by the OpenAI API with a warm, paper-inspired interface.

## Features

- Ask a question and receive an AI-generated answer.
- Paste an email and get a concise 2–3 sentence summary.
- See responses revealed with a typewriter effect.
- Use a responsive, note-card-inspired interface with reduced-motion support.

## Tech stack

- **Backend:** Python, Flask
- **AI:** OpenAI Responses API (`gpt-5.4`)
- **Frontend:** HTML, CSS, and vanilla JavaScript
- **Configuration:** `python-dotenv`

## Getting started

### Prerequisites

- Python 3
- An OpenAI API key

### Install and run

1. Clone the repository and open its directory:

   ```bash
   git clone <your-repository-url>
   cd AI_Assistant_withFlask
   ```

2. Create and activate a virtual environment:

   **Windows PowerShell**

   ```powershell
   python -m venv .venv
   .\.venv\Scripts\Activate.ps1
   ```

   **macOS / Linux**

   ```bash
   python -m venv .venv
   source .venv/bin/activate
   ```

3. Install the dependencies:

   ```bash
   python -m pip install -r requirements.txt
   ```

4. Add your API key to a `.env` file in the project root:

   ```env
   OPENAI_API_KEY=your_openai_api_key
   ```

   Keep `.env` private. Do not commit API keys or other secrets to GitHub.

5. Start the app:

   ```bash
   python main.py
   ```

6. Open [http://127.0.0.1:5000](http://127.0.0.1:5000) in your browser.

The development server runs with Flask debug mode enabled. Do not use it as a production server.

## Project structure

```text
AI_Assistant_withFlask/
├── main.py
├── templates/
│   └── index.html
└── static/
    └── style.css
```

## API endpoints

| Method | Endpoint | Form field | Description |
| --- | --- | --- | --- |
| `POST` | `/ask` | `question` | Answers a question and returns `{"response": "..."}`. |
| `POST` | `/summarize` | `email` | Summarizes an email and returns `{"response": "..."}`. |

Both endpoints expect form data and use the OpenAI API key configured in `.env`.

## License

No license has been specified for this project yet.

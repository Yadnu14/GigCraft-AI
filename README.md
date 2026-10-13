# GigCraft AI

A local AI assistant that turns freelance client briefs into structured project plans.

GigCraft AI uses Flask, Ollama, and Gemma 3:4B to generate proposal drafts, deliverables, timelines, pricing considerations, clarification questions, and next steps.

## Features

- Generate client proposal drafts
- Organize deliverables and project milestones
- Identify missing project requirements
- Consider budgets and deadlines
- Copy generated results
- Run AI generation locally through Ollama

## Technology Stack

- Python
- Flask
- HTML, CSS, JavaScript
- Ollama
- Gemma 3:4B

## Requirements

- Python
- Ollama
- The `gemma3:4b` model

## Run Locally

Install dependencies:

```bash
python -m pip install Flask requests
```

Verify the model:

```bash
ollama list
```

Start the application:

```bash
python app.py
```

Open http://127.0.0.1:5000 in your browser.

## How It Works

The Flask backend sends a structured prompt to a locally running Ollama instance. Gemma 3:4B generates the response, which is displayed in the browser.

The application uses `http://localhost:11434/api/generate` for local model inference and does not require a hosted AI API key.

## Privacy

AI generation is configured to use a local Ollama instance rather than a third-party hosted inference API. Users should still protect sensitive client information.

## Limitations

- AI-generated content requires human review.
- Pricing considerations are not verified market rates.
- Timelines depend on the project scope.
- Ollama must be running locally.

## License

This project is licensed under the MIT License. See [LICENSE](LICENSE).

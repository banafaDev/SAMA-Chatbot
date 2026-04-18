<div align="center">

# SAMABot 🤖

A simple bilingual chatbot for answering questions about the **SAMA Consumer Protection** document.

[![Python](https://img.shields.io/badge/Python-3.11+-blue.svg)](https://www.python.org/)
[![Jupyter Notebook](https://img.shields.io/badge/Jupyter-Notebook-orange.svg)](https://jupyter.org/)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Gemini](https://img.shields.io/badge/LLM-Gemini-blueviolet.svg)](https://ai.google.dev/)

</div>

## Overview

This project uses a retrieval-based chatbot flow to answer user questions from the official SAMA Consumer Protection PDF:

https://sama.gov.sa/en-US/LawsRegulations/ConsumerProtectionRules/Consumer_Protection_EN.pdf

## Features ✨

- Reads the PDF document from the project folder
- Splits the document into chunks for retrieval
- Uses the document context to generate answers
- Supports both Arabic and English
- Simple notebook-based workflow for quick validation

## Model Used 🧠

Current notebook version uses Google Gemini:

- `gemini-2.5-flash-lite`

## Project Structure 📁

- `SAMA_ChatBot.ipynb` - main notebook
- `Consumer_Protection_EN.pdf` - source document
- `README.md` - project overview
- `LICENSE` - project license

## Requirements 🛠️

- Python 3.11+
- Jupyter Notebook (or JupyterLab)
- `google-genai`
- `PyPDF2`
- Google Gemini API key (`GOOGLE_API_KEY`)

## Setup 🚀

1. Put `Consumer_Protection_EN.pdf` in the same folder as the notebook.
2. Install dependencies:

```bash
pip install google-genai PyPDF2
```

3. Open `SAMA_ChatBot.ipynb` and run the cells in order.
4. Set your Gemini API key as an environment variable:

```bash
export GOOGLE_API_KEY="your_api_key_here"
```

## Usage 💬

Ask questions like:

- What is SAMA?
- What are my rights as a bank customer?
- How are complaints handled?

## Testing ✅

Quick manual validation in the notebook:

1. Run all cells in `SAMA_ChatBot.ipynb`.
2. Ask one question that should exist in the PDF (for example: "What is SAMA?").
3. Ask one very specific question that is likely outside the document.
4. Confirm the bot gives a helpful fallback message when details are not covered.

## Notes ⚠️

- The bot should answer only from the PDF context.
- If the answer is not in the document, it should return the fallback message.
- Keep your API keys out of the notebook before pushing to GitHub.

## License 📄

This project is licensed under the MIT License. See [LICENSE](LICENSE).

---

Made for learning and document-based question answering.

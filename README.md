# AI Astrologer

A simple Streamlit app that collects birth details (Name, Date, Time, Place), generates a fun astrology-style reading (rule-based), and answers a free-text question.

## Features

- Clean UI with inputs for name, birth date, time, and place
- Rule-based reading using Zodiac sign, element, life path number, and time-of-day traits
- Free-text Q&A with deterministic, profile-aware responses
- Lightweight, offline — no external APIs

## Prerequisites

- Python 3.9+

## Setup

```bash
# 1) (Optional) Create and activate a virtual environment
python3 -m venv .venv
source .venv/bin/activate

# 2) Install dependencies
pip install -r requirements.txt
```

## Run the app

```bash
streamlit run app.py
```

It will open in your browser (usually http://localhost:8501). Fill in your details and click “Get Reading”. Ask a question in the Q&A section and click “Ask the Oracle”.

## Tests

Core logic is covered by a few unit tests. They don't require Streamlit.

```bash
pytest -q
```

## Demo video (2–5 minutes)

Record a quick walkthrough showing:

1) Launching the app (streamlit run)
2) Entering sample details
3) Generating the reading (overview of sign, element, traits)
4) Asking a free-form question and getting the response

Suggested recording methods on macOS:

- QuickTime Player: File → New Screen Recording
- Loom or any other screen recorder

Save the video as MP4 or MOV and share the link along with this codebase.

## Project structure

- `app.py` — Streamlit UI
- `astrologer/core.py` — Pure Python core logic (zodiac, life path, reading, Q&A)
- `tests/test_core.py` — Unit tests for core logic
- `requirements.txt` — Dependencies

## Notes

- The astrology logic is intentionally simple and for entertainment only.
- All responses are deterministic for the same inputs (seeded), so your demo will be reproducible.

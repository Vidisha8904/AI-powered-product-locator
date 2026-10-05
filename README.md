# Shelf Product Locator

A small Streamlit app that lets users upload a supermarket shelf photo, enter a product name, and receive an annotated image showing detected matches.

## Features

- Normalize misspelled product names with Gemini
- Locate products in shelf images with structured Gemini vision output
- Draw one or more bounding boxes on the uploaded image
- Gracefully handle not-found and low-confidence cases

## Setup

1. Install dependencies:
   ```bash
   pip install -r requirements.txt
   ```
2. Copy the example environment file and add your key:
   ```bash
   copy .env.example .env
   ```
   Then fill in your Gemini API key.

## Run the notebook

Open the notebook in [notebooks/test_pipeline.ipynb](notebooks/test_pipeline.ipynb) and run the cells to test each stage interactively.

## Run the app locally

```bash
streamlit run app.py
```

## Deploy to Streamlit Community Cloud

1. Push this repository to GitHub.
2. Create a new app on Streamlit Community Cloud and connect the repo.
3. Set the environment variable `GEMINI_API_KEY` in Streamlit secrets.
4. Deploy the app.

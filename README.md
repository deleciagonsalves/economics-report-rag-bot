# Economic Report Q&A Assistant (RAG)

A Python tool that reads an economic report (PDF) and answers questions using only the text of that document, showing the sources it used.

## How it works
1. Reads the PDF with pypdf and splits it into chunks
2. Converts chunks to embeddings with sentence-transformers
3. Finds the chunks closest to the question (cosine similarity)
4. Uses a Hugging Face model (flan-t5-base) to write the answer

## Tech stack
Python, pypdf, sentence-transformers, Hugging Face Transformers, Google Colab

## How to run
Open the notebook in Google Colab, click Runtime > Run all, and upload a PDF (e.g. the RBI Monetary Policy Statement, October 2026).

## Limitations
The small free model sometimes gives very short answers, so the sources it prints should always be checked.

## Future improvements
Page numbers in sources, a bigger model, and a chat interface.

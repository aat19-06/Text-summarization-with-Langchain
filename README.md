# 📝 Text Summarization with LangChain

This notebook explores how different document summarization strategies work in LangChain. The goal wasn't just to generate summaries, but to understand why multiple approaches exist and when each one should be used.

## What this notebook covers

* Loading PDF documents
* Splitting large documents into chunks
* Stuff Document Chain
* Map-Reduce Chain
* Refine Chain
* Prompt templates for summarization
* Context window limitations

## Why different chains?

### Stuff

The entire document is passed to the LLM in a single prompt. This works well for smaller documents but becomes impractical once the document exceeds the model's context window.

### Map-Reduce

The document is divided into smaller chunks. Each chunk is summarized independently, and those summaries are combined to produce a final summary. This approach scales much better for larger documents.

### Refine

Instead of combining independent summaries, the model starts with an initial summary and updates it as it processes each new chunk. This helps preserve context across long documents.

## Tech Stack

* Python
* LangChain
* OpenAI / Groq
* PyPDF
* Jupyter Notebook

## What I learned

* How context windows affect LLM applications
* Why document chunking is important
* The differences between Stuff, Map-Reduce, and Refine
* Building prompt templates for summarization
* Choosing the right summarization strategy based on document size

## Running the notebook

```bash
pip install -r requirements.txt
```

Open `text_summarization.ipynb` and run the cells in order.
